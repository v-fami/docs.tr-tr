---
title: ICorDebugChain::GetCaller Metodu
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetCaller
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetCaller
helpviewer_keywords:
- ICorDebugChain::GetCaller method [.NET Framework debugging]
- GetCaller method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: d0b8ab4b-d7d2-4fa0-945f-3d2b87e7e991
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fd65de77209f5a981c0a4c291f8573a61cf6335b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61645285"
---
# <a name="icordebugchaingetcaller-method"></a>ICorDebugChain::GetCaller Metodu
Bu zincir denir zinciri alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT GetCaller (  
    [out] ICorDebugChain      **ppChain  
);  
```  
  
## <a name="parameters"></a>Parametreler  
 `ppChain`  
 [out] Çağrı zincirini temsil eden bir Icordebugchain nesnenin adresi için bir işaretçi.  
  
 (Bu zincir veya hata ayıklayıcı çağrı yığınını başlatılmış durumda olurdu gibi) Bu zincir kendiliğinden çağrıldı, `ppChain` null olacaktır.  
  
## <a name="remarks"></a>Açıklamalar  
 Çağrı zincirinin çağrı iş parçacıkları arasında sıralanmış farklı bir iş parçacığı üzerinde olabilir.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** CorDebug.idl, CorDebug.h  
  
 **Kitaplığı:** CorGuids.lib  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
