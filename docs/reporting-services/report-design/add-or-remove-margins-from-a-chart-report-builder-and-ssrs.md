---
title: Adición o eliminación de márgenes de un gráfico (Generador de informes) | Microsoft Docs
description: Agregue o quite los márgenes de un gráfico de columnas o de dispersión en el Generador de informes. Mejore la legibilidad o la apariencia de los informes paginados.
ms.date: 03/03/2017
ms.prod: reporting-services
ms.prod_service: reporting-services-native
ms.technology: report-design
ms.topic: conceptual
ms.assetid: 91c43f58-5771-4d33-a54d-0e802d2f5cba
author: maggiesMSFT
ms.author: maggies
ms.openlocfilehash: bbe5af103737cb9b4a5ba7e063f19b9cd6c1da41
ms.sourcegitcommit: fe59f8dc27fd633f5dfce54519d6f5dcea577f56
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2020
ms.locfileid: "91935363"
---
# <a name="add-or-remove-margins-from-a-chart-report-builder-and-ssrs"></a>Agregar o quitar márgenes de un gráfico (Generador de informes y SSRS)
Para los gráficos de columnas y de dispersión de los informes paginados de [!INCLUDE[ssRSnoversion](../../includes/ssrsnoversion-md.md)] , el gráfico agrega automáticamente márgenes laterales en los extremos del eje X. En los gráficos de barras, el gráfico agrega automáticamente márgenes laterales en los extremos del eje Y. En todos los demás tipos de gráficos, el gráfico no agrega márgenes laterales. No puede cambiar el tamaño del margen.  
  
 Este tema no se aplica a los tipos de gráficos circulares, de anillos, de embudo ni piramidales.  
  
> [!NOTE]  
>  [!INCLUDE[ssRBRDDup](../../includes/ssrbrddup-md.md)]  
  
## <a name="to-enable-or-disable-side-margins"></a>Habilitar o deshabilitar los márgenes laterales  
  
1.  Haga clic con el botón derecho en el eje y seleccione **Propiedades del eje**. Se abre el cuadro de diálogo **Propiedades del eje vertical** u **horizontal** .  
  
2.  En la página **Opciones del eje** , establezca la propiedad **Márgenes laterales** :  
  
    -   **Automático:** el gráfico determinará si se agrega un margen lateral basado en el tipo de gráfico.  
  
    -   **Deshabilitado:** los gráficos de barras, columna y dispersión no tendrán márgenes laterales.  
  
3.  [!INCLUDE[clickOK](../../includes/clickok-md.md)]  
  
## <a name="see-also"></a>Consulte también  
 [Aplicar formato a las etiquetas de los ejes de un gráfico &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/formatting-axis-labels-on-a-chart-report-builder-and-ssrs.md)   
 [Cuadro de diálogo Propiedades del eje, Opciones del eje &#40;Generador de informes y SSRS&#41;](/previous-versions/sql/)   
 [Especificar un intervalo de eje &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/specify-an-axis-interval-report-builder-and-ssrs.md)   
 [Aplicar formato de fecha o de moneda a las etiquetas de los ejes &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/format-axis-labels-as-dates-or-currencies-report-builder-and-ssrs.md)   
 [Gráficos &#40;Generador de informes y SSRS&#41;](../../reporting-services/report-design/charts-report-builder-and-ssrs.md)  
  
