---
title: ICorProfilerInfo::GetILToNativeMapping Metodu
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetILToNativeMapping
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetILToNativeMapping
helpviewer_keywords:
- GetILToNativeMapping method, ICorProfilerInfo interface [.NET Framework profiling]
- ICorProfilerInfo::GetILToNativeMapping method [.NET Framework profiling]
ms.assetid: 6a5431ef-22fb-4e53-bac5-703986297eb1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d7bbf0e03fc69332f77f3ac34a399a96f638da3f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61991841"
---
# <a name="icorprofilerinfogetiltonativemapping-method"></a>ICorProfilerInfo::GetILToNativeMapping Metodu
Harita, Microsoft Ara dili (MSIL) kodu belirtilen işlevinde yerel uzaklıklar için uzaklıkları alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT GetILToNativeMapping(  
    [in] FunctionID functionId,  
    [in] ULONG32 cMap,  
    [out] ULONG32 *pcMap,  
    [out, size_is(cMap), length_is(*pcMap)]  
        COR_DEBUG_IL_TO_NATIVE_MAP map[]);  
```  
  
## <a name="parameters"></a>Parametreler  
 `functionId`  
 [in] Kodu içeren işlev kimliği.  
  
 `cMap`  
 [in] En büyük boyutunu `map` dizisi.  
  
 `pcMap`  
 [out] Kullanılabilir cor_debug_ıl_to_natıve_map yapıları toplam sayısı.  
  
 `map`  
 [out] Bir dizi `COR_DEBUG_IL_TO_NATIVE_MAP` yapıları, her biri uzaklıkları belirtir. Sonra `GetILToNativeMapping` yöntemi döndüğünde, `map` bazılarını veya tümünü içerecektir `COR_DEBUG_IL_TO_NATIVE_MAP` yapıları.  
  
## <a name="remarks"></a>Açıklamalar  
 `GetILToNativeMapping` Yöntemi, bir dizi döndürür `COR_DEBUG_IL_TO_NATIVE_MAP` yapıları. Belirli aralıkları yerel yönergeleri için kod (örneğin, giriş) özel bölgeleri karşılık gelen iletmek için bir giriş dizisinde olabilir, `ilOffset` alan için bir değer kümesi [Cordebugıltonativemappingtypes](../../../../docs/framework/unmanaged-api/debugging/cordebugiltonativemappingtypes-enumeration.md) sabit listesi.  
  
 Sonra `GetILToNativeMapping` döndürür, doğrulamalısınız `map` arabellek tüm içerecek şekilde büyük `COR_DEBUG_IL_TO_NATIVE_MAP` yapıları. Bunu yapmak için değeri ile karşılaştırmak `cMap` değeriyle `pcMap` parametresi. Varsa `pcMap` boyutu tarafından çarpıldığında değeri bir `COR_DEBUG_IL_TO_NATIVE_MAP` yapısı, büyüktür `cMap`, daha büyük bir ayırma `map` arabellek, güncelleştirme `cMap` yeni, daha büyük bir boyut ve çağrı `GetILToNativeMapping` yeniden.  
  
 Alternatif olarak, ilk çağırabilirsiniz `GetILToNativeMapping` sıfır uzunluklu ile `map` arabellek doğru arabellek boyutu elde edilir. Arabellek boyutu döndürülen değere ayarlayabilirsiniz `pcMap` ve çağrı `GetILToNativeMapping` yeniden.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** CorProf.idl, CorProf.h  
  
 **Kitaplığı:** CorGuids.lib  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [ICorProfilerInfo Arabirimi](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [GetILToNativeMapping2 Yöntemi](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-getiltonativemapping2-method.md)
- [Profil Oluşturma Arabirimleri](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [Profil Oluşturma](../../../../docs/framework/unmanaged-api/profiling/index.md)
