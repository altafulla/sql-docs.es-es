---
title: Extensión de servidores de Administración Central de SQL Server
titleSuffix: Azure Data Studio
description: Instalar y usar la extensión de servidores de Administración Central de SQL Server (versión preliminar) para Azure Data Studio
ms.custom: seodec18
ms.date: 06/06/2019
ms.reviewer: alayu; sstein
ms.prod: sql
ms.technology: azure-data-studio
ms.topic: conceptual
author: yualan
ms.author: alayu
manager: jroth
ms.openlocfilehash: 743bf6f78fa84f628a20bed23af0ace8cf23d06f
ms.sourcegitcommit: ad2e98972a0e739c0fd2038ef4a030265f0ee788
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/07/2019
ms.locfileid: "66798022"
---
# <a name="sql-server-central-management-servers-extension-preview"></a>Extensión de servidores de Administración Central de SQL Server (versión preliminar)
La extensión de servidores de Administración Central permite a los usuarios almacenar una lista de instancias de SQL Server que se organizan en uno o varios grupos. Las acciones que se realizan mediante un grupo CMS actúan en todos los servidores del grupo de servidores.

Esta experiencia está actualmente en su versión preliminar inicial. Notificar problemas y solicitudes de características [aquí](https://github.com/microsoft/azuredatastudio/issues).

![Extensión CMS](media/sql-server-cms-extension/cms-list.png)

## <a name="install-the-sql-server-central-management-servers-extension"></a>Instalar la extensión de servidores de Administración Central de SQL Server

1. Para abrir el Administrador de extensiones y tener acceso a las extensiones disponibles, seleccione el icono de extensiones o **extensiones** en el **vista** menú.
2. Seleccione una extensión disponible para ver sus detalles.
1. Seleccione la extensión que desee (SQL Server servidores de Administración Central) y **instalar** lo.

### <a name="how-do-i-start-central-management-servers"></a>¿Cómo se pueden iniciar los servidores de Administración Central?
 Servidores de administración central pueden verse haciendo clic en el icono de conexiones (Cmd/Ctrl + G). La primera vez que descargue la extensión, se minimizará la vista CMS, y puede abrir haciendo clic en **servidores de Administración Central**

## <a name="next-steps"></a>Pasos siguientes
Para obtener información sobre conceptos sobre servidores de Administración Central, [puede leer más información aquí.](https://docs.microsoft.com/sql/ssms/register-servers/create-a-central-management-server-and-server-group)

