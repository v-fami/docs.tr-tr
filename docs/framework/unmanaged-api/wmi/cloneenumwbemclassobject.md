---
title: CloneEnumWbemClassObject işlevi (yönetilmeyen API Başvurusu)
description: CloneEnumWbemClassObject işlevi bir numaralandırıcı mantıksal bir kopyasını oluşturur.
ms.date: 11/06/2017
api_name:
- CloneEnumWbemClassObject
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- CloneEnumWbemClassObject
helpviewer_keywords:
- CloneEnumWbemClassObject function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f7b384bb24cbf7ab7379949fd85a22121a1310e3
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65636863"
---
# <a name="cloneenumwbemclassobject-function"></a>CloneEnumWbemClassObject işlevi
Numaralandırma içindeki geçerli konumu koruma Numaralandırıcı mantıksal bir kopyasını oluşturur.

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a>Sözdizimi

```
HRESULT CloneEnumWbemClassObject (
   [out] IEnumWbemClassObject**  ppEnum, 
   [in] DWORD                    authLevel,
   [in] DWORD                    impLevel,
   [in] IEnumWbemClassObject*    pCurrentEnumWbemClassObject, 
   [in] BSTR                     strUser,
   [in] BSTR                     strPassword,
   [in BSTR]                     strAuthority 
); 
```

## <a name="parameters"></a>Parametreler

`ppEnum`\
[out] Yeni bir işaretçi alır [IEnumWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-ienumwbemclassobject).

`authLevel`\
[in] Yetkilendirme düzeyi.

`impLevel`\
[in] Kimliğe bürünme düzeyi.

`pCurrentEnumWbemClassObject`\
[out] Bir işaretçi [IEnumWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-ienumwbemclassobject) kopyalanma örneği.

`strUser`\
[in] Kullanıcı adı. Bkz: [ConnectServerWmi](connectserverwmi.md) işlevi daha fazla bilgi için.

`strPassword`\
[in] Parola. Bkz: [ConnectServerWmi](connectserverwmi.md) işlevi daha fazla bilgi için.

`strAuthority`\ [in] kullanıcının etki alanı adı. Bkz: [ConnectServerWmi](connectserverwmi.md) işlevi daha fazla bilgi için.

## <a name="return-value"></a>Dönüş değeri

Bu işlev tarafından döndürülen aşağıdaki değerleri tanımlanan *WbemCli.h* üst bilgi dosyası veya tanımlayabilirsiniz bunları sabitleri kodunuzda:

|Sabit  |Değer  |Açıklama  |
|---------|---------|---------|
| `WBEM_E_FAILED` | 0x80041001 | Genel bir hata oluştu. |
| `WBEM_E_INVALID_PARAMETER` | 0x80041008 | Bir parametre geçersiz. |
| `WBEM_E_OUT_OF_MEMORY` | 0x80041006 | Kullanılabilir yeterli bellek işlem tamamlanamadı. |
| `WBEM_E_TRANSPORT_FAILURE` | 0x80041015 | Geçerli işlem WMI arasındaki uzak yordam çağrısı (RPC) bağlantı başarısız oldu. |
| `WBEM_S_NO_ERROR` | 0 | İşlev çağrısı başarılı oldu.  |

## <a name="remarks"></a>Açıklamalar

Bu işlev bir çağrı sarılır [IEnumWbemClassObject::Clone](/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-clone) yöntemi.

Bu yöntem yalnızca bir "en iyi çaba" kopya oluşturur. Birçok CIM Nesne dinamik doğası nedeniyle yeni Numaralandırıcı kaynak Numaralandırıcı aynı nesne kümesini numaralandırmaz mümkündür.

İşlev çağrısı başarısız olursa, ek hata bilgileri çağırarak elde edebileceğiniz [Geterrorınfo](geterrorinfo.md) işlevi.

## <a name="example"></a>Örnek

Bir örnek için bkz. [IEnumWbemClassObject::Clone](/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-clone) yöntemi.

## <a name="requirements"></a>Gereksinimler
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).

 **Üst bilgi:** WMINet_Utils.idl

 **.NET framework sürümleri:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]

## <a name="see-also"></a>Ayrıca bkz.

- [WMI ve performans sayaçları (yönetilmeyen API Başvurusu)](index.md)
