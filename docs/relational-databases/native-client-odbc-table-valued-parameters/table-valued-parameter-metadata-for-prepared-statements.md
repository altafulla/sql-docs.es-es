---
description: Metadatos de parámetros con valores de tabla para instrucciones preparadas
title: Metadatos de TVP para instrucciones preparadas
ms.custom: ''
ms.date: 03/04/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: native-client
ms.topic: reference
helpviewer_keywords:
- table-valued parameters (ODBC), metadata for prepared statements
ms.assetid: fd2fc705-2e98-4011-9822-c7e6cca4a535
author: markingmyname
ms.author: maghan
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: c93614fa84a1758586deb72382dde042d40dd827
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88455891"
---
# <a name="table-valued-parameter-metadata-for-prepared-statements"></a>Metadatos de parámetros con valores de tabla para instrucciones preparadas
[!INCLUDE[SQL Server Azure SQL Database Synapse Analytics PDW ](../../includes/applies-to-version/sql-asdb-asdbmi-asa-pdw.md)]

  Una aplicación puede obtener metadatos para una llamada a procedimiento preparada a través de SQLNumParams y SQLDescribeParam. En el caso de los parámetros con valores de tabla, *DataTypePtr* se establece en SQL_SS_TABLE. Los metadatos adicionales están disponibles a través de SQLGetDescField para SQL_CA_SS_TYPE_NAME, SQL_CA_SS_CATALOG_NAME y SQL_CA_SS_SCHEMA_NAME.  
  
 SQL_CA_SS_TYPE_NAME, SQL_CA_SS_CATALOG_NAME y SQL_CA_SS_SCHEMA_NAME se pueden usar con SQLColumns para obtener los metadatos de columna para los tipos de tabla asociados a los parámetros con valores de tabla. En este caso, SQL_SOPT_SS_NAME_SCOPE debe establecerse en SQL_SS_NAME_SCOPE_TABLE_TYPE antes de que se llame a SQLColumns. A continuación, SQL_SOPT_SS_NAME_SCOPE se debe volver a establecer en el valor predeterminado, SQL_SS_NAME_SCOPE_TABLE, cuando la aplicación haya terminado de recuperar los metadatos de columnas de parámetros con valores de tabla.  
  
 SQL_CA_SS_TYPE_NAME, SQL_CA_SS_CATALOG_NAME y SQL_CA_SS_SCHEMA_NAME se pueden usar también con parámetros de tipos definidos por el usuario de CLR.  
  
 No puede obtener metadatos de parámetros con valores de tabla para instrucciones preparadas que no sean llamadas a procedimientos almacenados. Si lo intenta, la aplicación devuelve SQL_ERROR con SQLSTATE 42000 y el mensaje "error de sintaxis o infracción de acceso".  
  
## <a name="see-also"></a>Consulte también  
 [Parámetros con valores de tabla &#40;ODBC&#41;](../../relational-databases/native-client-odbc-table-valued-parameters/table-valued-parameters-odbc.md)  
  
  
