---
description: sp_helpdistributor_properties (Transact-SQL)
title: sp_helpdistributor_properties (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/03/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: language-reference
f1_keywords:
- sp_helpdistributor_properties_TSQL
- sp_helpdistributor_properties
helpviewer_keywords:
- sp_helpdistributor_properties
ms.assetid: ee267724-3244-49eb-84c9-f38dbefdd639
author: markingmyname
ms.author: maghan
ms.openlocfilehash: 51dc2311b4fffae164d0b1ac789289f1638c3b36
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89543315"
---
# <a name="sp_helpdistributor_properties-transact-sql"></a>sp_helpdistributor_properties (Transact-SQL)
[!INCLUDE [SQL Server SQL MI](../../includes/applies-to-version/sql-asdbmi.md)]

  Devuelve las propiedades del distribuidor. Este procedimiento almacenado se ejecuta en el distribuidor de la base de datos de distribución.  
  
 ![Icono de vínculo de tema](../../database-engine/configure-windows/media/topic-link.gif "Icono de vínculo de tema") [Convenciones de sintaxis de Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
sp_helpdistributor_properties   
```  
  
## <a name="result-set"></a>Tipo de cursor  
  
|Nombre de la columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|**heartbeat_interval**|**int**|Número máximo de minutos que un agente puede ejecutarse sin registrar un mensaje de progreso.|  
  
## <a name="return-code-values"></a>Valores de código de retorno  
 **0** (correcto) o **1** (error)  
  
## <a name="remarks"></a>Observaciones  
 **sp_helpdistributor_properties** se usa con todos los tipos de replicación.  
  
## <a name="permissions"></a>Permisos  
 Solo los miembros del rol fijo de servidor **sysadmin** , los miembros del rol fijo de base de datos **db_owner** o **replmonitor** en la base de datos de distribución y los usuarios de la lista de acceso a la publicación (PAL) para una publicación que usa este distribuidor pueden ejecutar **sp_helpdistributor_properties**.  
  
## <a name="see-also"></a>Consulte también  
 [sp_changedistributor_property &#40;&#41;de Transact-SQL ](../../relational-databases/system-stored-procedures/sp-changedistributor-property-transact-sql.md)  
  
  
