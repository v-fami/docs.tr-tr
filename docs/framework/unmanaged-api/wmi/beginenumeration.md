---
title: BeginEnumeration işlevi (yönetilmeyen API Başvurusu)
description: BeginEnumeration işlevi Numaralayıcı sabit başlangıcına sıfırlar.
ms.date: 11/06/2017
api_name:
- BeginEnumeration
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- BeginEnumeration
helpviewer_keywords:
- BeginEnumeration function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 07396428dafbaa76e7771a4022bb493768f9f6c1
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65636799"
---
# <a name="beginenumeration-function"></a>BeginEnumeration işlevi
Bir numaralandırıcı geri numaralandırma başlangıç durumuna sıfırlar.  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT BeginEnumeration (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr, 
   [in] LONG              lEnumFlags
); 
```  

## <a name="parameters"></a>Parametreler

`vFunc`\
[in] Bu parametre kullanılmaz.

`ptr`\
[in] Bir işaretçi bir [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) örneği.

`lEnumFlags`\
[in] Bayrakları veya açıklanan değerler Bitsel bir birleşimi [açıklamalar](#remarks) numaralandırmada özellikleri denetleyen bölümü.

## <a name="return-value"></a>Dönüş değeri

Bu işlev tarafından döndürülen aşağıdaki değerleri tanımlanan *WbemCli.h* üst bilgi dosyası veya tanımlayabilirsiniz bunları sabitleri kodunuzda:

|Sabit  |Değer  |Açıklama  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | 0x80041008 | Bayrakları birleşimi `lEnumFlags` geçersiz veya geçersiz bir bağımsız değişken belirtildi. |
|`WBEM_E_UNEXPECTED` | 0x8004101d | İkinci çağrı `BeginEnumeration` bir çağrı göndermelisiniz olmadan yapılan [ `EndEnumeration` ](endenumeration.md). |
|`WBEM_E_OUT_OF_MEMORY` | 0x80041006 | Yeni bir numaralandırma başlatmak yeterli bellek yok. |
|`WBEM_S_NO_ERROR` | 0 | İşlev çağrısı başarılı oldu.  |
  
## <a name="remarks"></a>Açıklamalar

Bu işlev bir çağrı sarılır [IWbemClassObject::BeginEnumeration](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) yöntemi.

Olarak geçirilen bayraklar `lEnumFlags` bağımsız değişken tanımlanmış *WbemCli.h* üst bilgi dosyası veya tanımlayabilirsiniz bunları sabitleri kodunuzda.  Herhangi diğer bir grup bayrağı ile her bir gruptan bir bayrak birleştirebilirsiniz. Ancak, aynı grup bayrakları birbirini dışlar. 

**Grup 1**

|Sabit  |Değer  |Açıklama  |
|---------|---------|---------|
|`WBEM_FLAG_KEYS_ONLY` | 0x4 | Yalnızca anahtar oluşturan özellikleri içerir. |
|`WBEM_FLAG_REFS_ONLY` | 0x8 | Nesne başvuruları yalnızca özellikleri içerir. |

**Grup 2**

Sabit  |Değer  |Açıklama  |
|---------|---------|---------|
|`WBEM_FLAG_SYSTEM_ONLY` | 0x30 | Sistem özellikleri yalnızca numaralandırma sınırlayın. |
|`WBEM_FLAG_NONSYSTEM_ONLY` | 0x40 | Yerel ve yayılan özellikleri içerir, ancak Sistem özellikleri sabit listesinden alınmış hariç. |

Sınıflar için:

Sabit  |Değer  |Açıklama  |
|---------|---------|---------|
|`WBEM_FLAG_CLASS_OVERRIDES_ONLY` | 0x100 | Sınıf tanımında geçersiz kılınan özellikleri için sabit sınırlar. |
|`WBEM_FLAG_CLASS_LOCAL_AND_OVERRIDES` | 0x100 | Geçerli sınıf tanımında geçersiz kılınan özellikleri ve yeni özellikleri sınıfta tanımlanan sabit sınırlar. |
| `WBEM_MASK_CLASS_CONDITION` | 0x300 | Karşı uygulamak için bir maske (yerine bir bayrak) bir `lEnumFlags` ya da denetlenecek değer `WBEM_FLAG_CLASS_OVERRIDES_ONLY` veya `WBEM_FLAG_CLASS_LOCAL_AND_OVERRIDES` ayarlanır. |
| `WBEM_FLAG_LOCAL_ONLY` | 0x10 | Sabit listesi sınıfı, değiştiren veya tanımlanan özelliklere sınırlayın. |
| `WBEM_FLAG_PROPAGATED_ONLY` |  0x20 | Temel sınıftan devralınan özellikler için sabit sınırlar. |

İçin örnek:

Sabit  |Değer  |Açıklama  |
|---------|---------|---------|
| `WBEM_FLAG_LOCAL_ONLY` | 0x10 | Sabit listesi sınıfı, değiştiren veya tanımlanan özelliklere sınırlayın. |
| `WBEM_FLAG_PROPAGATED_ONLY` |  0x20 | Temel sınıftan devralınan özellikler için sabit sınırlar. |

## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** WMINet_Utils.idl  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [WMI ve performans sayaçları (yönetilmeyen API Başvurusu)](index.md)
