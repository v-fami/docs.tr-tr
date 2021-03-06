---
title: IReferenceAppId Arabirimi
ms.date: 03/30/2017
api_name:
- IReferenceAppId
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IReferenceAppId
helpviewer_keywords:
- IReferenceAppId interface [.NET Framework fusion]
ms.assetid: 8eb9e565-f358-43ce-900e-a8f8a5aa6cfb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 25733e459423500352595d6be0eee26ef75ca7e2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789694"
---
# <a name="ireferenceappid-interface"></a>IReferenceAppId Arabirimi
Geçerli kapsam içinde bir uygulama için benzersiz tanımlayıcı bir başvuruyu temsil eder.  
  
## <a name="methods"></a>Yöntemler  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|`IReferenceAppId::get_CodeBase`|Bu başvuru uygulaması için kod tanımlayıcısı için bir dize gösterimini bir işaretçi alır `IReferenceAppId`.|  
|`IReferenceAppId::put_CodeBase`|Bu başvuru uygulaması için kod tanımlayıcısı ayarlar `IReferenceAppId`.|  
|`IReferenceAppId::EnumAppPath`|Bir arabirim işaretçisi alır bir `IEnumReferenceIdentity` örneği içeren `IReferenceIdentity` bu üyeleri temsil eden örnekleri `IReferenceAppId`.|  
|`IReferenceAppId::get_SubscriptionId`|Abonelik için bu belirteci tanımlayıcı bir dize gösterimini bir işaretçi alır `IReferenceAppId`.|  
|`IReferenceAppId::put_SubscriptionId`|Bir abonelik için belirteç tanımlayıcısı için ayarlar `IReferenceAppId` belirtilen dize değeri.|  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** Isolation.h  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Fusion Arabirimleri](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [IEnumReferenceIdentity Arabirimi](../../../../docs/framework/unmanaged-api/fusion/ienumreferenceidentity-interface.md)
- [IReferenceIdentity Arabirimi](../../../../docs/framework/unmanaged-api/fusion/ireferenceidentity-interface.md)
