---
title: ICorDebugModule2 Arabirimi
ms.date: 03/30/2017
api_name:
- ICorDebugModule2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2
helpviewer_keywords:
- ICorDebugModule2 interface [.NET Framework debugging]
ms.assetid: 0847e64f-fdbe-4c96-8168-da20fdc84d80
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d3fb1bf3f61c78f4eb157b93363b1c06b25bee04
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61987954"
---
# <a name="icordebugmodule2-interface"></a>ICorDebugModule2 Arabirimi

Icordebugmodule arabirimi mantıksal uzantısı olarak görev yapar.  
  
## <a name="methods"></a>Yöntemler  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[ApplyChanges Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-applychanges-method.md)|Meta veri değişiklikleri ve Microsoft Ara dil (MSIL) kodu değişiklikleri çalışan işlemi için geçerlidir.|  
|[GetJITCompilerFlags Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-getjitcompilerflags-method.md)|Just-in-time (JIT) derlenmesi için bu denetim bayrakları alır `ICorDebugModule2`.|  
|[ResolveAssembly Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-resolveassembly-method.md)|Belirtilen meta veri belirteci tarafından başvurulan derlemenin çözümler.|  
|[SetJITCompilerFlags Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-setjitcompilerflags-method.md)|Bunun için JIT derlemesi denetleyen bayraklar ayarlar `ICorDebugModule2`.|  
|[SetJMCStatus Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-setjmcstatus-method.md)|Bu tüm yöntemleri tüm sınıflara yalnızca benim kodum (JMC) durumunu ayarlar `ICorDebugModule2` hariç belirtilen değere `pTokens` dizisi karşı değer olarak ayarlar.|  
  
## <a name="remarks"></a>Açıklamalar  
  
> [!NOTE]
>  Bu arabirim makineler arası veya çapraz işlem uzaktan çağrılan desteklemez.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** CorDebug.idl, CorDebug.h  
  
 **Kitaplığı:** CorGuids.lib  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Hata Ayıklama Arabirimleri](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
