---
title: IMetaDataImport::GetMemberProps Metodu
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetMemberProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetMemberProps
helpviewer_keywords:
- IMetaDataImport::GetMemberProps method [.NET Framework metadata]
- GetMemberProps method [.NET Framework metadata]
ms.assetid: 42790918-4142-4938-b8f4-a56979a55846
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 83dec9b6ed3b1e538e0f1b7d13a33b8bdbc1cf54
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61777734"
---
# <a name="imetadataimportgetmemberprops-method"></a>IMetaDataImport::GetMemberProps Metodu
Belirtilen üye tanımı, adını, ikili imzası ve göreli sanal adres dahil olmak üzere, meta verileri içinde depolanan bilgilerini alır <xref:System.Type> belirtilen metaveri belirteci tarafından başvurulan üyesi. Basit bir yardımcı yöntem budur: varsa *mb* bir MethodDef ise **GetMethodProps** ; Aranan *mb* bir fieldDef simgesi ise **GetFieldProps** çağrılır. Bunlar diğer ayrıntılar için bkz. 
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT GetMemberProps (  
   [in]  mdToken           mb,   
   [out] mdTypeDef         *pClass,  
   [out] LPWSTR            szMember,   
   [in]  ULONG             cchMember,   
   [out] ULONG             *pchMember,   
   [out] DWORD             *pdwAttr,  
   [out] PCCOR_SIGNATURE   *ppvSigBlob,   
   [out] ULONG             *pcbSigBlob,   
   [out] ULONG             *pulCodeRVA,   
   [out] DWORD             *pdwImplFlags,   
   [out] DWORD             *pdwCPlusTypeFlag,   
   [out] UVCP_CONSTANT     *ppValue,  
   [out] ULONG             *pcchValue  
);  
```  
  
## <a name="parameters"></a>Parametreler  
 `mb`  
 [in] Belirteç ilişkili meta verileri almak için bir üyeye başvuruda bulunuyor.  
  
 `pClass`  
 [out] Üye sınıfı temsil eden meta veri belirteci için bir işaretçi.  
  
 `szMember`  
 [out] Üyenin adı.  
  
 `cchMember`  
 [in] Geniş karakter cinsinden boyutu `szMember` arabellek.  
  
 `pchMember`  
 [out] Döndürülen adının geniş karakter cinsinden boyutu.  
  
 `pdwAttr`  
 [out] Üyeye uygulanan tüm bayrak değerleri.  
  
 `ppvSigBlob`  
 [out] İkili meta veri imzası üyenin bir işaretçisi.  
  
 `pcbSigBlob`  
 [out] Bayt cinsinden boyutu `ppvSigBlob`.  
  
 `pulCodeRVA`  
 [out] Göreli sanal adres üyenin bir işaretçisi.  
  
 `pdwImplFlags`  
 [out] Üye ile ilişkili tüm yöntemi uygulama bayrakları.  
  
 `pdwCPlusTypeFlag`  
 [out] İşaretler bayrak bir <xref:System.ValueType>. Biridir `ELEMENT_TYPE_*` değerleri.
  
 `ppValue`  
 [out] Bu üye tarafından döndürülen bir sabit dize değeri.  
  
 `pcchValue`  
 [out] Karakter cinsinden boyutu `ppValue`, ya da sıfır `ppValue` bir dize tutmaz.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** COR.h  
  
 **Kitaplığı:** Bir kaynak olarak MsCorEE.dll dahil  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [IMetaDataImport Arabirimi](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2 Arabirimi](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
