---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset Yöntemi
ms.date: 03/30/2017
ms.assetid: 92af7896-2201-408d-8b1b-23e28001eeac
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 923c85a9dff11753a338fcfd3673d3590fca607a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61940133"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinecatchhandleriloffset-method"></a>ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset Yöntemi
IL uzaklığı bir zaman uyumsuz yöntem sarmalayan derleyicinin ürettiği catch işleyicisi için ayarlar.  
  
 Oluşturulan yakalama IL uzaklığı, hata ayıklayıcı tarafından bir kullanıcı kodu yöntemi ortaya çıkabilecek olsa bile, kullanıcı olmayan kod gibi yakalama işlemek için kullanılır. Özellikle, yanıt olarak kullanılır bir **CatchHandlerFound** özel durum olayı.  
  
## <a name="syntax"></a>Sözdizimi  
  
```idl  
HRESULT DefineCatchHandlerILOffset(    [in] ULONG32 catchHandlerOffset);  
```  
  
## <a name="parameters"></a>Parametreler  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`catchHandlerOffset`||  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `HRESULT`.  
  
## <a name="requirements"></a>Gereksinimler  
 **Üst bilgi:** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Ayrıca bkz.

- [ISymUnmanagedAsyncMethodPropertiesWriter Arabirimi](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
