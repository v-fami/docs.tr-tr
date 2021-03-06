---
title: StrongNameSignatureVerificationEx İşlevi
ms.date: 03/30/2017
api_name:
- StrongNameSignatureVerificationEx
api_location:
- mscoree.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameSignatureVerificationEx
helpviewer_keywords:
- StrongNameSignatureVerificationEx function [.NET Framework strong naming]
ms.assetid: cfe4b634-18bf-44b8-9773-d94fb7e8a480
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 049b7b11473a05d74dc311ca6ee79947039b0dd1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61794426"
---
# <a name="strongnamesignatureverificationex-function"></a>StrongNameSignatureVerificationEx İşlevi
Sağlanan yol, derleme bildirimi tanımlayıcı ad imzası içerip içermediğini gösteren bir değer alır.  
  
 Bu işlev kullanım dışı bırakıldı. Kullanım [Iclrstrongname::strongnamesignatureverificationex](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverificationex-method.md) yöntemi yerine.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
BOOLEAN StrongNameSignatureVerificationEx (  
    [in]  LPCWSTR   wszFilePath,  
    [in]  BOOLEAN   fForceVerification,  
    [out] BOOLEAN   *pfWasVerified  
);  
```  
  
## <a name="parameters"></a>Parametreler  
 `wszFilePath`  
 [in] Taşınabilir yürütülebilir (.exe veya .dll) dosyası doğrulanması derleme yolu.  
  
 `fForceVerification`  
 [in] `true` , olsa bile gerekli kayıt defteri ayarlarını geçersiz kılmak; Aksi takdirde, doğrulamanın `false`.  
  
 `pfWasVerified`  
 [out] `true` tanımlayıcı ad imzası, doğrulanmış; Aksi takdirde `false`. `pfWasVerified` Ayrıca kümesine `false` kayıt defteri ayarları nedeniyle doğrulama başarılı olursa.  
  
## <a name="return-value"></a>Dönüş Değeri  
 `true` doğrulama başarılı olduysa; Aksi takdirde, `false`.  
  
## <a name="remarks"></a>Açıklamalar  
 `StrongNameSignatureVerificationEx` benzer şekilde bir özellik sunar [StrongNameSignatureVerification](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignatureverification-function.md) işlevi. Ancak, giriş parametresi ve çıkış parametresi için ikinci `StrongNameSignatureVerificationEx` türü `BOOLEAN` yerine `DWORD`.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** StrongName.h  
  
 **Kitaplığı:** Bir kaynak olarak mscoree.dll dahil  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [StrongNameSignatureVerificationEx Yöntemi](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverificationex-method.md)
- [StrongNameSignatureVerification Yöntemi](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamesignatureverification-method.md)
- [ICLRStrongName Arabirimi](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
