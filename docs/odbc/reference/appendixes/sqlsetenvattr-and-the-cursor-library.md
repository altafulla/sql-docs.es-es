---
description: SQLSetEnvAttr y la biblioteca de cursores
title: SQLSetEnvAttr y la biblioteca de cursores | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- SQLSetEnvAttr function [ODBC], Cursor Library
ms.assetid: 59cc8eae-09ae-4796-869a-c5806488ae83
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 97751c4735ed7357b87a3b50df5f116f7bb38c7d
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88476937"
---
# <a name="sqlsetenvattr-and-the-cursor-library"></a>SQLSetEnvAttr y la biblioteca de cursores
> [!IMPORTANT]  
>  Esta característica se quitará en una versión futura de Windows. Evite usar esta característica en los nuevos trabajos de desarrollo y planee modificar las aplicaciones que actualmente la utilizan. Microsoft recomienda el uso de la funcionalidad de cursor del controlador.  
  
 En este tema se describe el uso de la función **SQLSetEnvAttr** con la biblioteca de cursores. Para obtener información general sobre **SQLSetEnvAttr**, consulte la [función SQLSetEnvAttr](../../../odbc/reference/syntax/sqlsetenvattr-function.md).  
  
 La biblioteca de cursores no se ve afectada por la configuración del atributo de entorno SQL_ATTR_ODBC_VERSION, independientemente de la versión de la aplicación o de la versión del controlador.
