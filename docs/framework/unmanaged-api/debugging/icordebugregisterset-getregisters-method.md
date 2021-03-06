---
title: ICorDebugRegisterSet::GetRegisters Metodu
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.GetRegisters
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::GetRegisters
helpviewer_keywords:
- GetRegisters method, ICorDebugRegisterSet interface [.NET Framework debugging]
- ICorDebugRegisterSet::GetRegisters method [.NET Framework debugging]
ms.assetid: fdf91864-48ea-4aa6-b70c-361b7a3184c7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b417685361126951470571e2440cc842ab1c94fb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61782921"
---
# <a name="icordebugregistersetgetregisters-method"></a>ICorDebugRegisterSet::GetRegisters Metodu
Her kaydın değerini alır (şu anda kod yürüttüğünü bilgisayarda) bit maskesi kullanılarak belirtilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT GetRegisters (  
    [in] ULONG64       mask,   
    [in] ULONG32       regCount,  
    [out, size_is(regCount), length_is(regCount)]  
        CORDB_REGISTER regBuffer[]  
);  
```  
  
## <a name="parameters"></a>Parametreler  
 `mask`  
 [in] Hangi kayıt alınması için değerler belirten bir bit maskesi. Her bit bir kasaya karşılık gelir. Bir bit olarak ayarlanırsa kasanın değeri alınır; Aksi takdirde, kaydın değeri alınamadı.  
  
 `regCount`  
 [in] YAZMAÇ değerlerini alınacak sayısı.  
  
 `regBuffer`  
 [out] Bir dizi `CORDB_REGISTER` nesneleri, her biri bir kayıt değeri alır.  
  
## <a name="remarks"></a>Açıklamalar  
 Dizinin boyutu bir bit maskesi için bitler sayısına eşit olmalıdır. `regCount` Parametresi, YAZMAÇ değerlerini alacak arabellek öğelerin sayısını belirtir. Varsa `regCount` değeri numarası maskesi tarafından belirtilen kayıtları için çok küçük, daha yüksek numaralı kayıtları kümesinden kesilecek. Varsa `regCount` değer çok büyük olduğu kullanılmayan `regBuffer` öğeleri değiştirilmemiş olacaktır.  
  
 Bit maskesi kullanılamıyor, bir kayıt belirtiyorsa `GetRegisters` konusu kasaya belirsiz bir değer döndürür.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** CorDebug.idl, CorDebug.h  
  
 **Kitaplığı:** CorGuids.lib  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [ICorDebugRegisterSet Arabirimi](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md)
- [ICorDebugRegisterSet2 Arabirimi](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)
