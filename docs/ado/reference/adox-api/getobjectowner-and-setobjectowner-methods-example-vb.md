---
description: Ejemplo de métodos GetObjectOwner y SetObjectOwner (VB)
title: Ejemplo de los métodos GetObjectOwner y SetObjectOwner (VB) | Microsoft Docs
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
dev_langs:
- VB
helpviewer_keywords:
- SetObjectOwner method [ADOX], Visual Basic example
- GetObjectOwner method [ADOX], Visual Basic example
ms.assetid: e44ec3d4-42ae-447d-aaed-bdea53cb0cca
author: rothja
ms.author: jroth
ms.openlocfilehash: 6b3033c06d7853768069b20493494e128991abff
ms.sourcegitcommit: 18a98ea6a30d448aa6195e10ea2413be7e837e94
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2020
ms.locfileid: "88984576"
---
# <a name="getobjectowner-and-setobjectowner-methods-example-vb"></a>Ejemplo de métodos GetObjectOwner y SetObjectOwner (VB)
En este ejemplo se muestran los métodos [GetObjectOwner](./getobjectowner-method-adox.md) y [SetObjectOwner](./setobjectowner-method.md) . Este código supone la existencia de la cuenta de grupo (vea el ejemplo de los [métodos Append y ChangePassword de grupos y usuarios (VB)](./groups-and-users-append-changepassword-methods-example-vb.md) para ver cómo agregar este grupo al sistema). El propietario de la tabla Categories está establecido en Accounting.  
  
```  
' BeginOwnersVB  
Sub OwnersX()  
  
    Dim tblLoop As New ADOX.Table  
    Dim cat As New ADOX.Catalog  
    Dim strOwner As String  
  
    ' Open the Catalog.  
    cat.ActiveConnection = "Provider=Microsoft.Jet.OLEDB.4.0;" & _  
        "Data Source=c:\Program Files\" & _  
        "Microsoft Office\Office\Samples\Northwind.mdb;" & _  
        "jet oledb:system database=" & _  
        "c:\Program Files\Microsoft Office\Office\system.mdw"  
  
    ' Print the original owner of Categories  
    strOwner = cat.GetObjectOwner("Categories", adPermObjTable)  
    Debug.Print "Owner of Categories: " & strOwner  
  
    ' Set the owner of Categories to Accounting  
    cat.SetObjectOwner "Categories", adPermObjTable, "Accounting"  
  
    ' List the owners of all tables and columns in the catalog.  
    For Each tblLoop In cat.Tables  
        Debug.Print "Table: " & tblLoop.Name  
        Debug.Print "   Owner: " & _  
            cat.GetObjectOwner(tblLoop.Name, adPermObjTable)  
    Next tblLoop  
  
    ' Restore the original owner of Categories  
    cat.SetObjectOwner "Categories", adPermObjTable, strOwner  
  
End Sub  
' EndOwnersVB  
```  
  
## <a name="see-also"></a>Consulte también  
 [Objeto Catalog (ADOX)](./catalog-object-adox.md)   
 [Método GetObjectOwner (ADOX)](./getobjectowner-method-adox.md)   
 [SetObjectOwner (método)](./setobjectowner-method.md)