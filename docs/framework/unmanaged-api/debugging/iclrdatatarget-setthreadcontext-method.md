---
title: ICLRDataTarget::SetThreadContext Yöntemi
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.SetThreadContext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::SetThreadContext
helpviewer_keywords:
- SetThreadContext method, ICLRDataTarget interface [.NET Framework debugging]
- ICLRDataTarget::SetThreadContext method [.NET Framework debugging]
ms.assetid: 103c8502-81fe-40d7-9c1e-9008d8fb19e1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d3f98ab65512a380ebd4dc0ecd50e36f94a6d6b5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61698037"
---
# <a name="iclrdatatargetsetthreadcontext-method"></a>ICLRDataTarget::SetThreadContext Yöntemi
Belirtilen iş parçacığının geçerli bağlam hedef işlemde ayarlar. Bu yöntem, ortak dil çalışma zamanı (CLR) veri erişim Hizmetleri tarafından çağrılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT SetThreadContext (  
    [in] ULONG32            threadID,  
    [in] ULONG32            contextSize,  
    [in, size_is(contextSize)]   
         BYTE               *context  
);  
```  
  
## <a name="parameters"></a>Parametreler  
 `threadID`  
 [in] Bir iş parçacığı hedef işlem, işletim sistemi tanımlayıcısı.  
  
 `contextSize`  
 [in] İçerik boyutu.  
  
 `context`  
 [in] Bağlamını içeren bir arabellek için işaretçi.  
  
 Verileri `context` arabellek Win32 biçiminde olacaktır `CONTEXT` yapısı. Bağlam nedenle işlemciye özel kayıt veri belirtir Win32 tanımını `CONTEXT` yapısı işlemci mimarisine bağlıdır. Win32 tanımını WinNT.h üstbilgi dosyasına `CONTEXT` yapısı.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, hata ayıklama uygulamanın yazıcı tarafından uygulanır.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** ClrData.idl, ClrData.h  
  
 **Kitaplığı:** CorGuids.lib  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [ICLRDataTarget Arabirimi](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
