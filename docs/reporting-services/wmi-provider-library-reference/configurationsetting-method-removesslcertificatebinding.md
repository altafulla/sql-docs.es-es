---
description: Método RemoveSSLCertificateBindings (WMI MSReportServer_ConfigurationSetting)
title: Método RemoveSSLCertificateBindings (MSReportServer_ConfigurationSetting de WMI) | Microsoft Docs
ms.date: 03/01/2017
ms.prod: reporting-services
ms.prod_service: reporting-services-native
ms.technology: wmi-provider-library-reference
ms.topic: conceptual
helpviewer_keywords:
- RemoveSSLCertificateBindings method
ms.assetid: b8b484c9-04c4-4ae9-980e-67bbe5aa8481
author: maggiesMSFT
ms.author: maggies
ms.openlocfilehash: edead6fb553151265556163659eb6b1383918c6d
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "88423169"
---
# <a name="configurationsetting-method---removesslcertificatebinding"></a>Método ConfigurationSetting - RemoveSSLCertificateBinding
  Quita un enlace de certificado TLS/SSL.  
  
## <a name="syntax"></a>Sintaxis  
  
```vb  
Public Sub RemoveSSLCertificateBinding(ByVal Application As String, _  
    ByVal CertificateHash As String, ByVal IPAddress As String, _  
    ByVal Port As Int32, ByVal Lcid As Int32, _  
    ByRef [Error] As String, ByRef HRESULT As Int32)  
```  
  
```csharp  
public void RemoveSSLCertificateBindings(string Application,  
    string CertificateHash, string IPAddress, Int32 Port, Int32 Lcid,  
    out string Error, out Int32 HRESULT);  
```  
  
## <a name="parameters"></a>Parámetros  
 *Aplicación*  
 El nombre de la aplicación para la que se debería quitar el enlace de certificado.  
  
 *CertificateHash*  
 Valor hash del certificado.  
  
 *IPAddress*  
 Dirección IP para la aplicación.  
  
 *Puerto*  
 Puerto TLS asociado al enlace.  
  
 *lcid*  
 Configuración regional que se utilizará para los mensajes de error que se devuelven.  
  
 *Error*  
 [out] Descripción del error que se produjo.  
  
 *HRESULT*  
 [out] Valor que indica si la llamada se realizó correctamente o no.  
  
## <a name="return-value"></a>Valor devuelto  
 Devuelve *HRESULT* que indica si la llamada al método se realizó correctamente o no. Un valor de 0 indica que la llamada al método se realizó correctamente; un código de error indica que la llamada no se realizó correctamente.  
  
## <a name="remarks"></a>Observaciones  
 Este método quita el enlace específico del archivo rsreportserver.config y opcionalmente HTTP.SYS.  
  
## <a name="requirements"></a>Requisitos  
 **Espacio de nombres:** [!INCLUDE[ssRSWMInmspcA](../../includes/ssrswminmspca-md.md)]  
  
## <a name="see-also"></a>Consulte también  
 [Miembros MSReportServer_ConfigurationSetting](../../reporting-services/wmi-provider-library-reference/msreportserver-configurationsetting-members.md)  
  
  
