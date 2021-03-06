---
title: ISSAsynchStatus::Abort (controlador OLE DB) | Microsoft Docs
description: Obtenga información sobre cómo el método ISSAsynchStatus::Abort cancela una operación de ejecución asincrónica en OLE DB Driver for SQL Server.
ms.custom: ''
ms.date: 06/14/2018
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: connectivity
ms.topic: reference
apiname:
- ISSAsynchStatus::Abort (OLE DB)
apitype: COM
helpviewer_keywords:
- Abort method
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: cbbef11ae17029500a6910e5b28c121f6312dce2
ms.sourcegitcommit: c95f3ef5734dec753de09e07752a5d15884125e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/25/2020
ms.locfileid: "88862204"
---
# <a name="issasynchstatusabort-ole-db"></a>ISSAsynchStatus::Abort (OLE DB)
[!INCLUDE [SQL Server](../../../includes/applies-to-version/sql-asdb-asdbmi-asa-pdw.md)]

[!INCLUDE[Driver_OLEDB_Download](../../../includes/driver_oledb_download.md)]

  Cancela una operación que se ejecuta de forma asincrónica.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
HRESULT Abort(  
        HCHAPTER hChapter,  
        DBASYNCHOP eOperation);  
```  
  
## <a name="arguments"></a>Argumentos  
 *hChapter*[in]  
 El identificador del segmento para el que se anula la operación. Si el objeto al que se llama no es un objeto de conjunto de filas o la operación no se aplica a un segmento, el autor de la llamada debe establecer *hChapter* en DB_NULL_HCHAPTER.  
  
 *eOperation*[in]  
 Operación para anular. Se debe usar el siguiente valor:  
  
 DBASYNCHOP_OPEN-La solicitud para cancelar se aplica a la apertura o rellenado asincrónico de un conjunto de filas o a la inicialización asincrónica de un objeto de origen de datos.  
  
## <a name="return-code-values"></a>Valores de código de retorno  
 S_OK  
 Se procesó la solicitud para cancelar la operación asincrónica. Esto no garantiza que la operación en sí se haya cancelado. Para determinar si se canceló la operación, el consumidor debería llamar a [ISSAsynchStatus::GetStatus](../../oledb/ole-db-interfaces/issasynchstatus-getstatus-ole-db.md) y realizar una comprobación para DB_E_CANCELED; sin embargo, puede que no se devuelva en la llamada siguiente.  
  
 DB_E_CANTCANCEL  
 La operación asincrónica no puede cancelarse.  
  
 DB_E_CANCELED  
 La solicitud para anular la operación asincrónica se canceló durante las notificaciones. La operación todavía se está ejecutando de forma asincrónica.  
  
 E_FAIL  
 Se produjo un error específico del proveedor.  
  
 E_INVALIDARG  
 El parámetro *hChapter* no es DB_NULL_HCHAPTER, o bien *eOperation* no es DBASYNCH_OPEN.  
  
 E_UNEXPECTED  
 Se ha llamado a `ISSAsynchStatus::Abort` en un objeto de origen de datos en el que no se ha llamado a `IDBInitialize::Initialize`, o bien no se ha completado.  
  
 Se ha llamado a `ISSAsynchStatus::Abort` en un objeto de origen de datos en el que se ha llamado a `IDBInitialize::Initialize` e inmediatamente se ha cancelado antes de la inicialización o se ha agotado el tiempo de espera. Todavía no se ha inicializado el objeto de origen de datos.  
  
 Se ha llamado a `ISSAsynchStatus::Abort` en un conjunto de filas en el que previamente se había llamado a `ITransaction::Commit` o a `ITransaction::Abort`, y el conjunto de filas no ha conservado la confirmación o anulación y se encuentra en un estado zombi.  
  
 Se llamó a`ISSAsynchStatus::Abort` en un conjunto de filas que se canceló de forma asincrónica en su fase de inicialización. El conjunto de filas se encuentra en estado inerte.  
  
## <a name="remarks"></a>Observaciones  
 Al anular la inicialización de un conjunto de filas u objeto de origen de datos, se podría dejar el conjunto de filas u objeto de origen de datos en un estado zombi, de forma que todos los métodos distintos de los métodos `IUnknown` devuelvan un valor E_UNEXPECTED. Si esto sucede, la única acción posible para el consumidor es liberar el conjunto de filas u objeto de origen de datos.  
  
 Llamando a `ISSAsynchStatus::Abort` y pasando un valor para *eOperation* distinto de DBASYNCHOP_OPEN, devuelve S_OK. Este valor no implica que la operación se haya completado o cancelado.  
  
## <a name="see-also"></a>Consulte también  
 [Realizar operaciones asincrónicas](../../oledb/features/performing-asynchronous-operations.md)  
  
  
