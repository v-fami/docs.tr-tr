---
title: <net.pipe>
ms.date: 03/30/2017
ms.assetid: 6a0f0318-f8f6-466c-9fae-199d7274a82e
ms.openlocfilehash: 885cfad7be42f7c48b4c061f3293d667eb5d4ad8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772352"
---
# <a name="netpipe"></a>\<NET.pipe >
Adlandırılmış kanal etkinleştirme adlandırılmış kanal bağlantısının yaşam yönetir ve Adlandırılmış Kanallar üzerinden erişen aktivasyon isteklerini işleyen hizmeti için yapılandırma ayarlarını belirtir.  
  
 \<system.serviceModel.activation>  
\<NET.pipe >  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<configuration>
  <system.serviceModel.activation>
    <net.pipe maxPendingAccepts="Integer"
              maxPendingConnections="Integer"
              receiveTimeout="TimeSpan">
      <allowAccounts>
        <!-- LocalSystem account -->
        <add securityIdentifier="S-1-5-18" />
        <!-- LocalService account -->
        <add securityIdentifier="S-1-5-19" />
        <!-- Administrators account -->
        <add securityIdentifier="S-1-5-20" />
        <!-- Network Service account -->
        <add securityIdentifier="S-1-5-32-544" />
        <!-- IIS_IUSRS account (Vista only) -->
        <add securityIdentifier="S-1-5-32-568" />
      </allowAccounts>
    </net.pipe>
  </system.serviceModel.activation>
</configuration>
```  
  
## <a name="type"></a>Tür  
 `Type`  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`maxPendingAccepts`|Hizmetler için olan uç noktaları en fazla bekleyen eşzamanlı kabul iş parçacığı belirten bir tamsayı. Varsayılan değer 2'dir.|  
|`maxPendingConnections`|Gönderme için bekleyebileceği bağlantı maksimum sayısını belirten bir tamsayı. Varsayılan değer 100'dür.|  
|`receiveTimeout`|A <xref:System.TimeSpan> ve çerçeveleme verilerini okumak ve altı çizili bağlantılardan bağlantı dağıtımını gerçekleştirmek için zaman aşımını belirtir. Varsayılan değer "00: 00:10"|  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[\<allowAccounts >](../../../../../docs/framework/configure-apps/file-schema/wcf/allowaccounts.md)|Bir koleksiyon içeren yapılandırma öğelerinin bir `securityIdentifier` barındıran WCF hizmetleri ve Paylaşım Hizmeti bağlantı erişim izni verilen işlemleri için kullanıcı hesabı belirtmek için özniteliği.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[\<system.serviceModel.activation>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel-activation.md)|Dinleyici işlem SMSvcHost.exe için yapılandırma ayarlarını içerir.|  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.ServiceModel.Activation.Configuration.NetPipeSection>
