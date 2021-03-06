---
description: GetChildren (método) (ADO)
title: GetChildren (método) (ADO) | Microsoft Docs
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
apitype: COM
f1_keywords:
- _Record::raw_GetChildren
- _Record::GetChildren
helpviewer_keywords:
- GetChildren method [ADO]
ms.assetid: b3f09bac-4f66-49f6-aa5a-6fbb4fb28338
author: rothja
ms.author: jroth
ms.openlocfilehash: ea59a94f095a438be8fc7009a58179d488af20a2
ms.sourcegitcommit: 18a98ea6a30d448aa6195e10ea2413be7e837e94
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "88972836"
---
# <a name="getchildren-method-ado"></a>GetChildren (método) (ADO)
Devuelve un [conjunto de registros](./recordset-object-ado.md) cuyas filas representan los elementos secundarios de un [registro](./record-object-ado.md)de la colección.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
Set recordset = record.GetChildren  
```  
  
## <a name="return-value"></a>Valor devuelto  
 Objeto de **conjunto de registros** para el que cada fila representa un elemento secundario del objeto de **registro** actual. Por ejemplo, los elementos secundarios de un **registro** que representa un directorio serían los archivos y subdirectorios contenidos en el directorio primario.  
  
## <a name="remarks"></a>Observaciones  
 El proveedor determina qué columnas existen en el **conjunto de registros**devuelto. Por ejemplo, un proveedor de origen de documento siempre devuelve un **conjunto de registros**de recursos.  
  
## <a name="applies-to"></a>Se aplica a  

:::row:::
    :::column:::
        [Objeto Record (ADO)](./record-object-ado.md)  
    :::column-end:::
    :::column:::
        [Objeto de conjunto de registros (ADO)](./recordset-object-ado.md)  
    :::column-end:::
:::row-end:::