---
title: ICorDebugValue3::GetSize64 Yöntemi
ms.date: 03/30/2017
api_name:
- ICorDebugValue3::GetSize64
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue3::GetSize64
helpviewer_keywords:
- GetSize64 method, ICorDebugValue3 interface [.NET Framework debugging]
- ICorDebugValue3::GetSize64 method [.NET Framework debugging]
ms.assetid: fee56a29-3154-4192-958d-71da2ced3740
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7c0b45e08f7b88d9374023f95c6e3e22139c8949
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61768933"
---
# <a name="icordebugvalue3getsize64-method"></a>ICorDebugValue3::GetSize64 Yöntemi
Bu bayt cinsinden boyutunu alır [Icordebugvalue3](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md) nesne.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT GetSize64(  
    [out] ULONG64 *pSize  
);  
```  
  
## <a name="parameters"></a>Parametreler  
 pSize  
 [out] Bu nesnenin bayt cinsinden boyutu için bir işaretçi.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu değer türü bir başvuru türü ise, bu yöntem, nesnenin boyutu yerine işaretçinin boyutu döndürür.  
  
 `ICorDebugValue3::GetSize` Yönteminden farklıdır [Icordebugvalue::getsize](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getsize-method.md) yöntemi, çıkış parametresinin türü. İçinde [Icordebugvalue::getsize](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getsize-method.md), çıkış parametresi olan bir `ULONG32`; `ICorDebugValue3::GetSize`, bunun bir `ULONG64`. Böylece [Icordebugvalue3](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md) boyutu 2 GB'ı aşan diziler bildirmek için arabirim.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** CorDebug.idl, CorDebug.h  
  
 **Kitaplığı:** CorGuids.lib  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [ICorDebugValue3 Arabirimi](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md)
- [Hata Ayıklama Arabirimleri](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
