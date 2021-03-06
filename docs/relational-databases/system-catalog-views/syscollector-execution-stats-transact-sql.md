---
description: syscollector_execution_stats (Transact-SQL)
title: syscollector_execution_stats (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 06/10/2016
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- syscollector_execution_stats
- syscollector_execution_stats_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- syscollector_execution_stats view
- data collector view
ms.assetid: 23e35ac5-fbbf-4922-970c-f4fac44c1263
author: markingmyname
ms.author: maghan
ms.openlocfilehash: d0819aba312ddfaceaff092815b1c78297308dd6
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89550363"
---
# <a name="syscollector_execution_stats-transact-sql"></a>syscollector_execution_stats (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Proporciona información sobre la ejecución de la tarea para un paquete o un conjunto de recopilación.  
  
|Nombre de la columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|**log_id**|**bigint**|Identifica cada ejecución del conjunto de recopilación. Se usa para combinar esta vista con otros registros detallados. No admite valores NULL.|  
|**task_name**|**nvarchar(128)**|El nombre de la tarea de paquete o de conjunto de recopilación a la que corresponde esta información. No admite valores NULL.|  
|**execution_row_count_in**|**int**|Número de filas procesadas al principio del flujo de datos. Acepta valores NULL.|  
|**execution_row_count_out**|**int**|Número de filas procesadas al final del flujo de datos. Acepta valores NULL.|  
|**execution_row_count_errors**|**int**|Número de filas que dieron error durante el flujo de datos. Acepta valores NULL.|  
|**execution_time_ms**|**int**|Tiempo, en milisegundos, necesario para completar la tarea. Acepta valores NULL.|  
|**log_time**|**datetime**|Momento en que se registró la información. No admite valores NULL.|  
  
## <a name="permissions"></a>Permisos  
 Requiere el permiso SELECT para **dc_operator**.  
  
## <a name="see-also"></a>Vea también  
 [Procedimientos almacenados del recopilador de datos &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/data-collector-stored-procedures-transact-sql.md)   
 [Vistas del recopilador de datos &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/data-collector-views-transact-sql.md)   
 [Recopilación de datos](../../relational-databases/data-collection/data-collection.md)  
  
  
