---
title: IMetaDataImport::GetInterfaceImplProps Yöntemi
ms.date: 02/25/2019
api_name:
- IMetaDataImport.GetInterfaceImplProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetInterfaceImplProps
helpviewer_keywords:
- IMetaDataImport::GetInterfaceImplProps method [.NET Framework metadata]
- GetInterfaceImpProps method [.NET Framework metadata]
ms.assetid: be3f5985-b1e4-4036-8602-c16e8508d4af
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 76e2ebbd47a5e36a722fce33ba67d7efb4db8675
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61777773"
---
# <a name="imetadataimportgetinterfaceimplprops-method"></a>IMetaDataImport::GetInterfaceImplProps Yöntemi
Meta veri belirteçleri için bir işaretçi alır <xref:System.Type> belirtilen yöntemini uygulayan ve arabirim için bu yöntem bildirir.
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT GetInterfaceImplProps (  
   [in]  mdInterfaceImpl        iiImpl,  
   [out] mdTypeDef              *pClass,  
   [out] mdToken                *ptkIface  
);  
```  
  
## <a name="parameters"></a>Parametreler  
 `iiImpl`  
 [in] Sınıf ve arabirim belirteçleri için döndürülecek yöntemi temsil eden meta veri belirteci.  
  
 `pClass`  
 [out] Yöntemini uygulayan bir sınıfı temsil eden meta veri belirteci.  
  
 `ptkIface`  
 [out] Uygulanan yöntemi tanımlar arabirimi temsil eden meta veri belirteci.  

## <a name="remarks"></a>Açıklamalar

 Değeri elde `iImpl` çağırarak [Enumınterfaceımpls](imetadataimport-enuminterfaceimpls-method.md) yöntemi.
 
 Örneğin, bir sınıf olduğunu varsayalım. bir `mdTypeDef` belirteç 0x02000007 değeri ile eşleşen türleri belirteçleri sahip üç arabirimi uygular: 

- 0x02000003 (TypeDef)
- 0x0100000A (TypeRef)
- 0x0200001C (TypeDef)

Kavramsal olarak, bu bilgileri, bir arabirim uygulaması tablosuna depolanır:

| Satır numarası | Sınıf simgesi | Belirteç arabirimi |
|------------|-------------|-----------------|
| 4          |             |                 |
| 5          | 02000007    | 02000003        |
| 6          | 02000007    | 0100000A        |
| 7          |             |                 |
| 8          | 02000007    | 0200001C        |

Geri çağırırsanız, belirteç bir 4 baytlık değerdir:

- Daha düşük 3 baytlar satır numarasına tutun veya RID.
- Belirteç türü – 0x09 için üst bayt tutar `mdtInterfaceImpl`.

`GetInterfaceImplProps` bilgi tutulan belirteç tarafınıza sıradaki döndürür `iImpl` bağımsız değişken. 
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** COR.h  
  
 **Kitaplığı:** Bir kaynak olarak MsCorEE.dll dahil  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [IMetaDataImport Arabirimi](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2 Arabirimi](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
