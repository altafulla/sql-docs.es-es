---
description: MSSQLSERVER_33081
title: MSSQLSERVER_33081 | Microsoft Docs
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.reviewer: ''
ms.technology: supportability
ms.topic: language-reference
helpviewer_keywords:
- 33081 (Database Engine error)
ms.assetid: 839705e7-fa37-4c0d-9f3f-95a9eab98bcf
author: MashaMSFT
ms.author: mathoma
ms.openlocfilehash: 3267a9195cd5128864bcb55503ffe1720be9299c
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88456327"
---
# <a name="mssqlserver_33081"></a>MSSQLSERVER_33081
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  
## <a name="details"></a>Detalles  
  
| Atributo | Value |  
| :-------- | :---- |  
|Nombre de producto|SQL Server|  
|Id. de evento|33081|  
|Origen de eventos|MSSQLSERVER|  
|Componente|SQLEngine|  
|Nombre simbólico|SEC_DLL_TRUST_VERIFICATION_FAILED|  
|Texto del mensaje|No se pudo cargar el proveedor de servicios criptográficos '%.*ls' debido a una firma Authenticode o una ruta de archivo no válida.  Revise los mensajes de otros errores anteriores.|  
  
## <a name="explanation"></a>Explicación  
[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] no pudo cargar el proveedor de servicios criptográficos enumerado en el mensaje de error. Hay varios errores de la API de Windows que podrían producir este error. El búfer en anillo contiene el nombre de la API con errores y el código de error de Windows devueltos por la API. Para obtener más información, consulte la vista de sys.dm_os_ring_buffers mediante lo siguiente.  
  
```  
SELECT * FROM sys.dm_os_ring_buffers   
WHERE ring_buffer_type = 'RING_BUFFER_SECURITY_ERROR';  
```  
  
## <a name="user-action"></a>Acción del usuario  
Para estudiar el problema, busque el código de error de Windows en MSDN (https://msdn.microsoft.com/). Resuelva el error o póngase en contacto con [!INCLUDE[msCoName](../../includes/msconame-md.md)] CSS para obtener más información. Si necesita ponerse en contacto con CSS, recopile la información siguiente para nuestro personal de soporte técnico.  
  
-   El registro de errores que muestra el error de carga del proveedor de servicios criptográficos.  
  
-   La salida de la instrucción siguiente:  
  
    ```  
    SELECT * FROM sys.dm_os_ring_buffers   
    WHERE ring_buffer_type = 'RING_BUFFER_SECURITY_ERROR';  
    ```  
  
> [!NOTE]  
> Intente recopilar la información de búfer en anillo enseguida, ya que se puede perder durante un reinicio.  
  
