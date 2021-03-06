---
title: CorBindToCurrentRuntime İşlevi
ms.date: 03/30/2017
api_name:
- CorBindToCurrentRuntime
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- HeaderDef
f1_keywords:
- CorBindToCurrentRuntime
helpviewer_keywords:
- CorBindToCurrentRuntime function [.NET Framework hosting]
ms.assetid: 6105c13e-d9cd-44d2-a95a-924e042830c7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d0acb322fa3348f0bb2d819529a370110580343c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61985887"
---
# <a name="corbindtocurrentruntime-function"></a>CorBindToCurrentRuntime İşlevi
Ortak dil çalışma zamanı (CLR), bir XML dosyasında depolanan sürüm bilgilerini kullanarak bir işlem içine yükler. XML dosyasının biçimi sonra standart uygulama yapılandırma dosyasına modellenir. Yapılandırma dosyaları hakkında daha fazla bilgi için bkz. [yapılandırma dosyası şeması](../../../../docs/framework/configure-apps/file-schema/index.md).  
  
 Bu işlev içinde kullanımdan kalkmış [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)]. Bkz: [ortak dil çalışma zamanını bir işleme yükleme](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/01918c6x(v=vs.100)).  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT CorBindToCurrentRuntime (  
    [in]  LPCWSTR   pwszFileName,  
    [in]  REFCLSID  rclsid,  
    [in]  REFIID    riid,  
    [out] LPVOID    *ppv  
);  
```  
  
## <a name="parameters"></a>Parametreler  
 `pwszFileName`  
 [in] Yüklenecek CLR sürümünü belirten bir uygulama yapılandırma dosyası adı. Dosya adı tam nitelenmiş değil, çağrıyı yapan yürütülebilir dosya ile aynı dizinde olduğu varsayılır.  
  
 Yüklenecek çalışma zamanı sürümü içindeki version özniteliği tarafından tanımlanan [ \<requiredRuntime >](../../../../docs/framework/configure-apps/file-schema/startup/requiredruntime-element.md) yapılandırma dosyasının öğesi.  
  
 Hiçbir sürüm belirtilmezse veya `<requiredRuntime>` öğesi bulunamıyor, makinede yüklü CLR en son sürümü yüklendi.  
  
 `rclsid`  
 [in] `CLSID` Ya da uygulayan yardımcı sınıf, [Icorruntimehost](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md) veya [Iclrruntimehost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md) arabirimi. Desteklenen değerler: clsıd_corruntimehost veya clsıd_clrruntimehost şunlardır.  
  
 `riid`  
 [in] `IID` Arabirimin istiyorsunuz. Desteklenen değerler: ııd_ıcorruntimehost veya ııd_ıclrruntimehost şunlardır.  
  
 `ppv`  
 [out] Döndürülen arabirim işaretçisi.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** MSCorEE.h  
  
 **Kitaplığı:** MSCorEE.dll  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [CorBindToRuntime İşlevi](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntime-function.md)
- [CorBindToRuntimeByCfg İşlevi](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimebycfg-function.md)
- [CorBindToRuntimeEx İşlevi](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)
- [CorBindToRuntimeHost İşlevi](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimehost-function.md)
- [ICorRuntimeHost Arabirimi](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
- [Kullanım Dışı CLR Barındırma İşlevleri](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
