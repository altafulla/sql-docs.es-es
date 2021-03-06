---
description: Programa de administración
title: Programa de administración | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- administration program [ODBC]
- ODBC administrator [ODBC]
ms.assetid: a6c8248a-7a01-42e7-aaed-99dc94d50028
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 5aef5e00fa69fd1f699228b2c0ac82b2a8041962
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88429037"
---
# <a name="administration-program"></a>Programa de administración
> [!NOTE]  
>  A partir de Windows XP y Windows Server 2003, ODBC se incluye en el sistema operativo Windows. Solo debe instalar explícitamente ODBC en versiones anteriores de Windows.  
  
 Un programa de administración, el administrador de ODBC, se incluye con el SDK de Windows SDK/MDAC. Este programa y puede ser redistribuido por los usuarios del SDK. Además, los programadores pueden escribir sus propios programas de administración. Por lo general, los desarrolladores escriben sus propios programas de administración únicamente si desean conservar el control completo sobre la configuración del origen de datos o si están configurando orígenes de datos directamente desde una aplicación que actúa como programa de administración. Por ejemplo, un programa de hoja de cálculo puede permitir que los usuarios agreguen y usen orígenes de datos en tiempo de ejecución.  
  
 El programa de Administración carga primero la DLL del instalador. A continuación, llama a las funciones del archivo DLL del instalador para realizar las siguientes tareas:  
  
-   **Agregar, modificar o eliminar orígenes de datos de forma interactiva.** El programa de administración puede llamar a **SQLManageDataSources**, **SQLCreateDataSource**o **SQLConfigDataSource**.  
  
     **SQLManageDataSources** muestra un cuadro de diálogo con el que el usuario puede Agregar, modificar o eliminar orígenes de datos y especificar opciones de seguimiento. se llama a esta función cuando la DLL del instalador se invoca directamente desde el panel de control. **SQLCreateDataSource** muestra un cuadro de diálogo con el que el usuario solo puede Agregar orígenes de datos. **SQLConfigDataSource** pasa la llamada directamente al archivo dll de instalación del controlador.  
  
     En todos los casos, la DLL del instalador llama a **ConfigDSN** en el archivo dll de instalación del controlador para agregar, modificar o eliminar el origen de datos. Es posible que el archivo DLL de instalación del controlador solicite información adicional al usuario.  
  
-   **Agregar, modificar o eliminar orígenes de datos de forma silenciosa.** El programa de administración llama a **SQLConfigDataSource** en el archivo DLL del instalador y le pasa un identificador de ventana nulo, el nombre de un origen de datos que se va a agregar, modificar o eliminar, y una lista de valores para el registro. La DLL del instalador llama a **ConfigDSN** en el archivo dll de instalación del controlador para agregar, modificar o eliminar el origen de datos.  
  
-   **Agregar, modificar o eliminar un origen de datos predeterminado.** El origen de datos predeterminado es el mismo que cualquier otro origen de datos, con la excepción de que su nombre es predeterminado. Se agrega, modifica o elimina de la misma manera que cualquier otro origen de datos.
