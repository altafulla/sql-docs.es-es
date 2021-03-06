---
description: Clase SQLServerStatement
title: Clase SQLServerStatement | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
ms.assetid: ec24963c-8b51-4838-91e9-1fbfa2347451
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: c794edb2b0f2c62177b6591881c8886e36590bd4
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88462589"
---
# <a name="sqlserverstatement-class"></a>Clase SQLServerStatement
[!INCLUDE[Driver_JDBC_Download](../../../includes/driver_jdbc_download.md)]

  Representa la implementación básica de la funcionalidad de la instrucción de JDBC.  
  
 **Paquete:** com.microsoft.sqlserver.jdbc  
  
 **Implementa:** [ISQLServerStatement](../../../connect/jdbc/reference/isqlserverstatement-interface.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
public class SQLServerStatement  
```  
  
## <a name="remarks"></a>Observaciones  
 La clase SQLServerStatement también proporciona varios métodos de implementación de la clase base para la instrucción preparada e instrucciones invocables de JDBC. El rol básico de la clase SQLServerStatement es ejecutar las instrucciones SQL y, a continuación, devolver los conteos de actualizaciones y conjuntos de resultados a la aplicación del usuario.  
  
 Esta clase admite la desencapsulación en la clase SQLServerStatement, la interfaz ISQLServerStatement y la interfaz java.sql.Statement. Para más información, consulte [Contenedores e interfaces](../../../connect/jdbc/wrappers-and-interfaces.md).  
  
## <a name="see-also"></a>Consulte también  
 [Miembros SQLServerStatement](../../../connect/jdbc/reference/sqlserverstatement-members.md)   
 [Referencia de API del controlador JDBC](../../../connect/jdbc/reference/jdbc-driver-api-reference.md)  
  
  
