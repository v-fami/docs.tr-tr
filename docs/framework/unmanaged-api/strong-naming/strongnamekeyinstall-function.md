---
title: StrongNameKeyInstall İşlevi
ms.date: 03/30/2017
api_name:
- StrongNameKeyInstall
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameKeyInstall
helpviewer_keywords:
- StrongNameKeyInstall function [.NET Framework strong naming]
ms.assetid: e32fd546-7757-4681-be3d-658e93281e50
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7121ace6777e7cf947fcc6ff30b1ea314851feff
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65636712"
---
# <a name="strongnamekeyinstall-function"></a>StrongNameKeyInstall İşlevi

Bir ortak/özel anahtar çifti bir kapsayıcının içine aktarır.

Bu işlev kullanım dışı bırakıldı. Kullanım [Iclrstrongname::strongnamekeyınstall](../hosting/iclrstrongname-strongnamekeyinstall-method.md) yöntemi yerine.

## <a name="syntax"></a>Sözdizimi

```cpp
BOOLEAN StrongNameKeyInstall (
    [in]  LPCWSTR   wszKeyContainer,
    [in]  BYTE      *pbKeyBlob,
    [in]  ULONG     cbKeyBlob
);
```

## <a name="parameters"></a>Parametreler

`wszKeyContainer`\
[in] Anahtar kapsayıcısının adı. `wszKeyContainer` boş olmayan bir dize olmalıdır.

`pbKeyBlob`\
[in] İkili bir anahtar çifti.

`cbKeyBlob`\
[in] Bayt cinsinden boyutu, `pbKeyBlob`.

## <a name="return-value"></a>Dönüş Değeri

`true` başarıyla tamamlandığında; Aksi takdirde, `false`.

## <a name="remarks"></a>Açıklamalar

Kullanım [StrongNameKeyDelete](strongnamekeydelete-function.md) işlevi anahtar kapsayıcısı silinemedi.

Varsa `StrongNameKeyInstall` işlevi değil başarıyla tamamlanması, çağrı [Strongnameerrorınfo](strongnameerrorinfo-function.md) oluşturulan son hatayı alması için işlevi.

## <a name="requirements"></a>Gereksinimler

**Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).

**Üst bilgi:** StrongName.h

**Kitaplığı:** Bir kaynak olarak MsCorEE.dll dahil

**.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]

## <a name="see-also"></a>Ayrıca bkz.

- [StrongNameKeyInstall Yöntemi](../hosting/iclrstrongname-strongnamekeyinstall-method.md)
- [StrongNameKeyDelete Yöntemi](../hosting/iclrstrongname-strongnamekeydelete-method.md)
- [ICLRStrongName Arabirimi](../hosting/iclrstrongname-interface.md)
