---
description: Secuencias de escape GUID
title: Secuencias de escape de GUID | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- ODBC escape sequences [ODBC], GUID
- escape sequences [ODBC], guid
- guid escape sequence [ODBC]
ms.assetid: 71d43ef9-4a31-493e-b9e0-f864e9ef3ce6
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: d7babe2d26c0e5f2b311f8df5bbd1763622f3042
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88466161"
---
# <a name="guid-escape-sequences"></a>Secuencias de escape GUID
ODBC utiliza secuencias de escape para literales de GUID. La sintaxis de esta secuencia de escape es la siguiente:  
  
```  
{guid 'nnnnnnnn-nnnn-nnnn-nnnn-nnnnnnnnnnnn'}  
```  
  
## <a name="remarks"></a>Observaciones  
 En la notación BNF, la sintaxis es la siguiente:  
  
 *ODBC-GUID-escape* :: =  
     *ODBC-ESC-GUID del iniciador* '*GUID-valor*' *ODBC-ESC-Terminator*  
  
 *ODBC-ESC-Initiator* :: = {  
  
 *ODBC-ESC-Terminator* :: =}  
  
 *GUID-valor* :: = *reloj-bajo-valor GUID-separador-punto-medio-valor GUID-* separador-valor-de-número-número-valor-valor-valor  
  
 *GUID-separador* :: =-  
  
 *Clock-Low-Value* :: = *hex_digit hex_digit hex_digit hex_digit hex_digit* hex_digit hex_digit hex_digit  
  
 *Clock-Middle-Value* :: = *hex_digit hex_digit hex_digit hex_digit*  
  
 *Clock-High-value* :: = *hex_digit hex_digit hex_digit hex_digit*  
  
 *Clock-SEQ-Value* :: = *hex_digit hex_digit hex_digit hex_digit*  
  
 *Clock-node-Value* :: = *hex_digit hex_digit hex_digit hex_digit hex_digit hex_digit* hex_digit hex_digit hex_digit hex_digit hex_digit hex_digit  
  
 *hex_digit* :: = 0 &#124; 1 &#124; 2 &#124; 3 &#124; 4 &#124; 5 &#124; 6 &#124; 7 &#124; 8 &#124; 9 &#124; A &#124; B &#124; C &#124; D &#124; E &#124; F  
  
 La secuencia de escape literal de GUID se admite si el tipo de datos de GUID es compatible con el origen de datos. Una aplicación debe llamar a **SQLGetTypeInfo** para determinar si se admite este tipo de datos.
