---
title: ICorProfilerCallback::ManagedToUnmanagedTransition Yöntemi
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ManagedToUnmanagedTransition
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ManagedToUnmanagedTransition
helpviewer_keywords:
- ManagedToUnmanagedTransition method [.NET Framework profiling]
- ICorProfilerCallback::ManagedToUnmanagedTransition method [.NET Framework profiling]
ms.assetid: ef3cd619-912d-40c5-a449-03ba02a39ee7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b00394d0b08e7e4a02b95437908dd65a51d0a042
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61597680"
---
# <a name="icorprofilercallbackmanagedtounmanagedtransition-method"></a>ICorProfilerCallback::ManagedToUnmanagedTransition Yöntemi
Profil Oluşturucu, yönetilen koddan yönetilmeyen koda geçiş oluştuğunu bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT ManagedToUnmanagedTransition(  
    [in] FunctionID functionId,  
    [in] COR_PRF_TRANSITION_REASON reason);  
```  
  
## <a name="parameters"></a>Parametreler  
 `functionId`  
 [in] Aranan işlev kimliği.  
  
 `reason`  
 [in] Değerini [cor_prf_transıtıon_reason](../../../../docs/framework/unmanaged-api/profiling/cor-prf-transition-reason-enumeration.md) geçiş nedeniyle yönetilen koddan yönetilmeyen koda bir çağrı veya yönetilmeyen bir tarafından çağrılan yönetilen bir işlev geri döndürme nedeniyle oluşup oluşmadığını belirten sabit listesi.  
  
## <a name="remarks"></a>Açıklamalar  
 Varsa değerini `reason` COR_PRF_TRANSITION_CALL, kimliğidir yönetilmeyen işlevi, hangi asla tam zamanında derleyici kullanarak derlenen, işlevi olduğu. Yönetilmeyen işlevleri, kendileriyle bir ad ve bazı meta veriler gibi ilgili temel bilgiler vardır. Örtük platform kullanarak yönetilmeyen işlev çağrıldı (PInvoke) çağırmak, çalışma zamanının çağrı hedefi ve değeri belirlenemiyor `functionId` null olacaktır. Örtük PInvoke hakkında daha fazla bilgi için bkz. [C++ Çalışabilirliği kullanma (örtük PInvoke)](/cpp/dotnet/using-cpp-interop-implicit-pinvoke).  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** CorProf.idl, CorProf.h  
  
 **Kitaplığı:** CorGuids.lib  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [ICorProfilerCallback Arabirimi](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [UnmanagedToManagedTransition Yöntemi](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-unmanagedtomanagedtransition-method.md)
- [C++'ta Açık PInvoke Kullanma (DllImport Özniteliği)](/cpp/dotnet/using-explicit-pinvoke-in-cpp-dllimport-attribute)
