---
title: <add> / <protocolMapping>
ms.date: 03/30/2017
ms.assetid: 08e62249-1641-41d1-91b1-66d7b46244e4
ms.openlocfilehash: 85d09c920de2ca1ab4971551ff98ea58c4492f44
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704498"
---
# <a name="add-of-protocolmapping"></a>\<Ekle >, \<protocolMapping >
Taşıma protokol şeması (örneğin, http, net.tcp, net.pipe, vb.) ve Windows Communication Foundation (WCF) bağlaması arasında varsayılan protokol eşleşmelerinin temsil eder. Varsayılan uç noktalar çalışma zamanında oluştururken, WCF yapılandırılmış eşlemelerin arar ve hangi belirli bir için kullanılacak bağlama adresine göre karar verir.  
  
 \<system.serviceModel>  
\<protocolMapping >  
\<Ekle >  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<protocolMapping>
  <add binding="String"
       bindingConfiguration="String"
       scheme="http/net.msmq/net.pipe/net.tcp" />
</protocolMapping>
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|bağlama|Varsayılan uç nokta oluşturma sırasında bir uç nokta için kullanılacak bağlama türünü belirten bir dize.|  
|bindingConfiguration|Başvurulacak bağlama yapılandırma bölümünün adını belirten dize.|  
|düzen|Varsayılan uç nokta için kullanılacak taşıma protokol şeması.|  
  
### <a name="child-elements"></a>Alt Öğeler  
 Yok.  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[\<protocolMapping >](../../../../../docs/framework/configure-apps/file-schema/wcf/protocolmapping.md)|Taşıma protokol şemaları (örn., http, net.tcp, net.pipe, vb.) ve Windows Communication Foundation (WCF) bağlamaları arasında varsayılan protokol eşlemeleri tanımlayan bir yapılandırma bölümünü temsil eder.|  
  
## <a name="example"></a>Örnek  
 Aşağıdaki yapılandırma örnek machine.config dosyasında varsayılan protokol eşleşmelerinin gösterir. Machine.config dosyasının değiştirerek bu varsayılan eşleme makine düzeyinde geçersiz kılabilirsiniz. Veya yalnızca bir uygulama kapsamında geçersiz kılmak istiyorsanız, bu bölümde, uygulama yapılandırma dosyasında geçersiz kılmak ve eşlemeyi tek protokol şemaları için değiştirin.  
  
```xml  
<protocolMapping>
  <add scheme="http"
       binding="basicHttpBinding" />
  <add scheme="net.tcp"
       binding="netTcpBinding" />
  <add scheme="net.pipe"
       binding="netNamedPipeBinding" />
  <add scheme="net.msmq"
       binding="netMsmqBinding" />
</protocolMapping>
```  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.ServiceModel.Configuration.ProtocolMappingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Configuration.ProtocolMappingElement?displayProperty=nameWithType>
