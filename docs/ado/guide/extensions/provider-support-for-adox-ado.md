---
description: Compatibilidad del proveedor con ADOX (ADO)
title: Compatibilidad del proveedor con ADOX (ADO) | Microsoft Docs
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
helpviewer_keywords:
- ADOX provider support [ADO]
ms.assetid: 64234ce5-dc46-4c8a-a316-61956b6b9abb
author: rothja
ms.author: jroth
ms.openlocfilehash: cbc2b4821ac5c57c2302892caff1afa742e829b9
ms.sourcegitcommit: 18a98ea6a30d448aa6195e10ea2413be7e837e94
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "88978696"
---
# <a name="provider-support-for-adox-ado"></a>Compatibilidad del proveedor con ADOX (ADO)
Ciertas características de ADOX no se admiten, en función del proveedor de datos de OLE DB. ADOX es totalmente compatible con el [proveedor de OLE DB para Microsoft Jet](../appendixes/microsoft-ole-db-provider-for-microsoft-jet.md). En las tablas siguientes se enumeran las características no admitidas con el [proveedor de microsoft OLE DB para SQL Server](../appendixes/microsoft-ole-db-provider-for-sql-server.md), el [proveedor de Microsoft OLE DB para ODBC](../appendixes/microsoft-ole-db-provider-for-odbc.md)o el [proveedor OLE DB de Microsoft para Oracle](../appendixes/microsoft-ole-db-provider-for-oracle.md) . ADOX no es compatible con ningún otro proveedor de Microsoft OLE DB.  
  
## <a name="microsoft-ole-db-provider-for-sql-server"></a>Proveedor OLE DB de Microsoft para SQL Server  
  
|Objeto o colección|Restricción de uso|  
|--------------------------|-----------------------|  
|Colección de **tablas**|Las propiedades son de lectura y escritura antes de la creación de objetos y de solo lectura cuando se hace referencia a un objeto existente.|  
|Colección de **vistas**|No se admiten **vistas** .|  
|Colección de **procedimientos**|No se admiten los métodos **Append** y **Delete** .|  
|**Procedure** (objeto)|No se admite la propiedad **Command** .|  
|Colección de **claves**|No se admiten los métodos **Append** y **Delete** .|  
|Recopilación de **usuarios**|No se admiten **usuarios** .|  
|Colección de **grupos**|No se admiten **grupos** .|  
  
## <a name="microsoft-ole-db-provider-for-odbc"></a>Proveedor Microsoft OLE DB para ODBC  
  
|Objeto o colección|Restricción de uso|  
|--------------------------|-----------------------|  
|Objeto de **Catálogo**|No se admite el método **Create** .|  
|Colección de **tablas**|No se admiten los métodos **Append** y **Delete** . Las propiedades son de lectura y escritura antes de la creación de objetos y de solo lectura cuando se hace referencia a un objeto existente.|  
|Colección de **procedimientos**|No se admiten los métodos **Append** y **Delete** .|  
|**Procedure** (objeto)|No se admite la propiedad **Command** .|  
|Colección de **índices**|No se admiten los métodos **Append** y **Delete** .|  
|Colección de **claves**|No se admiten los métodos **Append** y **Delete** .|  
|Recopilación de **usuarios**|No se admiten **usuarios** .|  
|Colección de **grupos**|No se admiten **grupos** .|  
  
## <a name="microsoft-ole-db-provider-for-oracle"></a>proveedor Microsoft OLE DB para Oracle  
  
|Objeto o colección|Restricción de uso|  
|--------------------------|-----------------------|  
|Objeto de **Catálogo**|No se admite el método **Create** .|  
|Colección de **tablas**|No se admiten los métodos **Append** y **Delete** . Las propiedades son de lectura y escritura antes de la creación de objetos y de solo lectura cuando se hace referencia a un objeto existente.|  
|Colección de **vistas**|No se admiten los métodos **Append** y **Delete** .|  
|Objeto de **vista**|No se admite la propiedad **Command** .|  
|**Procedures** (objeto)|No se admiten los métodos **Append** y **Delete** .|  
|**Procedure** (objeto)|No se admite la propiedad **Command** .|  
|Colección de **índices**|No se admiten los métodos **Append** y **Delete** .|  
|Colección de **claves**|No se admiten los métodos **Append** y **Delete** .|  
|Recopilación de **usuarios**|No se admiten **usuarios** .|  
|Colección de **grupos**|No se admiten **grupos** .|