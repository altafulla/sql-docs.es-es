---
description: IsNull (tipo de datos geometry)
title: IsNull (tipo de datos geometry) | Microsoft Docs
ms.custom: ''
ms.date: 09/12/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: t-sql
ms.topic: language-reference
f1_keywords:
- IsNull (geometry Data Type)
dev_langs:
- TSQL
helpviewer_keywords:
- IsNull (geometry Data Type)
ms.assetid: f95813a5-26c0-48aa-bfb8-56d2a0980788
author: MladjoA
ms.author: mlandzic
ms.openlocfilehash: 02e8775089f6e8112452ff2a0ff780bc9a848f31
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88497061"
---
# <a name="isnull-geometry-data-type"></a>IsNull (tipo de datos geometry)
[!INCLUDE [SQL Server SQL Database](../../includes/applies-to-version/sql-asdb.md)]

El tipo de una instancia de **geometry** es NULL. Devuelve 0 si la instancia no es NULL.
  
## <a name="syntax"></a>Sintaxis  
  
```  
.IsNull  
```  
  
[!INCLUDE[sql-server-tsql-previous-offline-documentation](../../includes/sql-server-tsql-previous-offline-documentation.md)]

## <a name="return-types"></a>Tipos de valor devuelto
 Tipo de [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)]: **bit**  
  
 Tipo de CLR: **SqlBoolean**  
  
## <a name="remarks"></a>Observaciones  
 `IsNull` se puede usar para comprobar si una instancia de **geometry** es NULL. `IsNull` devuelve 0 si la instancia no es NULL; en caso contrario, devuelve NULL.  
  
 Este método lo usa principalmente la infraestructura de SQL Server; no es recomendable usar `IsNull` para comprobar si una instancia es NULL.  
  

## <a name="see-also"></a>Consulte también  
 [Métodos extendidos en instancias de geometry](../../t-sql/spatial-geometry/extended-methods-on-geometry-instances.md)  
  
  

