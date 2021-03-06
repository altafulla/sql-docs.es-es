---
description: Dígitos decimales
title: Dígitos decimales | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- size of data types [ODBC]
- decimal digits of data types [ODBC]
- data types [ODBC], decimal digits
- SQL data types [ODBC], column characteristics
ms.assetid: 07f3d1fc-b4ee-4693-b342-330b2231b6d0
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 0c56d0d4cdd4c40c2174085d80618bbcc58af14e
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88456622"
---
# <a name="decimal-digits"></a>Dígitos decimales
Los *dígitos decimales* de los tipos de datos decimal y NUMERIC se definen como el número máximo de dígitos a la derecha del separador decimal o la escala de los datos. En el caso de las columnas o los parámetros de número de punto flotante aproximado, la escala no está definida porque el número de dígitos a la derecha del separador decimal no es fijo. Para los datos de fecha y hora o de intervalo que contienen un componente de segundos, los dígitos decimales se definen como el número de dígitos a la derecha del separador decimal en el componente de segundos de los datos.  
  
 En el caso de los tipos de datos SQL_DECIMAL y SQL_NUMERIC, la escala máxima suele ser la misma que la precisión máxima. Sin embargo, algunos orígenes de datos imponen un límite independiente en la escala máxima. Para determinar las escalas mínima y máxima permitidas para un tipo de datos, una aplicación llama a **SQLGetTypeInfo**.  
  
 Los dígitos decimales definidos para cada tipo de datos conciso de SQL se muestran en la tabla siguiente.  
  
|Tipo SQL|Dígitos decimales|  
|--------------|--------------------|  
|Todos los tipos de caracteres y binarios [a]|N/D|  
|SQL_DECIMAL<br />SQL_NUMERIC|Número definido de dígitos a la derecha del separador decimal. Por ejemplo, la escala de una columna definida como numérica (10, 3) es 3. Puede ser un número negativo para admitir el almacenamiento de números muy grandes sin usar la notación exponencial. por ejemplo, "12000" podría almacenarse como "12" con una escala de-3.|  
|Todos los tipos numéricos exactos distintos de SQL_DECIMAL y SQL_NUMERIC [a]|0|  
|Todos los tipos de datos aproximados [a]|N/D|  
|SQL_TYPE_DATE y todos los tipos de intervalo sin componente de segundos [a]|N/D|  
|Todos los tipos DateTime excepto SQL_TYPE_DATE y todos los tipos de intervalo con un componente de segundos|Número de dígitos a la derecha del separador decimal en la parte de segundos del valor (fracciones de segundo). Este número no puede ser negativo.|  
|SQL_GUID|N/D|  
  
 [a] el argumento *ColumnSize* de **SQLBindParameter** se omite para este tipo de datos.  
  
 Los valores devueltos para los dígitos decimales no se corresponden con los valores de un campo de descriptor. Los valores pueden provienen del SQL_DESC_SCALE o del campo SQL_DESC_PRECISION, dependiendo del tipo de datos, como se muestra en la tabla siguiente.  
  
|Tipo SQL|Campo descriptor correspondiente a<br /><br /> dígitos decimales|  
|--------------|----------------------------------------------------------|  
|Todos los tipos de caracteres y binarios|N/D|  
|Todos los tipos numéricos exactos|SCALE|  
|SQL_BIT|N/D|  
|Todos los tipos numéricos aproximados|N/D|  
|Todos los tipos DateTime|PRECISION|  
|Todos los tipos de intervalo con un componente de segundos|PRECISION|  
|Todos los tipos de intervalo sin componente de segundos|N/D|
