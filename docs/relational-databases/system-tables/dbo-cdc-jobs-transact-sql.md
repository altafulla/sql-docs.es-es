---
description: dbo.cdc_jobs (Transact-SQL)
title: DBO. cdc_jobs (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- cdc_jobs
- cdc_jobs_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- dbo.cdc_jobs
ms.assetid: 85e2d580-1c54-4b81-b7e6-2e12997199fd
author: markingmyname
ms.author: maghan
ms.openlocfilehash: 5c7b71f64a66adaf829bd4041a0a14f4e91e30dc
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89551082"
---
# <a name="dbocdc_jobs-transact-sql"></a>dbo.cdc_jobs (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Almacena los parámetros de configuración de captura de datos del cambio para trabajos de captura y limpieza. Esta tabla se almacena en **msdb**.  
  
 
  
|Nombre de la columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|**database_id**|**int**|Id. de la base de datos en la que se ejecuta el trabajo.|  
|**job_type**|**nvarchar (20)**|Tipo de trabajo, que puede ser 'capture' o 'cleanup'.|  
|**job_id**|**uniqueidentifier**|Id. único asociado al trabajo.|  
|**maxtrans**|**int**|Número máximo de transacciones que se van a procesar en cada ciclo de examen.<br /><br /> **maxtrans** solo es válido para los trabajos de captura.|  
|**maxscans**|**int**|El número máximo de ciclos de recorrido para ejecutar en orden y extraer todas las filas del registro.<br /><br /> **maxscans** solo es válido para los trabajos de captura.|  
|**continua**|**bit**|Una marca que indica si el trabajo de captura debe ejecutarse continuamente (1) o solo una vez (0). Para obtener más información, vea [Sys. sp_cdc_add_job &#40;&#41;de Transact-SQL ](../../relational-databases/system-stored-procedures/sys-sp-cdc-add-job-transact-sql.md).<br /><br /> **Continuous** solo es válido para los trabajos de captura.|  
|**PollingInterval**|**bigint**|El número de segundos entre los ciclos del recorrido del registro.<br /><br /> **PollingInterval** solo es válido para los trabajos de captura.|  
|**políticas**|**bigint**|El número de minutos que se conservan las filas de cambios en las tablas de cambios.<br /><br /> la **retención** solo es válida para los trabajos de limpieza.|  
|**threshold**|**bigint**|El número máximo de entradas correspondientes a operaciones de eliminación que se pueden eliminar mediante una única instrucción durante el proceso de limpieza.|  
  
## <a name="see-also"></a>Consulte también  
 [Sys. sp_cdc_add_job &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sys-sp-cdc-add-job-transact-sql.md)   
 [Sys. sp_cdc_change_job &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sys-sp-cdc-change-job-transact-sql.md)   
 [Sys. sp_cdc_help_jobs &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sys-sp-cdc-help-jobs-transact-sql.md)   
 [Sys. sp_cdc_drop_job &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sys-sp-cdc-drop-job-transact-sql.md)  
  
  
