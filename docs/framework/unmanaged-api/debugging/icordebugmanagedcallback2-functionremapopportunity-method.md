---
title: ICorDebugManagedCallback2::FunctionRemapOpportunity Yöntemi
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2.FunctionRemapOpportunity
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2::FunctionRemapOpportunity
helpviewer_keywords:
- FunctionRemapOpportunity method [.NET Framework debugging]
- ICorDebugManagedCallback2::FunctionRemapOpportunity method [.NET Framework debugging]
ms.assetid: 0d6471bc-ad9b-4b1d-a307-c10443918863
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 14291ced9a606cc0b2a3792c2157b7bc2a3460a3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61756240"
---
# <a name="icordebugmanagedcallback2functionremapopportunity-method"></a>ICorDebugManagedCallback2::FunctionRemapOpportunity Yöntemi
Hata ayıklayıcı, yürütmeyi bir dizi noktası düzenlenmiş bir işlevin daha eski bir sürümünde ulaştı bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT FunctionRemapOpportunity (  
    [in] ICorDebugAppDomain   *pAppDomain,  
    [in] ICorDebugThread      *pThread,  
    [in] ICorDebugFunction    *pOldFunction,  
    [in] ICorDebugFunction    *pNewFunction,  
    [in] ULONG32              oldILOffset  
);  
```  
  
## <a name="parameters"></a>Parametreler  
 `pAppDomain`  
 [in] İşlev düzenlendi içeren uygulama etki alanını temsil eden bir Icordebugappdomain nesne işaretçisi.  
  
 `pThread`  
 [in] Kesme noktası eşleme tespit edildi iş parçacığını temsil eden bir Icordebugthread nesne işaretçisi.  
  
 `pOldFunction`  
 [in] İş parçacığı üzerinde çalışmakta olan işlevin sürümünü temsil eden bir ICorDebugFunction nesne işaretçisi.  
  
 `pNewFunction`  
 [in] İşlevin en son sürümünü temsil eden bir ICorDebugFunction nesne işaretçisi.  
  
 `oldILOffset`  
 [in] Microsoft Ara dili (MSIL) yönerge işaretçisinin işlevi'nın eski sürümünde uzaklığı.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu geri çağırma, hata ayıklayıcı çağırarak uygun onun yerine yeni sürümü, belirtilen işlev için yönerge işaretçisini yeniden eşlemek için bir fırsat sağlar. [Icordebugılframe2::RemapFunction](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe2-remapfunction-method.md) yöntemi. Hata ayıklayıcı değil çağırırsanız `RemapFunction` çağırmadan önce [Icordebugcontroller::continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) yöntemi, çalışma zamanı, eski kod yürütülmeye devam eder ve başka ateşlenir `FunctionRemapOpportunity` sonraki dizisi noktasına geri çağırma.  
  
 Bu geri çağırma, hata ayıklayıcı S_OK döndürür kadar verilen işlevin daha eski bir sürümünü yürüten her karede çağrılır.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** CorDebug.idl, CorDebug.h  
  
 **Kitaplığı:** CorGuids.lib  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [ICorDebugManagedCallback2 Arabirimi](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md)
- [ICorDebugManagedCallback Arabirimi](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
