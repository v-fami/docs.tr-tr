---
title: IMetaDataImport::EnumFieldsWithName Yöntemi
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumFieldsWithName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumFieldsWithName
helpviewer_keywords:
- IMetaDataImport::EnumFieldsWithName method [.NET Framework metadata]
- EnumFieldsWithName method [.NET Framework metadata]
ms.assetid: 42145e8d-000f-4d0b-ae43-c08201190fa2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cf624695136a9397937f05b28dec18493c8e12d7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62042711"
---
# <a name="imetadataimportenumfieldswithname-method"></a>IMetaDataImport::EnumFieldsWithName Yöntemi
Belirtilen ada sahip belirtilen türün fieldDef simgesi belirteçleri numaralandırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT EnumFieldsWithName (  
   [in, out] HCORENUM    *phEnum,   
   [in]  mdTypeDef       cl,   
   [in]  LPCWSTR         szName,   
   [out] mdFieldDef      rFields[],   
   [in]  ULONG           cMax,   
   [out] ULONG           *pcTokens   
);  
```  
  
## <a name="parameters"></a>Parametreler  
 `phEnum`  
 [out içinde] Numaralandırıcı bir işaretçi.  
  
 `cl`  
 [in] Numaralandırılacak alanları olan türde bir belirteç.  
  
 `szName`  
 [in] Numaralandırma kapsamını sınırlayan alan adı.  
  
 `rFields`  
 [out] Dizi fieldDef simgesi simgeleri depolamak için kullanılır.  
  
 `cMax`  
 [in] En büyük boyutunu `rFields` dizisi.  
  
 `pcTokens`  
 [out] Döndürülen fieldDef simgesi belirteçleri gerçek sayısını `rFields`.  
  
## <a name="remarks"></a>Açıklamalar  
 Farklı [Imetadataımport::enumfields](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enumfields-method.md), `EnumFieldsWithName` belirtilen ada sahip olmayan tüm alan belirteçleri atar.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
|HRESULT|Açıklama|  
|-------------|-----------------|  
|`S_OK`|`EnumFieldsWithName` başarıyla döndürüldü.|  
|`S_FALSE`|Numaralandırılacak alan yok. Bu durumda, `pcTokens` sıfırdır.|  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** COR.h  
  
 **Kitaplığı:** Bir kaynak olarak MsCorEE.dll dahil  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [IMetaDataImport Arabirimi](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2 Arabirimi](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
