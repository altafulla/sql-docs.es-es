---
description: Creación de archivos de valor variable (OracleToSQL)
title: Crear archivos de valor variable (OracleToSQL) | Microsoft Docs
ms.prod: sql
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.technology: ssma
ms.topic: conceptual
helpviewer_keywords:
- Variable Value File Creation
- Variable Value File, Variable Value File Validation
ms.assetid: f583d81a-8e34-41b1-8100-ee3a6a82213b
author: nahk-ivanov
ms.author: alexiva
manager: alexiva
ms.openlocfilehash: b97455172dbed11a8d29168946decca7b3b919e4
ms.sourcegitcommit: 22dacedeb6e8721e7cdb6279a946d4002cfb5da3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "92039209"
---
# <a name="creating-variable-value-files-oracletosql"></a>Creación de archivos de valor variable (OracleToSQL)
El archivo de valores de variable es un archivo XML que comprende los valores de parámetro de comandos como, el nombre de servidor de origen o de destino que cambian con frecuencia de una migración de servidor a otra. Cuando se produce un gran número de migraciones de base de datos, se crearán varios archivos de variables para almacenar el valor de cada servidor de origen y se hará referencia a ellos en un archivo de script maestro con el modificador **-v** en la línea de comandos. Esto ayuda a mantener valores estáticos en algunos archivos de script con los valores de variable en varios archivos de variables.  
  
> [!NOTE]  
> 1.  Los nombres de variable tienen el prefijo y el sufijo con un símbolo $ (dólar). Si no se asigna un valor a las variables en el archivo de valores de variable, se producirá un error durante el análisis del archivo de script, lo que provocará que se detenga el proceso de ejecución de la consola.  
> 2.  El carácter de escape para **$** es **$$** . Si el valor de una variable o un valor estático de un parámetro contiene un **$** símbolo (dólar), **$$** debe especificarse para tratarlo como un carácter en lugar de una variable.  
> 3.  En lo que respecta a la facilidad de mantenimiento, las variables se pueden declarar dentro de `'variable-group'` elementos para la separación lógica de las variables definidas por el usuario.  El uso de este elemento no es obligatorio.  
  
**Ejemplos:**  
  
**Ejemplo 1:**  
  
```  
<!--Sample of variable value file commands-->  
  
<variables>  
  
  <variable-group name="ProjectSpecs">  
  
    <variable name="$project_folder$" value="<project-folder>"/>  
  
    <variable name="$project_name$" value="<project-name>"/>  
  
    <variable name="$project_overwrite$" value="<true/false>"/>  
  
    <variable name="$project_type$" value="<project-type>"/>  
  
  </variable-group>  
  
</variables>  
```  
**Ejemplo 2:**  
  
```  
<!--Sample of variable value file commands-->  
  
<variables>  
  
  <variable-group name="SQLServerParams">  
  
    <variable-group name="SqlServerConnectionParams">  
  
      <variable name="$TargetServerName$" value="<server-name>"/>  
  
      <variable name="$TargetDB$" value="<database-name>"/>  
  
      <variable name="$TargetUserName$" value="<user-name>"/>  
  
      <variable name="$TargetPassword$" value="<password>"/>  
  
      <variable name="$TrustedConnection$" value="<true/false>"/>  
  
    </variable-group>  
  
    <variable-group name="SqlServerObjectParams">  
  
      <variable name="$ObjectName1$" value="<object-name>"/>  
  
      <variable name="$ObjectName2$" value="<object-name>"/>  
  
    </variable-group>  
  
  </variable-group>  
  
</variables>  
```  
  
## <a name="next-step"></a>siguiente paso  
El siguiente paso en el funcionamiento de la consola es [la creación de los archivos de conexión del servidor &#40;OracleToSQL&#41;](../../ssma/oracle/creating-the-server-connection-files-oracletosql.md)  
  
## <a name="see-also"></a>Consulte también  
[Crear los archivos de servidor (Oracle)](./creating-the-server-connection-files-oracletosql.md)  
