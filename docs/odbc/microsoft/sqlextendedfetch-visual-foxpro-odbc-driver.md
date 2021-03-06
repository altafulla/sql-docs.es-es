---
description: SQLExtendedFetch (controlador ODBC de Visual FoxPro)
title: SQLExtendedFetch (controlador ODBC de Visual FoxPro) | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- SQLExtendedFetch function [ODBC], Visual FoxPro ODBC Driver
ms.assetid: b28af112-fb47-4143-b11e-3b743b2ae1b8
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 7f938dda4e9e474854d62c50401ee0bf91317983
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88449177"
---
# <a name="sqlextendedfetch-visual-foxpro-odbc-driver"></a>SQLExtendedFetch (controlador ODBC de Visual FoxPro)
> [!NOTE]  
>  Este tema contiene información específica del controlador ODBC de Visual FoxPro. Para obtener información general sobre esta función, vea el tema correspondiente en referencia de la [API de ODBC](../../odbc/reference/syntax/odbc-api-reference.md).  
  
 Compatibilidad: completa  
  
 Conformidad con la API de ODBC: nivel 2  
  
 Similar a [SQLFetch](../../odbc/microsoft/sqlfetch-visual-foxpro-odbc-driver.md) pero devuelve varias filas utilizando una matriz para cada columna. El conjunto de resultados es desplazable hacia delante y se puede desplazar hacia atrás si el cursor se define como estático, no solo hacia delante.  
  
 De forma predeterminada, el controlador ODBC de Visual FoxPro no devuelve las filas marcadas como eliminadas en una tabla de FoxPro. Las filas marcadas para su eliminación pero que todavía no se han quitado de una tabla no se incluyen en el cursor del conjunto de resultados. Puede cambiar este comportamiento mediante el comando [set Deleted](../../odbc/microsoft/set-deleted-command.md) .  
  
 Para obtener más información, vea [SQLExtendedFetch](../../odbc/reference/syntax/sqlextendedfetch-function.md) en la *Referencia del programador de ODBC*.
