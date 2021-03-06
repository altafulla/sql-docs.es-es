---
description: Sys. query_context_settings (Transact-SQL)
title: Sys. query_context_settings (Transact-SQL) | Microsoft Docs
ms.custom: ''
ms.date: 11/29/2018
ms.prod: sql
ms.prod_service: database-engine, sql-database
ms.reviewer: ''
ms.technology: system-objects
ms.topic: language-reference
f1_keywords:
- QUERY_CONTEXT_SETTINGS_TSQL
- SYS.QUERY_CONTEXT_SETTINGS_TSQL
- SYS.QUERY_CONTEXT_SETTINGS
- QUERY_CONTEXT_SETTINGS
dev_langs:
- TSQL
helpviewer_keywords:
- sys.query_context_settings catalog view
ms.assetid: 3c1887df-6bd8-491e-82fc-d25ad9589faf
author: markingmyname
ms.author: maghan
monikerRange: =azuresqldb-current||>=sql-server-2016||= azure-sqldw-latest||=sqlallproducts-allversions||>=sql-server-linux-2017||=azuresqldb-mi-current
ms.openlocfilehash: ce442458968fe21fc8ac84008bf33e823c2f3876
ms.sourcegitcommit: dd36d1cbe32cd5a65c6638e8f252b0bd8145e165
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89542503"
---
# <a name="sysquery_context_settings-transact-sql"></a>Sys. query_context_settings (Transact-SQL)
[!INCLUDE [sqlserver2016-asdb-asdbmi-asa](../../includes/applies-to-version/sqlserver2016-asdb-asdbmi-asa.md)]

  Contiene información sobre la semántica que afecta a la configuración de contexto asociada a una consulta. Hay una serie de valores de contexto disponibles en [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] que influyen en la semántica de la consulta (que define el resultado correcto de la consulta). El mismo texto de consulta compilado con distintos valores de configuración puede producir resultados diferentes (dependiendo de los datos subyacentes).  
  
|Nombre de la columna|Tipo de datos|Descripción|  
|-----------------|---------------|-----------------|  
|**context_settings_id**|**bigint**|Clave principal. Este valor se expone en SHOWPLAN XML for queries.|  
|**set_options**|**varbinary(8**|Máscara de bits que refleja el estado de varias opciones SET. Para obtener más información, vea [Sys. dm_exec_plan_attributes &#40;&#41;de Transact-SQL ](../../relational-databases/system-dynamic-management-views/sys-dm-exec-plan-attributes-transact-sql.md).|  
|**language_id**|**smallint**|Identificador del idioma. Para obtener más información, vea [ lenguajes desys.sys&#40;&#41;de Transact-SQL ](../../relational-databases/system-compatibility-views/sys-syslanguages-transact-sql.md).|  
|**date_format**|**smallint**|El formato de la fecha. Para más información, vea [SET DATEFORMAT &#40;Transact-SQL&#41;](../../t-sql/statements/set-dateformat-transact-sql.md).|  
|**date_first**|**tinyint**|El primer valor de fecha. Para más información, vea [SET DATEFIRST &#40;Transact-SQL&#41;](../../t-sql/statements/set-datefirst-transact-sql.md).|  
|**status**|**varbinary (2)**|Campo de máscara de máscara que indica el tipo de consulta o contexto en el que se ejecutó la consulta. <br />El valor de la columna puede ser una combinación de varias marcas (expresadas en hexadecimal):<br /><br /> 0X0: consulta normal (sin marcas específicas)<br /><br /> 0x1: consulta que se ejecutó a través de uno de los procedimientos almacenados de las API de cursor<br /><br /> 0X2: consulta de notificación<br /><br /> 0x4: consulta interna<br /><br /> 0x8: consulta parametrizada automática sin parametrización universal<br /><br /> 0x10-cursor fetch de la consulta de actualización<br /><br /> 0x20: consulta que se usa en las solicitudes de actualización de cursor<br /><br /> 0x40: se devuelve el conjunto de resultados inicial cuando se abre un cursor (captura automática de cursor)<br /><br /> 0x80: consulta cifrada<br /><br /> 0x100-Query en contexto del predicado de seguridad de nivel de fila|  
|**required_cursor_options**|**int**|Opciones de cursor especificadas por el usuario, como el tipo de cursor.|  
|**acceptable_cursor_options**|**int**|Opciones de cursor que [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] puede convertir de forma implícita para permitir la ejecución de la instrucción.|  
|**merge_action_type**|**smallint**|El tipo de plan de ejecución del desencadenador utilizado como resultado de una instrucción **Merge** .<br /><br /> 0 indica un plan que no es de desencadenador, un plan de desencadenadores que no se ejecuta como resultado de una instrucción **Merge** o un plan de desencadenador que se ejecuta como resultado de una instrucción **Merge** que solo especifica una acción de **eliminación** .<br /><br /> 1 indica un plan de desencadenador de **inserción** que se ejecuta como resultado de una instrucción **Merge** .<br /><br /> 2 indica un plan de desencadenador de **actualización** que se ejecuta como resultado de una instrucción **Merge** .<br /><br /> 3 indica un plan de desencadenador de **eliminación** que se ejecuta como resultado de una instrucción **Merge** que contiene una acción **Insert** o **Update** correspondiente.<br /><br /> <br /><br /> En el caso de los desencadenadores anidados ejecutados por acciones en cascada, este valor es la acción de la instrucción **Merge** que causó la cascada.|  
|**default_schema_id**|**int**|ID. del esquema predeterminado, que se utiliza para resolver nombres que no son completos.|  
|**is_replication_specific**|**bit**|Se usa para la replicación.|  
|**is_contained**|**varbinary (1)**|1 indica una base de datos independiente.|  
  
## <a name="permissions"></a>Permisos  
 Requiere el permiso **View Database State** .  
  
## <a name="see-also"></a>Consulte también  
 [Sys. database_query_store_options &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-database-query-store-options-transact-sql.md)   
 [Sys. query_store_plan &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-query-store-plan-transact-sql.md)   
 [Sys. query_store_query &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-query-store-query-transact-sql.md)   
 [Sys. query_store_query_text &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-query-store-query-text-transact-sql.md)   
 [Sys. query_store_runtime_stats &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-query-store-runtime-stats-transact-sql.md)   
 [Sys. query_store_wait_stats &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-query-store-wait-stats-transact-sql.md)   
 [Sys. query_store_runtime_stats_interval &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-query-store-runtime-stats-interval-transact-sql.md)   
 [Monitoring Performance By Using the Query Store](../../relational-databases/performance/monitoring-performance-by-using-the-query-store.md)   
 [Vistas de catálogo &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/catalog-views-transact-sql.md)   
 [Query Store Stored Procedures &#40;Transact-SQL&#41; (Procedimientos almacenados del Almacén de consultas &#40;Transact-SQL&#41;)](../../relational-databases/system-stored-procedures/query-store-stored-procedures-transact-sql.md)   
 [sys.fn_stmt_sql_handle_from_sql_stmt &#40;Transact-SQL&#41;](../../relational-databases/system-functions/sys-fn-stmt-sql-handle-from-sql-stmt-transact-sql.md)  
  
  
