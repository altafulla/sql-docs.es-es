---
description: Permisos de hoja (Master Data Services)
title: Permisos de hoja
ms.custom: ''
ms.date: 03/15/2017
ms.prod: sql
ms.prod_service: mds
ms.reviewer: ''
ms.technology: master-data-services
ms.topic: conceptual
helpviewer_keywords:
- attribute groups [Master Data Services], permissions
- members [Master Data Services], leaf member permissions
- permissions [Master Data Services], leaf members
- leaf members [Master Data Services], attribute permissions
- attributes [Master Data Services], leaf member attribute permissions
ms.assetid: bde16e8c-bcd4-4041-8130-55c5450e5f72
author: lrtoyou1223
ms.author: lle
ms.openlocfilehash: a50723727690307492d3d16cb3671e762dec401f
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88461774"
---
# <a name="leaf-permissions-master-data-services"></a>Permisos de hoja (Master Data Services)

[!INCLUDE [SQL Server - Windows only ASDBMI  ](../includes/applies-to-version/sql-windows-only-asdbmi.md)]

  Los permisos de hoja se aplican a los valores de atributo de todos los miembros hoja de una entidad.  
  
 Para las entidades sin jerarquías explícitas habilitadas, la asignación de un permiso a **Hoja** es equivalente a asignar un permiso a la entidad.  
  
 **Notas:**  
  
-   Los permisos de hoja solo se aplican al área funcional del **Explorador** de la interfaz de usuario.  
  
-   Los permisos asignados a **Nombre** y a los atributos de **Código** no se aplican.  
  
|Permiso|Descripción|  
|----------------|-----------------|  
|**Lectura**|El usuario puede leer miembros hoja y atributos.|  
|**Crear**|Usuario puede crear miembros hoja y asignar valores de atributo durante la creación.|  
|**Actualizar**|El usuario puede actualizar miembros hoja y atributos.|  
|**Eliminar**|El usuario puede eliminar miembros hoja.|  
|**Deny**|Denegar todo el acceso a los miembros hoja.|  
  
 Los permisos de lectura, creación, actualización y eliminación se pueden combinar. Cuando se asignan Crear, Actualizar y Eliminar, el permiso de lectura se asigna automáticamente.  
  
## <a name="attribute-permissions"></a>Permisos de atributo  
 Los permisos de atributo se aplican a los valores del atributo para la entidad concreta. Los usuarios que tengan únicamente permisos de atributo no pueden agregar o quitar miembros.  
  
|Permiso|Descripción|  
|----------------|-----------------|  
|**Lectura**|El usuario puede leer atributos.|  
|**Crear**|El usuario puede asignar valores al crear miembros.|  
|**Actualizar**|El usuario puede actualizar atributos.|  
|**Eliminar**|Ningún efecto.|  
|**Deny**|No se muestra el atributo.<br /><br /> Nota: No puede denegar explícitamente el acceso a los atributos Name y Code.|  
  
### <a name="example"></a>Ejemplo  
 Para la entidad Product, asigne el permiso **Actualizar** al atributo Subcategory. Deniegue el permiso al resto de los atributos.  
  
|Nombre|Código|Subcategory (actualizar)|  
|----------|----------|----------------------------|  
|Mountain-100|BK-M101|{5} Bicicletas de montaña|  
|Mountain-100|BK-M201|{5} Bicicletas de montaña|  
  
 En el **Explorador**, puede actualizar cualquier valor de atributo en la columna Subcategory. Si no dispone del permiso para un atributo, este no se mostrará.  
  
> [!NOTE]  
>  En este ejemplo, Subcategory es un atributo basado en dominio, que depende de la entidad SubcategoryList. Puede seleccionar una subcategoría diferente para Mountain-100, pero no puede agregar o eliminar miembros en la entidad SubcategoryList.  
  
## <a name="see-also"></a>Consulte también  
 [Asignar permisos de objeto de modelo &#40;Master Data Services&#41;](../master-data-services/assign-model-object-permissions-master-data-services.md)   
    
 [Permisos del objeto de modelo &#40;Master Data Services&#41;](../master-data-services/model-object-permissions-master-data-services.md)   
 [Miembros &#40;Master Data Services&#41;](../master-data-services/members-master-data-services.md)   
 [Atributos &#40;Master Data Services&#41;](../master-data-services/attributes-master-data-services.md)  
  
  
