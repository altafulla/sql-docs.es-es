---
description: MSreplication_subscriptions (Transact-SQL)
title: MSreplication_subscriptions (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: language-reference
f1_keywords:
- MSreplication_subscriptions
- MSreplication_subscriptions_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- MSreplication_subscriptions system table
ms.assetid: fd0c5843-4e9b-4448-8bfb-0a4067d1d8d1
author: markingmyname
ms.author: maghan
ms.openlocfilehash: b89aee32b5ea431da77043938104960d4d353b74
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89551044"
---
# <a name="msreplication_subscriptions-transact-sql"></a>MSreplication_subscriptions (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  La tabla **MSreplication_subscriptions** contiene una fila de información de replicación para cada agente de distribución atendiendo a la base de datos del suscriptor local. Esta tabla se almacena en la base de datos de suscripciones.  
  
|Nombre de la columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|**publisher**|**sysname**|El nombre del publicador.|  
|**publisher_db**|**sysname**|Nombre de la base de datos del publicador.|  
|**publicaciones**|**sysname**|Nombre de la publicación.|  
|**independent_agent**|**bit**|Indica si hay un agente de distribución independiente para esta publicación.|  
|**subscription_type**|**int**|El tipo de suscripción:<br /><br /> 0 = Inserción.<br /><br /> 1 = Extracción.<br /><br /> 2 = Anónima.|  
|**distribution_agent**|**sysname**|Nombre del Agente de distribución.|  
|**Time**|**smalldatetime**|Hora de la última actualización realizada por el Agente de distribución.|  
|**description**|**nvarchar(255)**|Descripción de la suscripción.|  
|**transaction_timestamp**|**varbinary(16)**|Solo para uso interno.|  
|**update_mode**|**tinyint**|Tipo de actualización.|  
|**agent_id**|**binario (16)**|Id. del agente.|  
|**subscription_guid**|**binario (16)**|Identificador global de la versión de la suscripción en la publicación.|  
|**Subid**|**binario (16)**|Identificador global de una suscripción anónima.|  
|**immediate_sync**|**bit**|Indica si los archivos de sincronización se crean o se vuelven a crear cada vez que se ejecuta el Agente de instantáneas.|  
  
## <a name="see-also"></a>Consulte también  
 [Tablas de replicación &#40;Transact-SQL&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Vistas de replicación &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)   
 [sp_helpsubscription &#40;&#41;de Transact-SQL ](../../relational-databases/system-stored-procedures/sp-helpsubscription-transact-sql.md)  
  
  
