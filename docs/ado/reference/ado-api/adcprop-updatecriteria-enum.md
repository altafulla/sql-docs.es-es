---
description: ADCPROP_UPDATECRITERIA_ENUM
title: ADCPROP_UPDATECRITERIA_ENUM | Microsoft Docs
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
apitype: COM
f1_keywords:
- ADCPROP_UPDATECRITERIA_ENUM
helpviewer_keywords:
- ADCPROP_UPDATECRITERIA_ENUM [ADO]
ms.assetid: 33fd7b65-2ec8-4f62-91a7-630b5dab1aa2
author: rothja
ms.author: jroth
ms.openlocfilehash: 3711266f3658fe2366caa56c6afba07d6b63c4c9
ms.sourcegitcommit: 18a98ea6a30d448aa6195e10ea2413be7e837e94
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "88976816"
---
# <a name="adcprop_updatecriteria_enum"></a>ADCPROP_UPDATECRITERIA_ENUM
Especifica los campos que se pueden utilizar para detectar conflictos durante una actualización optimista de una fila del origen de datos con un objeto de [conjunto de registros](./recordset-object-ado.md) .  
  
 Use estas constantes con la propiedad dinámica "**criterios de actualización**" del **conjunto de registros** , a la que se hace referencia en el [Índice de propiedades dinámicas de ADO](./ado-dynamic-property-index.md) y que se documenta en la documentación del [servicio de cursor de Microsoft para OLE DB](../../guide/appendixes/microsoft-cursor-service-for-ole-db-ado-service-component.md) .  
  
|Constante|Valor|Descripción|  
|--------------|-----------|-----------------|  
|**adCriteriaAllCols**|1|Detecta conflictos si se ha cambiado alguna columna de la fila del origen de datos.|  
|**adCriteriaKey**|0|Detecta conflictos si la columna de clave de la fila de origen de datos ha cambiado, lo que significa que se ha eliminado la fila.|  
|**adCriteriaTimeStamp**|3|Detecta conflictos si la marca de tiempo de la fila de origen de datos ha cambiado, lo que significa que se ha tenido acceso a la fila después de obtener el **conjunto de registros** .|  
|**adCriteriaUpdCols**|2|Detecta conflictos si se ha cambiado alguna de las columnas de la fila del origen de datos que corresponden a los campos actualizados del **conjunto de registros** .|  
  
## <a name="adowfc-equivalent"></a>Equivalente de ADO/WFC  
 Paquete: **com. ms. wfc. Data**  
  
|Constante|  
|--------------|  
|AdoEnums. AdcPropUpdateCriteria. ALLCOLS|  
|AdoEnums.AdcPropUpdateCriteria.KEY|  
|AdoEnums. AdcPropUpdateCriteria. TIMESTAMP|  
|AdoEnums. AdcPropUpdateCriteria. UPDCOLS|