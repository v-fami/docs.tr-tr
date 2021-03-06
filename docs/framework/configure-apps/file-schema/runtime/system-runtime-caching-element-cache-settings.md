---
title: <system.runtime.caching> Öğesi (Önbellek Ayarları)
ms.date: 03/30/2017
helpviewer_keywords:
- <system.runtime.caching> element
- caching [.NET Framework], configuration
- system.runtime.caching element
ms.assetid: 9b44daee-874a-4bd1-954e-83bf53565590
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 03a17e8f30c15e98a350ef558cc1cb6ddf65cade
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65584514"
---
# <a name="systemruntimecaching-element-cache-settings"></a>\<System.Runtime.Caching > öğesi (önbellek ayarları)
Bellekteki varsayılan yapılandırmasını sağlar <xref:System.Runtime.Caching.ObjectCache> uygulaması aracılığıyla `memoryCache` yapılandırma dosyasında giriş.  
  
 \<Yapılandırma >  
\<System.Runtime.Caching >  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<system.runtime.caching >  
   <!-- child elements -->  
</system.runtime.caching >  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
 `None`  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[\<memoryCache>](../../../../../docs/framework/configure-apps/file-schema/runtime/memorycache-element-cache-settings.md)|Temel alan bir önbellek yapılandırmak için kullanılan bir öğe tanımlar <xref:System.Runtime.Caching.MemoryCache> sınıfı.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[\<Yapılandırma >](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|Her yapılandırma dosyasında ortak dil çalışma zamanı ve .NET Framework uygulamaları tarafından kullanılan kök öğesini belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu ad alanındaki sınıflar üzerinde ASP.NET, ancak bir bağımlılık benzer önbelleğe alma özelliklerini kullanabilmeniz için bir yol sağlar `System.Web` derleme. Daha fazla bilgi için [.NET Framework uygulamalarında önbelleğe alma](../../../../../docs/framework/performance/caching-in-net-framework-applications.md).  
  
> [!NOTE]
>  Çıktı işlevleri ve türleri önbelleğe alma <xref:System.Runtime.Caching> ad alanı yeni [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)].  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, temel alan bir önbellek yapılandırma işlemi gösterilmektedir <xref:System.Runtime.Caching.MemoryCache> sınıfı. Örneğin, bir örneğini yapılandırma işlemi gösterilmektedir `namedCaches` önbellek girişi. Önbellek adı ayarlayarak varsayılan önbellek girişi adına ayarlanır `name` "varsayılan" özniteliği.  
  
 `cacheMemoryLimitMegabytes` Özniteliği ve `physicalMemoryPercentage` öznitelik sıfır olarak ayarlanır. Bu öznitelik sıfır olarak ayarlandığında <xref:System.Runtime.Caching.MemoryCache> otomatik boyutlandırma buluşsal yöntemler, varsayılan olarak kullanılır. Önbellek uygulaması, iki dakikada mutlak ve yüzde tabanlı bellek sınırlarını karşı geçerli bellek yükü karşılaştırmanız gerekir.  
  
```xml  
<configuration>  
  <system.runtime.caching>  
    <memoryCache>  
      <namedCaches>  
          <add name="default"   
               cacheMemoryLimitMegabytes="0"   
               physicalMemoryLimitPercentage="0"  
               pollingInterval="00:02:00" />  
      </namedCaches>  
    </memoryCache>  
  </system.runtime.caching>  
</configuration>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.

- [\<memoryCache > öğesi (önbellek ayarları)](../../../../../docs/framework/configure-apps/file-schema/runtime/memorycache-element-cache-settings.md)
