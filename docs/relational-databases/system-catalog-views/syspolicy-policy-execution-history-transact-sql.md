---
description: syspolicy_policy_execution_history (Transact-SQL)
title: syspolicy_policy_execution_history (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- syspolicy_policy_execution_history_TSQL
- syspolicy_policy_execution_history
dev_langs:
- TSQL
helpviewer_keywords:
- syspolicy_policy_execution_history view
ms.assetid: b13c44a7-6d49-4d50-abe1-e657fc52bb05
author: VanMSFT
ms.author: vanto
ms.openlocfilehash: 499f67e29a9d6a4205dd04acc325bf10bc917fc2
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88493832"
---
# <a name="syspolicy_policy_execution_history-transact-sql"></a>syspolicy_policy_execution_history (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Muestra el momento en que se ejecutaron las directivas, el resultado de cada ejecución y detalles sobre errores, si se produjo alguno. En la tabla siguiente se describen las columnas de la vista de syspolicy_policy_execution_history.  
  
|Nombre de la columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|history_id|**bigint**|Identificador de este registro. Cada registro indica una directiva y el momento en que se inició.|  
|policy_id|**int**|Identificador de la directiva.|  
|start_date|**datetime**|Fecha y hora en que intentó ejecutarse esta directiva.|  
|end_date|**datetime**|Momento en que terminó de ejecutarse esta directiva.|  
|resultado|**bit**|Corrección o error de la directiva. 0 = error, 1 = correcto.|  
|exception_message|**nvarchar(max)**|Mensaje generado por la excepción, si se produjo alguna.|  
|excepción|**nvarchar(max)**|Descripción de la excepción, si se produjo alguna.|  
  
## <a name="remarks"></a>Observaciones  
 La vista [syspolicy_policy_execution_history_details](../../relational-databases/system-catalog-views/syspolicy-policy-execution-history-details-transact-sql.md) contiene información relacionada con los destinos de la Directiva y las expresiones de condición probadas.  
  
## <a name="permissions"></a>Permisos  
 Requiere la pertenencia al rol PolicyAdministratorRole en la base de datos msdb.  
  
## <a name="see-also"></a>Consulte también  
 [Administrar servidores mediante la administración basada en directivas](../../relational-databases/policy-based-management/administer-servers-by-using-policy-based-management.md)   
 [Vistas de administración basada en directivas &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/policy-based-management-views-transact-sql.md)  
  
  
