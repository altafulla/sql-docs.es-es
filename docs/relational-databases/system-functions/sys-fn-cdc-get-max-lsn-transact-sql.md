---
description: sys.fn_cdc_get_max_lsn (Transact-SQL)
title: Sys. fn_cdc_get_max_lsn (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- sys.fn_cdc_get_max_lsn
- fn_cdc_get_max_lsn
- fn_cdc_get_max_lsn_TSQL
- sys.fn_cdc_get_max_lsn_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- fn_cdc_get_max_lsn
- sys.fn_cdc_get_max_lsn
ms.assetid: 93f3a4c8-b91f-4ebb-8e96-9397bb3a1c43
author: rothja
ms.author: jroth
ms.openlocfilehash: 314fac004523b27d5766cca264535dcca6dd058e
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88322141"
---
# <a name="sysfn_cdc_get_max_lsn-transact-sql"></a>sys.fn_cdc_get_max_lsn (Transact-SQL)
[!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

  Devuelve el número de secuencia de registro máximo (LSN) de la start_lsn columna de la tabla del sistema [CDC. lsn_time_mapping](../../relational-databases/system-tables/cdc-lsn-time-mapping-transact-sql.md) . Puede utilizar esta función para devolver el extremo alto de la escala de tiempo de captura de los datos del cambio para cualquier instancia de captura.  
  
 ![Icono de vínculo de tema](../../database-engine/configure-windows/media/topic-link.gif "Icono de vínculo de tema") [Convenciones de sintaxis de Transact-SQL](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
sys.fn_cdc_get_max_lsn ()  
```  
  
## <a name="return-types"></a>Tipos de valor devuelto  
 **binary(10)**  
  
## <a name="remarks"></a>Observaciones  
 Esta función devuelve el LSN máximo en la start_lsn columna de la tabla [CDC. lsn_time_mapping](../../relational-databases/system-tables/cdc-lsn-time-mapping-transact-sql.md) . Por tanto, es el último LSN procesado por el proceso de captura cuando los cambios se propagan a las tablas de cambios de base de datos. Actúa como extremo superior para todas las escalas de tiempo asociadas con las instancias de captura definidas para la base de datos.  
  
 La función se utiliza normalmente para obtener un extremo final superior adecuado para un intervalo de consulta.  
  
## <a name="permissions"></a>Permisos  
 Debe pertenecer al rol de base de datos public.  
  
## <a name="examples"></a>Ejemplos  
  
### <a name="a-returning-the-maximum-lsn-value"></a>A. Devolver el valor LSN máximo  
 El ejemplo siguiente devuelve el LSN máximo para todas las instancias de captura en la base de datos [!INCLUDE[ssSampleDBnormal](../../includes/sssampledbnormal-md.md)].  
  
```  
USE AdventureWorks2012;  
GO  
SELECT sys.fn_cdc_get_max_lsn()AS max_lsn;  
```  
  
### <a name="b-setting-the-high-endpoint-of-a-query-range"></a>B. Establecer el extremo alto de un rango de la consulta  
 El ejemplo siguiente utiliza el LSN máximo devuelto por `sys.fn_cdc_get_max_lsn` para establecer el extremo alto para un intervalo de consultas para la instancia de captura `HumanResources_Employee`.  
  
```  
USE AdventureWorks2012;  
GO  
DECLARE @from_lsn binary(10), @to_lsn binary(10);  
SET @from_lsn = sys.fn_cdc_get_min_lsn(N'HumanResources_Employee');  
SET @to_lsn = sys.fn_cdc_get_max_lsn();  
SELECT * FROM cdc.fn_cdc_get_all_changes_HumanResources_Employee(@from_lsn, @to_lsn, 'all');  
GO  
```  
  
## <a name="see-also"></a>Consulte también  
 [Sys. fn_cdc_get_min_lsn &#40;Transact-SQL&#41;](../../relational-databases/system-functions/sys-fn-cdc-get-min-lsn-transact-sql.md)   
 [El registro de transacciones &#40;SQL Server&#41;](../../relational-databases/logs/the-transaction-log-sql-server.md)  
  
  
