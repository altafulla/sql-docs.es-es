---
description: Propiedad FilterColumn (RDS)
title: FilterColumn (propiedad, RDS) | Microsoft Docs
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
apitype: COM
helpviewer_keywords:
- FilterColumn property [ADO]
ms.assetid: 0a5473e8-8ce6-4518-83fb-4920b827e285
author: rothja
ms.author: jroth
ms.openlocfilehash: f4fa38c64a353f6250bc400bf5ed7fc6bf46b95c
ms.sourcegitcommit: c7f40918dc3ecdb0ed2ef5c237a3996cb4cd268d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "91722232"
---
# <a name="filtercolumn-property-rds"></a>Propiedad FilterColumn (RDS)
Indica la columna en la que se van a evaluar los criterios de filtro.  
  
> [!IMPORTANT]
>  A partir de Windows 8 y Windows Server 2012, los componentes de servidor RDS ya no se incluyen en el sistema operativo Windows (consulte la guía de compatibilidad de Windows 8 y [Windows server 2012](https://www.microsoft.com/download/details.aspx?id=27416) para obtener más detalles). Los componentes de cliente RDS se quitarán en una versión futura de Windows. Evite utilizar esta característica en nuevos trabajos de desarrollo y tenga previsto modificar las aplicaciones que actualmente la utilizan. Las aplicaciones que utilizan RDS deben migrar al [servicio de datos de WCF](/dotnet/framework/wcf/).  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
DataControl.FilterColumn = String  
```  
  
#### <a name="parameters"></a>Parámetros  
 *DataControl*  
 Variable de objeto que representa un objeto [RDS. Objeto DataControl](./datacontrol-object-rds.md) .  
  
 *String*  
 Valor de **cadena** que especifica la columna en la que se van a evaluar los criterios de filtro. Los criterios de filtro se especifican en la propiedad [FilterCriterion](./filtercriterion-property-rds.md) .  
  
## <a name="remarks"></a>Observaciones  
 Las propiedades [SortColumn](./sortcolumn-property-rds.md), [SortDirection](./sortdirection-property-rds.md), [FilterValue](./filtervalue-property-rds.md), [FilterCriterion](./filtercriterion-property-rds.md)y **FilterColumn** proporcionan funcionalidad de ordenación y filtrado en la memoria caché del lado cliente. La funcionalidad de ordenación ordena los registros por los valores de una columna. La funcionalidad de filtrado muestra un subconjunto de registros basados en criterios de búsqueda, mientras que el [conjunto de registros](../ado-api/recordset-object-ado.md) completo se mantiene en la memoria caché. El método [RESET](./reset-method-rds.md) ejecutará los criterios y reemplazará el **conjunto de registros** actual por un **conjunto de registros**actualizable.  
  
## <a name="applies-to"></a>Se aplica a  
 [Objeto DataControl (RDS)](./datacontrol-object-rds.md)  
  
## <a name="see-also"></a>Consulte también  
 [Ejemplo de las propiedades FilterColumn, FilterCriterion, FilterValue, SortColumn y SortDirection y el método Reset (VBScript)](./filter-column-criterion-value-sortcolumn-sortdirection-example-vbscript.md)   
 [FilterCriterion (propiedad, RDS)](./filtercriterion-property-rds.md)   
 [Propiedad FilterValue (RDS)](./filtervalue-property-rds.md)   
 [Propiedad SortColumn (RDS)](./sortcolumn-property-rds.md)   
 [Propiedad SortDirection (RDS)](./sortdirection-property-rds.md)