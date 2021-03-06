---
title: LoggingLevelEnum Numaralandırması
ms.date: 03/30/2017
api_name:
- LoggingLevelEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- LoggingLevelEnum
helpviewer_keywords:
- LoggingLevelEnum enumeration [.NET Framework debugging]
ms.assetid: 09daac08-005a-46b2-beab-408d0820c5e5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2fe8e1355382273a681e927897f4a8ff5814b8de
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61765433"
---
# <a name="logginglevelenum-enumeration"></a>LoggingLevelEnum Numaralandırması
Yönetilen iş parçacığı bir olayı günlüğe kaydettiğinde, olay günlüğüne yazılan açıklayıcı bir iletisi önem derecesi düzeyini gösterir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
typedef enum LoggingLevelEnum {  
    LTraceLevel0 = 0,  
    LTraceLevel1,  
    LTraceLevel2,  
    LTraceLevel3,  
    LTraceLevel4,  
    LStatusLevel0 = 20,  
    LStatusLevel1,  
    LStatusLevel2,  
    LStatusLevel3,  
    LStatusLevel4,  
    LWarningLevel = 40,  
    LErrorLevel = 50,  
    LPanicLevel = 100  
} LoggingLevelEnum;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Açıklama|  
|------------|-----------------|  
|`LTraceLevel0`|İleti izleme düzeyi 0 ' dir.|  
|`LTraceLevel1`|İleti izleme düzeyini 1 ' dir.|  
|`LTraceLevel2`|İleti izleme düzeyini 2 ' dir.|  
|`LTraceLevel3`|İleti izleme düzeyini 3 ' dir.|  
|`LTraceLevel4`|İzleme düzeyi 4 iletisidir.|  
|`LStatusLevel0`|İleti durumu düzeyi 0 ' dir.|  
|`LStatusLevel1`|İleti durumu düzeyi 1 ' dir.|  
|`LStatusLevel2`|İleti durumu düzeyi 2 ' dir.|  
|`LStatusLevel3`|İleti durumu düzeyi 3 ' dir.|  
|`LStatusLevel4`|İleti durumu düzeyi 4 ' dir.|  
|`LWarningLevel`|İleti bir uyarı düzeyidir.|  
|`LErrorLevel`|İleti bir hata düzeyidir.|  
|`LPanicLevel`|İleti Panik düzeyidir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Ortak dil çalışma zamanı (CLR) çağıran [Icordebugmanagedcallback::LogMessage](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-logmessage-method.md) yönetilen iş parçacığı günlüğe bir olay, hata ayıklayıcı bildirmek için yöntemi. CLR değerini geçirir `LoggingLevelEnum` yönetilen iş parçacığı olay günlüğüne yazdığı ileti önem düzeyini belirtmek için sabit listesi.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** Bkz: [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Üst bilgi:** CorDebug.idl, CorDebug.h  
  
 **Kitaplığı:** CorGuids.lib  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Diagnostics.EventLog>
- [Hata Ayıklama Sabit Listeleri](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
