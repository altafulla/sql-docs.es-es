---
title: Creación de una credencial - autenticarse en Azure Storage | Microsoft Docs
description: En SQL Server, use la página Crear credencial del cuadro de diálogo Copia de seguridad de base de datos para especificar un certificado de administración de Azure para validar la conexión.
ms.custom: ''
ms.date: 03/01/2017
ms.prod: sql
ms.prod_service: backup-restore
ms.reviewer: ''
ms.technology: backup-restore
ms.topic: conceptual
f1_keywords:
- sql13.swb.backuptourl.createcred.f1
ms.assetid: 0622619d-27c5-4ff0-83e5-cde31648c27a
author: MikeRayMSFT
ms.author: mikeray
ms.openlocfilehash: b75085f8b5c01ad5257f5bc165f32be7a7a91902
ms.sourcegitcommit: 04cf7905fa32e0a9a44575a6f9641d9a2e5ac0f8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/07/2020
ms.locfileid: "91809246"
---
# <a name="create-credential---authenticate-to-azure-storage"></a>Crear credencial - autenticarse en Azure Storage
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]
  Use el cuadro de diálogo **Copia de seguridad en URL - Crear credencial** para crear una credencial de SQL.  
  
 Al utilizar este cuadro de diálogo para crear una credencial, debe proporcionar un certificado de administración de Azure agregado al almacén de certificados local o un perfil de publicación descargado en el equipo para validar la suscripción y la información de la cuenta de almacenamiento.  
  
 **Credencial SQL**  
 Especifique el nombre de la credencial SQL que desea crear.  
  
## <a name="azure-credentials"></a>Credenciales de Azure  
 **Certificado de administración**  
 Use esta opción para especificar un certificado del almacén de certificados local que coincida con el certificado de administración de Azure. Para obtener más información sobre el certificado de administración de Azure, vea [Creación y actualización de un certificado de administración para Azure](/previous-versions/azure/gg551722(v=azure.100)).  
  
 **Suscripción**  
 Seleccione, escriba o pegue el identificador de su suscripción de Azure que coincida con el certificado de administración del almacén de certificados local.  
  
 **Perfil de publicación**  
 Use esta opción si tiene un perfil de publicación descargado en el equipo. Si utiliza esta opción, el identificador de suscripción y el certificado se rellenan de forma automática.  
  
> [!CAUTION]  
>  SQL Server admite actualmente la versión 2.0 del perfil de publicación. Para descargar la versión compatible del perfil de publicación, vea [Descargar perfil de publicación 2.0](https://go.microsoft.com/fwlink/?LinkId=396421).  
  
## <a name="storage-account"></a>Cuenta de almacenamiento  
 Seleccione la cuenta de almacenamiento que desea usar para almacenar los archivos de copia de seguridad.  
  
