---
title: IMapToken::Map Yöntemi
ms.date: 03/30/2017
api_name:
- IMapToken.Map
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMapToken::Map
helpviewer_keywords:
- IMapToken::Map method [.NET Framework metadata]
- Map method [.NET Framework metadata]
ms.assetid: b9b4bf2f-1098-43d6-9619-a99b4bda1940
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a85dc586b0c08fabdd34c018e82314c9003eeded
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62044908"
---
# <a name="imaptokenmap-method"></a>IMapToken::Map Yöntemi
Meta verileri imza kullanma derlemeler arasında bir ilişki eşler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT Map (  
    [in]  mdToken tkImp,   
    [in]  mdToken tkEmit  
);  
```  
  
## <a name="parameters"></a>Parametreler  
 `tkImp`  
 [in] Alınan kod nesnesini temsil eden meta veri belirteci.  
  
 `tkEmit`  
 [in] Gösterilen kod nesneyi temsil eden meta veri belirteci.  
  
## <a name="remarks"></a>Açıklamalar  
 Belirteci yeniden eşlemeniz birleştirme sırasında ortaya çıktığında, özgün belirteç içeri aktarılan (kaynak) meta verileri kapsamda kapsama alınır ve yeni belirteç yayılan (hedef) meta verileri kapsamda kapsamlıdır.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** COR.h  
  
 **Kitaplığı:** Bir kaynak olarak MsCorEE.dll kullanılan  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [IMapToken Arabirimi](../../../../docs/framework/unmanaged-api/metadata/imaptoken-interface.md)
