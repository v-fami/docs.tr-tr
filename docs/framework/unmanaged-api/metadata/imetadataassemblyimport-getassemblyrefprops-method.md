---
title: IMetaDataAssemblyImport::GetAssemblyRefProps Yöntemi
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.GetAssemblyRefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::GetAssemblyRefProps
helpviewer_keywords:
- IMetaDataAssemblyImport::GetAssemblyRefProps method [.NET Framework metadata]
- GetAssemblyRefProps method [.NET Framework metadata]
ms.assetid: 5c6b7fb4-cbca-4479-b650-ab9a99732ea0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e6c550ff7af2dda8bc06afd771024fe290339904
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59089789"
---
# <a name="imetadataassemblyimportgetassemblyrefprops-method"></a>IMetaDataAssemblyImport::GetAssemblyRefProps Yöntemi
Belirtilen meta veri imzası olan derleme başvurusu için özellikler kümesini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT GetAssemblyRefProps (  
    [in]  mdAssemblyRef        mdar,   
    [out] const void          **ppbPublicKeyOrToken,   
    [out] ULONG                *pcbPublicKeyOrToken,   
    [out] LPWSTR               szName,   
    [in]  ULONG                cchName,   
    [out] ULONG                *pchName,   
    [out] ASSEMBLYMETADATA     *pMetaData,   
    [out] const void           **ppbHashValue,   
    [out] ULONG                *pcbHashValue,   
    [out] DWORD                *pdwAssemblyRefFlags  
);  
```  
  
## <a name="parameters"></a>Parametreler  
 `mdar`  
 [in] `mdAssemblyRef` Derleme başvurusu özellikleri alınacağı temsil eden bir meta veri belirteci.  
  
 `ppbPublicKeyOrToken`  
 [out] Ortak anahtarı veya meta veri belirteci için bir işaretçi.  
  
 `pcbPublicKeyOrToken`  
 [out] Döndürülen bir ortak anahtar veya belirteç bayt sayısı.  
  
 `szName`  
 [out] Derlemenin basit adını.  
  
 `cchName`  
 [in] Geniş karakter, boyutunu, `szName`.  
  
 `pchName`  
 [out] Gerçekte döndürülen geniş karakter sayısı için bir işaretçi `szName`.  
  
 `pMetaData`  
 [out] Derleme meta verileri içeren bir ASSEMBLYMETADATA yapısı işaretçisi.  
  
 `ppbHashValue`  
 [out] Karma değeri için bir işaretçi. Bu, SHA-1 algoritmasını kullanan karma `PublicKey` arfFullOriginator bayrak sürece, başvurulan derleme özelliği [AssemblyRefFlags](../../../../docs/framework/unmanaged-api/metadata/assemblyrefflags-enumeration.md) numaralandırma ayarı.  
  
 `pcbHashValue`  
 [out] Döndürülen karma değeri geniş karakter sayısı.  
  
 `pdwAssemblyRefFlags`  
 [out] Bir derlemeye uygulanan meta verileri açıklayan bayrakları için bir işaretçi. Bir veya daha fazla flags değeri birleşimidir [CorAssemblyFlags](../../../../docs/framework/unmanaged-api/metadata/corassemblyflags-enumeration.md) değerleri.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bu yöntem başarılı olursa başarılıysa S_OK döndürür; Aksi takdirde wınerror üstbilgi dosyasında tanımlanan hata kodlarından birini döndürür.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** COR.h  
  
 **Kitaplığı:** Bir kaynak olarak MsCorEE.dll kullanılan  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [IMetaDataAssemblyImport Arabirimi](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
