---
description: SQLNativeSql (biblioteca de cursores)
title: SQLNativeSql (biblioteca de cursores) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- SQLNativeSql function [ODBC], Cursor Library
ms.assetid: c4459092-1177-4b2a-b7f5-e0083d3bf2b2
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 6046c8dabbc128a3afae772730cbad9eacc4b61c
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88424916"
---
# <a name="sqlnativesql-cursor-library"></a>SQLNativeSql (biblioteca de cursores)
> [!IMPORTANT]  
>  Esta característica se quitará en una versión futura de Windows. Evite usar esta característica en los nuevos trabajos de desarrollo y planee modificar las aplicaciones que actualmente la utilizan. Microsoft recomienda el uso de la funcionalidad de cursor del controlador.  
  
 En este tema se describe el uso de la función **SQLNativeSql** en la biblioteca de cursores. Para obtener información general sobre **SQLNativeSql**, consulte la [función SQLNativeSql](../../../odbc/reference/syntax/sqlnativesql-function.md).  
  
 Si el controlador admite esta función, la biblioteca de cursores llama a **SQLNativeSql** en el controlador y la pasa a la instrucción SQL. Para la actualización posicionada, la eliminación posicionada y la **selección de instrucciones Update** , la biblioteca de cursores modifica la instrucción antes de pasarla al controlador.  
  
> [!NOTE]  
>  La biblioteca de cursores devuelve incorrectamente SQLSTATE 34000 (nombre de cursor no válido) si el nombre del cursor no es válido en una instrucción UPDATE o DELETE posicionada que se pasa en el argumento *InStatementText* de **SQLNativeSql**. **SQLNativeSql** no está pensado para devolver errores de sintaxis, que solo se devuelven tras la preparación o ejecución de la instrucción.
