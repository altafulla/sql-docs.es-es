---
description: MSmerge_metadataaction_request (Transact-SQL)
title: MSmerge_metadataaction_request (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: language-reference
f1_keywords:
- MSmerge_metadataaction_request
- MSmerge_metadataaction_request_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- MSmerge_metadataaction_request system table
ms.assetid: cd31a114-900a-4218-ab58-d959e547c647
author: markingmyname
ms.author: maghan
ms.openlocfilehash: 7e616cea34c3c2b440decaec14ac20be3a6bcc30
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89547075"
---
# <a name="msmerge_metadataaction_request-transact-sql"></a>MSmerge_metadataaction_request (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  En la tabla **MSmerge_metadataaction_request** se almacena una fila por cada acción de compensación necesaria. Mediante la sincronización Web, si se produce un error y se debe reintentar la sincronización, se realiza una entrada en **MSmerge_metadataaction_request**. Durante la fase de carga de la mezcla posterior, las solicitudes de todos los artículos pertenecientes a la publicación que se está sincronizando se recuperan de esta taba y se cargan. Cuando la sincronización se haya completado correctamente, se eliminará la fila correspondiente en la tabla de **MSmerge_metadataaction_request** . Esta tabla se almacena en la base de datos de publicación del publicador y en la base de datos de suscripciones del suscriptor.  
  
|Nombre de la columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|**tablenick**|**int**|El alias de la tabla publicada.|  
|**rowguid**|**uniqueidentifier**|Identificador de la fila especificada.|  
|**action**|**tinyint**|Identifica la acción de compensación necesaria.|  
|**última**|**bigint**|El valor de la generación para la que se necesita la acción de compensación.|  
|**cambio**|**int**|Solo para uso interno.|  
  
## <a name="see-also"></a>Consulte también  
 [Tablas de replicación &#40;Transact-SQL&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)   
 [Vistas de replicación &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)   
 [Sincronización web para la replicación de mezcla](../../relational-databases/replication/web-synchronization-for-merge-replication.md)  
  
  
