---
title: <endpointExtensions>
ms.date: 03/30/2017
ms.assetid: 33396e0a-1fae-4616-b822-923584eebfd1
ms.openlocfilehash: 12ac8d9a7b0ed584fb1308e56d197a03b1c53e51
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61700884"
---
# <a name="endpointextensions"></a>\<endpointExtensions >
Bu bölümde, bir makine uzantıları bölümünde yeni bir standart uç nokta kaydeder veya uygulama yapılandırma dosyası. Kullanarak, bu koleksiyona bir standart uç nokta ekleyebilirsiniz `add` anahtar sözcüğü ve ayarı `type` uç nokta türü için bir öğenin özniteliği hem de `name` öznitelik standart bitiş noktası adını.  
  
 Aşağıdaki örnekte `add` öğesi hem de `name` özniteliği için bir standart uç nokta eklemek için `<endpointExtensions>` yapılandırma dosyasının.  
  
```xml  
<system.serviceModel>
  <extensions>
    <endpointExtensions>
      <add name="udpDiscoveryEndpoint"
           type="System.Discovery.UdpEndpointCollectionElement, System.Discovery.dll, Version=1.0.0.0, Culture=neutral, PublicKeyToken=ffffffffffffffff"/>
    </endpointExtensions>
  </extensions>
</system.serviceModel>
```  
  
 Standart uç nokta kaydedildikten sonra aşağıdaki örnekte gösterildiği gibi kullanabilirsiniz. İçinde [ \<uç noktası >](../../../../../docs/framework/configure-apps/file-schema/wcf/endpoint-element.md) öğesi `kind` özniteliği belirtir, kayıtlı standart uç nokta türü `<endpointExtensions>` bölümü. `endpointConfiguration` Özniteliği aynı olacaktır `name` standart uç nokta yapılandırma öğesinin özniteliği `<standardEndpoints>` bölümü.  
  
```xml  
<system.serviceModel>
  <services>
    <service name="Service1">
      <endpoint kind="udpDiscoveryEndpoint"
                endpointConfiguration="udpConfig" />
    </service>
  </services>
  <standardEndpoints>
    <udpDiscoveryEndpoint>
      <standardEndpoint name="udpConfig"
                        multicastAddress="soap.udp://239.255.255.250:3703"
                        ... />
    </udpDiscoveryEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
