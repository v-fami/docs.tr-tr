---
title: IMetaDataImport2::EnumGenericParams Yöntemi
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.EnumGenericParams
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::EnumGenericParams
helpviewer_keywords:
- EnumGenericParams method [.NET Framework metadata]
- IMetaDataImport2::EnumGenericParams method [.NET Framework metadata]
ms.assetid: b50488a5-3cf0-483c-82dc-2892a3ec61ac
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7edd2eeafcce6a22c3256d0684a9c4f961b34002
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049901"
---
# <a name="imetadataimport2enumgenericparams-method"></a>IMetaDataImport2::EnumGenericParams Yöntemi
Bir numaralandırıcı genel parametre belirteçleri belirtilen TypeDef veya MethodDef ilişkili bir dizisi için belirteç alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT EnumGenericParams (  
   [in, out] HCORENUM     *phEnum,   
   [in]  mdToken          tk,  
   [out] mdGenericParam   rGenericParams[],   
   [in]  ULONG            cMax,   
   [out] ULONG            *pcGenericParams  
);  
```  
  
## <a name="parameters"></a>Parametreler  
 `phEnum`  
 [out içinde] Numaralandırıcı bir işaretçi.  
  
 `tk`  
 [in] Numaralandırılacak genel parametreleri olan TypeDef veya MethodDef belirteç.  
  
 `rGenericParams`  
 [out] Numaralandırılacak genel parametreler dizisi.  
  
 `cMax`  
 [in] İstenen sayısı yerleştirmek için belirteçleri `rGenericParams`.  
  
 `pcGenericParams`  
 [out] Döndürülen belirteç sayısı yerleştirilen `rGenericParams`.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
|HRESULT|Açıklama|  
|-------------|-----------------|  
|`S_OK`|`EnumGenericParams` başarıyla döndürüldü.|  
|`S_FALSE`|`phEnum` üye öğe yok. Bu durumda, `pcGenericParams` 0 (sıfır) olarak ayarlayın.|  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** COR.h  
  
 **Kitaplığı:** Bir kaynak olarak MsCorEE.dll kullanılan  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [IMetaDataImport2 Arabirimi](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
- [IMetaDataImport Arabirimi](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
