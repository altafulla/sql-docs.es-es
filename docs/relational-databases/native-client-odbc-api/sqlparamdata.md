---
description: SQLParamData
title: SQLParamData | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: native-client
ms.topic: reference
helpviewer_keywords:
- SQLParamData function
ms.assetid: 92349482-ea22-4a6a-8484-e9c6566794fa
author: markingmyname
ms.author: maghan
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: af2f9651ad0bc8986df1c688e4d94084ddeac0df
ms.sourcegitcommit: 04cf7905fa32e0a9a44575a6f9641d9a2e5ac0f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/07/2020
ms.locfileid: "91810937"
---
# <a name="sqlparamdata"></a>SQLParamData
[!INCLUDE[SQL Server Azure SQL Database Synapse Analytics PDW ](../../includes/applies-to-version/sql-asdb-asdbmi-asa-pdw.md)]

  Cuando SQLParamData devuelve el *ValuePtrPtr* asociado a un parámetro con valores de tabla, la aplicación debe llamar a SQLPutData con *StrLen_Or_Ind*. Si *StrLen_Or_Ind* tiene un valor mayor que 0, significa que la aplicación está lista para que [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Native Client recopile los datos de parámetro para la siguiente fila de parámetro con valores de tabla. Si *StrLen_Or_Ind* tiene un valor de 0, significa que no hay más filas de datos para el parámetro con valores de tabla. Para obtener más información, vea [enlazar y transferencia de datos de parámetros con valores de tabla y valores de columna](../../relational-databases/native-client-odbc-table-valued-parameters/binding-and-data-transfer-of-table-valued-parameters-and-column-values.md).  
  
 Para obtener más información sobre los parámetros con valores de tabla, vea [parámetros con valores de tabla &#40;ODBC&#41;](../../relational-databases/native-client-odbc-table-valued-parameters/table-valued-parameters-odbc.md).  
  
## <a name="see-also"></a>Consulte también  
 [SQLParamData](../../odbc/reference/syntax/sqlparamdata-function.md)   
 [ODBC API Implementation Details](../../relational-databases/native-client-odbc-api/odbc-api-implementation-details.md)  
  
