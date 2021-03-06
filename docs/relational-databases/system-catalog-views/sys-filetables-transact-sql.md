---
description: sys.filetables (Transact-SQL)
title: Sys. filetables (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- filetables
- filetables_TSQL
- sys.filetables
- sys.filetables_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sys.filetables catalog view
ms.assetid: a740be59-cd52-4707-9ad2-5203669a63ac
author: markingmyname
ms.author: maghan
ms.openlocfilehash: be56d53636a4916a402df709c5a7f7a0b3725dc8
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89542548"
---
# <a name="sysfiletables-transact-sql"></a>sys.filetables (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Devuelve una fila para cada objeto FileTable de [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)]. Para más información sobre FileTables, vea [FileTables &#40;SQL Server&#41;](../../relational-databases/blob/filetables-sql-server.md).    
  
|Nombre de la columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|**object_id**||Número de identificación del objeto. Es único en una base de datos.<br /><br /> Para obtener más información, [Sys. objects &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-objects-transact-sql.md).|  
|**is_enabled**|**bit**|1 = FileTable está en el estado "habilitado".|  
|**directory_name**|**VARCHAR(255**|Nombre del directorio raíz de un objeto FileTable.|  
|**filename_collation_id**||Es el identificador de intercalación definido para el FileTable|  
|**filename_collation_name**||Es el nombre de intercalación definido para el FileTable.|  
  
## <a name="see-also"></a>Consulte también  
 [Administrar FileTables](../../relational-databases/blob/manage-filetables.md)   
 [FileTables &#40;SQL Server&#41;](../../relational-databases/blob/filetables-sql-server.md)  
  
  
