---
description: MSpeer_response (Transact-SQL)
title: MSpeer_response (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/06/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: language-reference
f1_keywords:
- MSpeer_response
- MSpeer_response_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- MSpeer_response system table
ms.assetid: 510e24cf-0292-47a9-b1d9-71a30fef030f
author: markingmyname
ms.author: maghan
ms.openlocfilehash: 7e6133bee999ad828516f908aaf770321a59ec3c
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89545593"
---
# <a name="mspeer_response-transact-sql"></a>MSpeer_response (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  La tabla **MSpeer_response** se utiliza en la replicación punto a punto para almacenar la respuesta de cada nodo a una solicitud de estado de publicación. Esta tabla se almacena en la base de datos de publicación.  
  
## <a name="definition"></a>Definición  
  
|Nombre de la columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|**id_de_solicitud**|**int**|Identifica una entrada de solicitud de estado en la tabla [MSpeer_request](../../relational-databases/system-tables/mspeer-request-transact-sql.md) .|  
|**personas**|**sysname**|Nodo del mismo nivel que generó la respuesta.|  
|**peer_db**|**sysname**|Base de datos de suscripciones del nodo del mismo nivel que generó la respuesta.|  
|**received_date**|**datetime**|La fecha y hora en que se recibió la solicitud del mismo nivel.|  
  
## <a name="see-also"></a>Consulte también  
 [Tablas de replicación &#40;Transact-SQL&#41;](../../relational-databases/system-tables/replication-tables-transact-sql.md)  
  
  
