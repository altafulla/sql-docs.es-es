---
description: sp_posttracertoken (Transact-SQL)
title: sp_posttracertoken (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: replication
ms.topic: language-reference
f1_keywords:
- posttracerttoken
- posttracerttoken_TSQL
- sp_posttracertoken
- sp_posttracertoken_TSQL
helpviewer_keywords:
- sp_posttracertoken
ms.assetid: 24da5cd2-1c45-475e-93db-5bdf660f1c2c
author: markingmyname
ms.author: maghan
ms.openlocfilehash: aa46de0f06b0566de0a221ed8f7ca7bf97443836
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89545986"
---
# <a name="sp_posttracertoken-transact-sql"></a>sp_posttracertoken (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Este procedimiento envía un testigo de seguimiento al registro de transacciones del publicador y empieza el proceso de seguimiento de las estadísticas de latencia. La información se registra cuando el token de seguimiento se escribe en el registro de transacciones, cuando lo recoge el Agente de registro del LOG y cuando lo aplica el Agente de distribución. Este procedimiento almacenado se ejecuta en el publicador de la base de datos de publicación. Para más información, consulte [Medir la latencia y validar las conexiones de la replicación transaccional](../../relational-databases/replication/monitor/measure-latency-and-validate-connections-for-transactional-replication.md).  
  
 ![Icono de vínculo de tema](../../database-engine/configure-windows/media/topic-link.gif "Icono de vínculo de tema") [Convenciones de sintaxis de Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
sp_posttracertoken [ @publication = ] 'publication'   
    [ , [ @tracer_token_id = ] tracer_token_id OUTPUT  
    [ , [ @publisher = ] 'publisher'   
```  
  
## <a name="arguments"></a>Argumentos  
`[ @publication = ] 'publication'` Es el nombre de la publicación para la que se está midiendo la latencia. *Publication* es de **tipo sysname**y no tiene ningún valor predeterminado.  
  
`[ @tracer_token_id = ] _tracer_token_id OUTPUT` Es el identificador del testigo de seguimiento insertado. *tracer_token_id* es de **tipo int** y su valor predeterminado es null, y es un parámetro de salida. Este valor se puede usar para ejecutar [sp_helptracertokenhistory &#40;&#41;de Transact-SQL ](../../relational-databases/system-stored-procedures/sp-helptracertokenhistory-transact-sql.md) o [sp_deletetracertokenhistory &#40;Transact-SQL ](../../relational-databases/system-stored-procedures/sp-deletetracertokenhistory-transact-sql.md)&#41;sin ejecutar primero sp_helptracertokens &#40;[de Transact-SQL ](../../relational-databases/system-stored-procedures/sp-helptracertokens-transact-sql.md).  
  
`[ @publisher = ] 'publisher'` Especifica un publicador que no es de [!INCLUDE[msCoName](../../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] . *Publisher* es de **tipo sysname, su**valor predeterminado es NULL y no se debe especificar para un [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] publicador.  
  
## <a name="return-code-values"></a>Valores de código de retorno  
 **0** (correcto) o **1** (error)  
  
## <a name="remarks"></a>Observaciones  
 **sp_posttracertoken** se utiliza en la replicación transaccional.  
  
## <a name="example"></a>Ejemplo  
 [!code-sql[HowTo#sp_tracertokens](../../relational-databases/replication/codesnippet/tsql/sp-posttracertoken-trans_1.sql)]  
  
## <a name="permissions"></a>Permisos  
 Solo los miembros del rol fijo de servidor **sysadmin** o del rol fijo de base de datos **db_owner** pueden ejecutar **sp_posttracertoken**.  
  
## <a name="see-also"></a>Consulte también  
 [Medir la latencia y validar las conexiones de la replicación transaccional](../../relational-databases/replication/monitor/measure-latency-and-validate-connections-for-transactional-replication.md)  
  
  
