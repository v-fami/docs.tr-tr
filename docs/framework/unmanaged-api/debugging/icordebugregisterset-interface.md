---
title: ICorDebugRegisterSet Arabirimi
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet
helpviewer_keywords:
- ICorDebugRegisterSet interface [.NET Framework debugging]
ms.assetid: d3d9676d-0b87-4bc3-b679-7bbc7a186c88
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7b0a5d80d984a3c696b178c4d8c936bd47354945
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61782882"
---
# <a name="icordebugregisterset-interface"></a>ICorDebugRegisterSet Arabirimi
Şu anda kod yürüttüğünü bilgisayarda bulunan yazmaç kümesini temsil eder.  
  
## <a name="methods"></a>Yöntemler  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetRegisters Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-getregisters-method.md)|Her kaydın değerini alır (şu anda kod yürüttüğünü bilgisayarda) bit maskesi kullanılarak belirtilir.|  
|[GetRegistersAvailable Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-getregistersavailable-method.md)|Alır bir bit maskesi bu kayıtları belirten `ICorDebugRegisterSet` şu anda kullanılabilir.|  
|[GetThreadContext Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-getthreadcontext-method.md)|Geçerli iş parçacığı bağlamını alır.|  
|[SetRegisters Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-setregisters-method.md)|.NET Framework sürüm 2.0 uygulanmadı.|  
|[SetThreadContext Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-setthreadcontext-method.md)|.NET Framework 2.0 için uygulanmadı.|  
  
## <a name="remarks"></a>Açıklamalar  
 `ICorDebugRegisterSet` Arabirimi yalnızca 32-bit kayıtlarını destekler. Kullanım [Icordebugregisterset2](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md) gerektiren ek kayıtlar gibi platformlardaki IA-64 arabirimi.  
  
> [!NOTE]
>  Bu arabirim makineler arası veya çapraz işlem uzaktan çağrılan desteklemez.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** CorDebug.idl, CorDebug.h  
  
 **Kitaplığı:** CorGuids.lib  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Hata Ayıklama Arabirimleri](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [ICorDebugRegisterSet2 Arabirimi](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)
