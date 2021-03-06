---
description: Limitaciones del tipo de datos
title: Limitaciones de los tipos de datos | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- ODBC desktop database drivers [ODBC], data types
- data types [ODBC], desktop database drivers
- desktop database drivers [ODBC], data types
ms.assetid: 81c4eab7-1f6b-47a0-b940-89d6c6a14dae
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 4853846f21aa0ad763295bbdc4233c472ac53864
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88412791"
---
# <a name="data-type-limitations"></a>Limitaciones del tipo de datos
Los controladores de base de datos de Microsoft ODBC Desktop imponen las siguientes limitaciones en los tipos de datos:  
  
|Tipo de datos|Descripción|  
|---------------|-----------------|  
|Todos los tipos de datos|Los errores de conversión de tipos pueden dar lugar a que la columna afectada se establezca en NULL.|  
|BINARY|Al crear una columna BINARIa de longitud cero, se devuelve realmente una columna BINARIa de 255 bytes.|  
|DATE|El tipo de datos DATE no se puede convertir en otro tipo de datos (o en sí mismo) mediante la función CONVERT.|  
|DECIMAL (numérico exacto)|No compatible.|  
|Tipos de datos de punto flotante|El número de posiciones decimales en un número de punto flotante puede estar limitado por el formato de número establecido en la sección internacional del panel de control de Windows.|  
|NUMERIC|Admite la precisión máxima y una escala de 28.|  
|timestamp|La función CONVERT no puede convertir el tipo de datos TIMESTAMP en sí mismo.|  
|TINYINT|Los valores TINYINT siempre están sin signo.|  
|Cadenas de longitud cero|Cuando se usa dBASE, Microsoft Excel, Paradox o Textdriver, al insertar una cadena de longitud cero en una columna se inserta realmente un valor NULL.|
