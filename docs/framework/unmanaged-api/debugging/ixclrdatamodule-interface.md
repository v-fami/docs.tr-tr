---
title: IXCLRDataModule arabirimi
ms.date: 01/16/2019
api.name:
- IXCLRDataModule Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule Interface
helpviewer.keywords:
- IXCLRDataModule Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: c8d6e36687fd43bbc59304eee64dd42eb78101e3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54676529"
---
# <a name="ixclrdatamodule-interface"></a>IXCLRDataModule arabirimi

Yüklenen bir modülün hakkında bilgi sorgulamak için yöntemler sağlar.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a>Yöntemler

| Yöntem                                                                                                                                | Açıklama                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [GetMethodDefinitionByToken](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getmethoddefinitionbytoken-method.md) | Belirli bir metaveri belirteci için karşılık gelen yöntem tanımını alır. |
| [İstek](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-request-method.md)                                       | Modülün verilerle verilen arabelleği doldurmak için istek sayısı.       |
| [GetVersionId](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getversionid-method.md)                             | Modülün sürüm kimliğini alır.                                       |

## <a name="remarks"></a>Açıklamalar

Bu arabirim, çalışma zamanı içinde yer alan ve herhangi bir üst bilgiler veya kitaplık dosyaları gösterilmez. Ancak, bu, türetilen bir COM arabirimidir `IUnknown` GUID'e sahip `88E32849-0A0A-4cb0-9022-7CD2E9E139E2` normal COM mekanizmalar aracılığıyla edinilebilir.

## <a name="requirements"></a>Gereksinimler

**Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
**Üst bilgi:** Hiçbiri  
**Kitaplığı:** Hiçbiri  
**.NET framework sürümleri:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Ayrıca bkz.

- [Hata Ayıklama](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [Hata Ayıklama Arabirimleri](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
