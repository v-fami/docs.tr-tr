---
title: ICorProfilerCallback::RemotingServerReceivingMessage Yöntemi
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingServerReceivingMessage
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingServerReceivingMessage
helpviewer_keywords:
- ICorProfilerCallback::RemotingServerReceivingMessage method [.NET Framework profiling]
- RemotingServerReceivingMessage method [.NET Framework profiling]
ms.assetid: 5604d21f-e6b7-490e-b469-42122a7568e1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ec6f7cf8c70292d586e58b5b6d8251aa4700dbac
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64662894"
---
# <a name="icorprofilercallbackremotingserverreceivingmessage-method"></a>ICorProfilerCallback::RemotingServerReceivingMessage Yöntemi
Profil Oluşturucu işlemin bir uzak yöntem çağırma veya etkinleştirme isteği aldı bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT RemotingClientSendingMessage(  
    [in] GUID *pCookie,  
    [in] BOOL fIsAsync);  
```  
  
## <a name="parameters"></a>Parametreler  
 `pCookie`  
 [in] Sağlanan değer karşılık gelecek bir değerle [Icorprofilercallback::remotingclientsendingmessage](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientsendingmessage-method.md) Bu koşullar altında:  
  
- Uzaktan iletişim GUID tanımlama bilgilerinin etkin olur.  
  
- Kanal ileti iletilirken başarılı olur.  
  
- GUID tanımlama bilgileri istemci tarafı işlemini üzerinde etkindir.  
  
 Bu, uzak hizmet çağrıları ve bir mantıksal çağrı yığını oluşturulmasını kolay eşlemeye izin verir.  
  
 `fIsAsync`  
 [in] Bir değer `true` çağrısı ise, zaman uyumsuz; Aksi takdirde `false`.  
  
## <a name="remarks"></a>Açıklamalar  
 İleti isteği zaman uyumsuz olması durumunda, isteği herhangi bir rastgele iş parçacığı tarafından hizmet verebilir.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** CorProf.idl, CorProf.h  
  
 **Kitaplığı:** CorGuids.lib  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [ICorProfilerCallback Arabirimi](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
