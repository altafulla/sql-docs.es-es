---
title: Propiedades de SQL Server (página FILESTREAM) | Microsoft Docs
description: Familiarícese con la configuración de FILESTREAM en SQL Server. Obtenga información sobre cómo activar FILESTREAM y vea cómo configurar el acceso de cliente remoto y otras propiedades.
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: high-availability
ms.reviewer: ''
ms.technology: configuration
ms.topic: conceptual
f1_keywords:
- sql13.swb.serverproperties.filestream.f1
helpviewer_keywords:
- FILESTREAM [SQL Server], properties page
ms.assetid: 8a8d38d3-e97a-4b09-a40b-659b2e3a5c47
author: markingmyname
ms.author: maghan
ms.openlocfilehash: 81edbd9bfc913f9d339625a993f866d44e1a313b
ms.sourcegitcommit: da88320c474c1c9124574f90d549c50ee3387b4c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "85730931"
---
# <a name="server-properties---filestream-page"></a>Propiedades del servidor (página FILESTREAM)
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  Utilice esta página para habilitar FILESTREAM para esta instalación de [!INCLUDE[ssCurrent](../../includes/sscurrent-md.md)].  
  
## <a name="ui-element-list"></a>Lista de elementos de la interfaz de usuario  
 **Habilitar FILESTREAM para acceso Transact-SQL**  
 Seleccione esta opción para habilitar FILESTREAM para el acceso a [!INCLUDE[tsql](../../includes/tsql-md.md)] . Este control debe comprobarse para que las otras opciones de control estén disponibles.  
  
 **Habilitar FILESTREAM para el acceso de transmisión por secuencias de E/S de archivos**  
 Seleccione esta opción para habilitar el acceso de transmisión por secuencias de Win32 para FILESTREAM.  
  
 **Nombre de recurso compartido de Windows**  
 Utilice este control para escribir el nombre del recurso compartido de Windows en el que los datos de FILESTREAM se almacenarán.  
  
 **Permitir que los clientes remotos tengan acceso de transmisión por secuencias a los datos de FILESTREAM**  
 Seleccione este control para permitir que los clientes remotos tengan acceso a estos datos de FILESTREAM en este servidor.  
  
## <a name="see-also"></a>Consulte también  
 [FILESTREAM &#40;SQL Server&#41;](../../relational-databases/blob/filestream-sql-server.md)   
 [sp_configure &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/sp-configure-transact-sql.md)  
  
  
