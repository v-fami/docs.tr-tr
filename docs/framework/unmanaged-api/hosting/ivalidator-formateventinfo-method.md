---
title: IValidator::FormatEventInfo Yöntemi
ms.date: 03/30/2017
api_name:
- IValidator.FormatEventInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- FormatEventInfo
helpviewer_keywords:
- IValidator::FormatEventInfo method [.NET Framework hosting]
- FormatEventInfo method, IValidator interface [.NET Framework hosting]
ms.assetid: 4c0c7477-05ba-461b-b21b-cbfba95f1db1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ecbecec86d81357000679ab50e12f06d91c9f50d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61765381"
---
# <a name="ivalidatorformateventinfo-method"></a>IValidator::FormatEventInfo Yöntemi
Belirtilen doğrulama hatası için karşılık gelen hata iletisini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT FormatEventInfo(  
    [in] HRESULT            hVECode,  
    [in] VEContext          Context,  
    [in, out] LPWSTR        msg,  
    [in] unsigned long      ulMaxLength,  
    [in] SAFEARRAY(VARIANT) psa  
);  
```  
  
## <a name="parameters"></a>Parametreler  
 `hVECode`  
 [in] Doğrulama hata işleyicisine geçirilen HRESULT değerini.  
  
 `Context`  
 [in] A `VEContext` doğrulama hatası ile ilgili bağlam bilgilerini içeren bir örneği.  
  
 `msg`  
 [out içinde] Döndürülen hata iletisi içeren bir dize.  
  
 `ulMaxLength`  
 [in] Hata iletisi en fazla uzunluğu.  
  
 `psa`  
 [in] Hatayı açıklayan ek parametreler içeren güvenli bir dizi.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** IValidator.idl, IValidator.h  
  
 **Kitaplığı:** Bir kaynak olarak MSCorEE.dll dahil  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
