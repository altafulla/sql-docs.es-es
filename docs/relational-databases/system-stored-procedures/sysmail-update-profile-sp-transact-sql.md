---
description: sysmail_update_profile_sp (Transact-SQL)
title: sysmail_update_profile_sp (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sysmail_update_profile_sp
- sysmail_update_profile_sp_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- sysmail_update_profile_sp
ms.assetid: eaedf7ce-a8d5-4ab9-99e0-d77d5be19e90
author: VanMSFT
ms.author: vanto
ms.openlocfilehash: 78a123514e990499f191cbc6742870647adebc5e
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88454763"
---
# <a name="sysmail_update_profile_sp-transact-sql"></a>sysmail_update_profile_sp (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Cambia la descripción o el nombre de un perfil del Correo electrónico de base de datos.  
  
 ![Icono de vínculo de tema](../../database-engine/configure-windows/media/topic-link.gif "Icono de vínculo de tema") [Convenciones de sintaxis de Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
sysmail_update_profile_sp [ [ @profile_id = ] profile_id , ] [ [ @profile_name = ] 'profile_name' , ]  
    [ [ @description = ] 'description' ]  
```  
  
## <a name="arguments"></a>Argumentos  
`[ @profile_id = ] profile_id` Identificador de perfil que se va a actualizar. *profile_id* es de **tipo int**y su valor predeterminado es NULL. Se debe especificar al menos una de *profile_id* o *profile_name* . Si se especifican los dos, el procedimiento cambia el nombre del perfil.  
  
`[ @profile_name = ] 'profile_name'` Nombre del perfil que se va a actualizar o nombre nuevo del perfil. *profile_name* es de **tipo sysname y su**valor predeterminado es NULL. Se debe especificar al menos una de *profile_id* o *profile_name* . Si se especifican los dos, el procedimiento cambia el nombre del perfil.  
  
`[ @description = ] 'description'` Nueva descripción del perfil. la *Descripción* es de tipo **nvarchar (256)** y su valor predeterminado es NULL.  
  
## <a name="return-code-values"></a>Valores de código de retorno  
 **0** (correcto) o **1** (error)  
  
## <a name="remarks"></a>Observaciones  
 Si se especifican los dos (el Id. de perfil y el nombre de perfil), el procedimiento cambia el nombre del perfil por el nombre proporcionado y actualiza su descripción. Si solo se proporciona uno de estos argumentos, el procedimiento actualiza la descripción del perfil.  
  
 El procedimiento almacenado **sysmail_update_profile_sp** está en la base de datos **msdb** y pertenece al esquema **DBO** . El procedimiento se debe ejecutar con un nombre de tres partes si la base de datos actual no es **msdb**.  
  
## <a name="permissions"></a>Permisos  
 Los permisos de ejecución para este procedimiento tienen como valor predeterminado los miembros del rol fijo de servidor **sysadmin** .  
  
## <a name="examples"></a>Ejemplos  
 **A. Cambiar la descripción de un perfil**  
  
 En el ejemplo siguiente se cambia la descripción del perfil denominado `AdventureWorks Administrator` en la base de datos **msdb** .  
  
```  
EXECUTE msdb.dbo.sysmail_update_profile_sp  
    @profile_name = 'AdventureWorks Administrator'  
    ,@description = 'Administrative mail profile.';  
```  
  
 **B. Cambiar el nombre y la descripción de un perfil**  
  
 En este ejemplo se cambia el nombre y la descripción del perfil con el Id. de perfil `750`.  
  
```  
EXECUTE msdb.dbo.sysmail_update_profile_sp  
    @profile_id = 750  
    ,@profile_name = 'Operator'  
    ,@description = 'Profile to send alert e-mail to operators.';  
```  
  
## <a name="see-also"></a>Consulte también  
 [Correo electrónico de base de datos](../../relational-databases/database-mail/database-mail.md)   
 [Correo electrónico de base de datos objetos de configuración](../../relational-databases/database-mail/database-mail-configuration-objects.md)   
 [Creación de una cuenta de Correo electrónico de base de datos](../../relational-databases/database-mail/create-a-database-mail-account.md)   
 [Correo electrónico de base de datos procedimientos almacenados &#40;&#41;de Transact-SQL ](../../relational-databases/system-stored-procedures/database-mail-stored-procedures-transact-sql.md)  
  
  
