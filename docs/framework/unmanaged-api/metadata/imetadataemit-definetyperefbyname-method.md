---
title: IMetaDataEmit::DefineTypeRefByName Yöntemi
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineTypeRefByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineTypeRefByName
helpviewer_keywords:
- DefineTypeRefByName method [.NET Framework metadata]
- IMetaDataEmit::DefineTypeRefByName method [.NET Framework metadata]
ms.assetid: c30a4ce3-2d3e-411a-98df-e62ac4a5dd50
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 82d81be7a9e0843dfe382767de582f93371acb4c
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64584485"
---
# <a name="imetadataemitdefinetyperefbyname-method"></a>IMetaDataEmit::DefineTypeRefByName Yöntemi
Bir meta veri geçerli kapsamı dışında olan Belirtilen kapsam içinde tanımlanan bir tür için belirteç alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT DefineTypeRefByName (   
    [in]  mdToken     tkResolutionScope,   
    [in]  LPCWSTR     szName,   
    [out] mdTypeRef   *ptr   
);  
```  
  
## <a name="parameters"></a>Parametreler  
 `tkResolutionScope`  
 [in] Çözüm kapsamını belirten belirteç. Aşağıdaki belirteç türlerini geçerlidir:  
  
- `mdModuleRef`, çağıran tanımlanır aynı bütünleştirilmiş kodda tür tanımlı ise.  
  
- `mdAssemblyRef`, bir çağıranın tanımlanır dışındaki bir bütünleştirilmiş kodda tür tanımlı ise.  
  
- `mdTypeRef`, iç içe türü türü ise.  
  
- `mdModule`, türü çağıran tanımlanır aynı modülde tanımlandıysa.  
  
- Türü genel olarak tanımlanmışsa null.  
  
 `szName`  
 [in] Unicode hedef türünün adı.  
  
 `ptr`  
 [out] Bir işaretçi `mdTypeRef` türüne atanan belirteci.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** COR.h  
  
 **Kitaplığı:** Bir kaynak olarak MSCorEE.dll kullanılan  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [IMetaDataEmit Arabirimi](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [IMetaDataEmit2 Arabirimi](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
