---
title: Blessıwbemservicesobject işlevi (yönetilmeyen API Başvurusu)
description: Blessıwbemservicesobject işlevi kullanıcı kimlik bilgilerini IWbemServices nesneyi erişime olup olmadığını gösterir.
ms.date: 11/06/2017
api_name:
- BlessIWbemServicesObject
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- BlessIWbemServicesObject
helpviewer_keywords:
- BlessIWbemServicesObject function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d28497c637a40d7e2659b18868124ea898397f92
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65636902"
---
# <a name="blessiwbemservicesobject-function"></a>BlessIWbemServicesObject işlevi
Kullanıcı kimlik bilgilerini belirtilen erişim izni olup olmadığını gösteren [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) nesne. 

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a>Sözdizimi

```
HRESULT BlessIWbemServicesObject (
   [in] IUnknown* pIUnknown,
   [in] BSTR strUser, 
   [in] BSTR strPassword, 
   [in] BSTR strAuthority, 
   [in] DWORD impLevel, 
   [in] DWORD authnLevel
);
```

## <a name="parameters"></a>Parametreler

`pIWbemServices`\
[in] WMI hizmet nesnesine bir işaretçi.

`strUser`\
[in] Kullanıcı adı.

`strPassword`\
[in] İlişkili parolayı `strUser`.

`strAuthority`\
[in] Kullanıcı etki alanı adı. Bkz: [ConnectServerWmi](connectserverwmi.md) işlevi daha fazla bilgi için.

`impLevel`\
[in] Kimliğe bürünme düzeyi.

`authnLevel`\
[in] Yetkilendirme düzeyi.

## <a name="return-value"></a>Dönüş değeri

Bu işlev tarafından döndürülen aşağıdaki değerleri tanımlanan *Wınerror* üst bilgi dosyası veya tanımlayabilirsiniz bunları sabitleri kodunuzda:

|Sabit  |Değer  |Açıklama  |
|---------|---------|---------|
| `E_INVALIDARG` | 0x80070057 | Bir veya daha fazla bağımsız değişken geçersiz. |
| `E_POINTER` | 0x80004003 | `pIWbemServices` olan `null`. | 
| `E_FAIL` | 0x80000008 | Belirtilmeyen bir hata oluştu. |
| `E_OUTOFMEMORY` | 0x80000002 | İşlemi gerçekleştirmek yeterli bellek yok. | 
| `S_OK` | 0 | İşlev çağrısı başarılı oldu. | 

## <a name="requirements"></a>Gereksinimler

 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).

 **Üst bilgi:** WMINet_Utils.idl

 **.NET framework sürümleri:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]

## <a name="see-also"></a>Ayrıca bkz.

- [WMI ve performans sayaçları (yönetilmeyen API Başvurusu)](index.md)
