---
description: IndexNulls (propiedad, ADOX)
title: IndexNulls (propiedad, ADOX) | Microsoft Docs
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
apitype: COM
f1_keywords:
- _Index::get_IndexNulls
- _Index::GetIndexNulls
- _Index::put_IndexNulls
- _Index::PutIndexNulls
- _Index::IndexNulls
helpviewer_keywords:
- IndexNulls property [ADOX]
ms.assetid: 313b0bf7-3f37-4823-8fca-bd9c80e078a7
author: rothja
ms.author: jroth
ms.openlocfilehash: 055b873866758c4aede2a3f6364eb99036159427
ms.sourcegitcommit: 18a98ea6a30d448aa6195e10ea2413be7e837e94
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "88984156"
---
# <a name="indexnulls-property-adox"></a>IndexNulls (propiedad, ADOX)
Indica si los registros que tienen valores NULL en sus campos de índice tienen entradas de índice.  
  
## <a name="settings-and-return-values"></a>Configuración y valores devueltos  
 Establece y devuelve un valor de [AllowNullsEnum](./allownullsenum.md) . El valor predeterminado es **adIndexNullsDisallow**.  
  
## <a name="remarks"></a>Observaciones  
 Esta propiedad es de solo lectura en los objetos de [Índice](./index-object-adox.md) ya anexados a una colección.  
  
## <a name="applies-to"></a>Se aplica a  
 [Objeto Index (ADOX)](./index-object-adox.md)  
  
## <a name="see-also"></a>Consulte también  
 [Ejemplo de propiedad IndexNulls (VB)](./indexnulls-property-example-vb.md)