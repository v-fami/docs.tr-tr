---
title: GetResolutionScope Metodu
ms.date: 03/30/2017
api_name:
- IALink.GetResolutionScope
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetResolutionScope
helpviewer_keywords:
- GetResolutionScope method
ms.assetid: 5b48ca60-dacd-44b2-9979-4a5122f00812
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6c6d298c84b801b87832c56026b05f647cb5a9dd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789837"
---
# <a name="getresolutionscope-method"></a>GetResolutionScope Metodu
Kapsamı belirli bir türden alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT GetResolutionScope(  
    mdAssembly  AssemblyID,  
    mdToken     FileToken,  
    mdToken     TargetFile,  
    mdToken*    pScope  
) PURE;  
```  
  
## <a name="parameters"></a>Parametreler  
 `AssemblyID`  
 Derleme kimliği.  
  
 `FileToken`  
 Geçirilmesi gereken başvuru dosya.  
  
 `TargetFile`  
 Dosyanın belirteç türü, genellikle alınan tanımlanan [ImportFile yöntemi](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).  
  
 `pScope`  
 Derleme veya modül başvurusu alır.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem başarılı olursa S_OK döndürür.  
  
## <a name="requirements"></a>Gereksinimler  
 ALink.h gerektirir.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [IALink Arabirimi](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [IALink2 Arabirimi](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [ALink API](../../../../docs/framework/unmanaged-api/alink/index.md)
