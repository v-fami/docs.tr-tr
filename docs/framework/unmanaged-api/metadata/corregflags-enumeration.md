---
title: CorRegFlags Numaralandırması
ms.date: 03/30/2017
api_name:
- CorRegFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorRegFlags
helpviewer_keywords:
- CorRegFlags enumeration [.NET Framework metadata]
ms.assetid: 8d3080ee-39fe-4c57-8950-51323632d045
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: eb6b303fa7569712c854e8dc4e7513d8608e2519
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62045363"
---
# <a name="corregflags-enumeration"></a>CorRegFlags Numaralandırması
Bir modül veya bileşik görüntüsü yüklerken kayıt için kullanılan bayrak değerleri sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
typedef enum   
{  
    regNoCopy  = 0x00000001,  
    regConfig  = 0x00000002,  
    regHasRefs = 0x00000004  
} CorRegFlags;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Açıklama|  
|------------|-----------------|  
|`regNoCopy`|Dosyaları hedefe kopyalanmaması gereken olduğunu belirtir.|  
|`regConfig`|Modülün veya bileşik bir yapılandırma olduğunu belirtir.|  
|`regHasRefs`|Modülün veya bileşik sınıf başvuruları sahip olduğunu belirtir.|  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** COR.h  
  
 **Kitaplığı:** Bir kaynak olarak MsCorEE.dll dahil  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Meta Veri Sabit Listeleri](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
