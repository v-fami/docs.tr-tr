---
title: <add> / <issuerChannelBehaviors>
ms.date: 03/30/2017
ms.assetid: 50710506-e28f-45dd-ab7e-bff6f44173db
ms.openlocfilehash: 5c9937cb6302a194228461f3e2e06ecdf4d43269
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61673621"
---
# <a name="add-of-issuerchannelbehaviors"></a>\<Ekle >, \<issuerChannelBehaviors >

Bir STS ile iletişim kurarken kullanılacak uç nokta davranışı ekler.

> [!NOTE]
> Herhangi bir uç nokta davranışı içeriyorsa bir [ \<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) öğesi, bir özel durum oluşturulur.

\<sistemi. ServiceModel > \
\<davranışlar > \
endpointBehaviors bölümü \<davranışı > \
\<clientCredentials > \
\<IssuedToken > \
\<issuerChannelBehaviors > Element\
\<Ekle >

## <a name="syntax"></a>Sözdizimi

```xml
<add issuerAddress="string"
     behaviorConfiguration="string" />
```

## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler

Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|issuerAddress|İle iletişim kurmak için güvenlik belirteci vericisinin URI.|
|behaviorConfiguration|Aynı yapılandırma dosyasında tanımlanan bir uç nokta davranışı adı.|

### <a name="child-elements"></a>Alt Öğeler

Yok.

### <a name="parent-elements"></a>Üst Öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[\<issuerChannelBehaviors>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuerchannelbehaviors-element.md)|Windows Communication Foundation (WCF) hizmeti belirtilen belirteci Hizmetleri ile iletişim kurarken kullanılacak uç nokta davranışları istemci koleksiyonunu içerir.|

## <a name="remarks"></a>Açıklamalar

`issuerAddress` istemci ile iletişim kurmak istediği güvenlik belirteci hizmeti URI'sini içerir. `behaviorConfiguration` Güvenlik belirteci hizmetlerine verilen belirteçleri almak için Windows Communication Foundation (WCF) tarafından oluşturulan kanallar uygulamanın kullandığı bir uç nokta davranışı işaret eder.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.IssuerChannelBehaviors%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElement>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElementCollection>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential.IssuerChannelBehaviors%2A>
- [Kimlik Doğrulama ile Hizmet Kimliği](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [Güvenlik Davranışları](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [Federasyon ve Verilen Belirteçler](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [Hizmet ve İstemcileri Güvenli Hale Getirme](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [İstemcileri Güvenli Hale Getirme](../../../../../docs/framework/wcf/securing-clients.md)
- [Nasıl yapılır: Federe istemci oluşturma](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [Nasıl yapılır: Yerel yayımlayan yapılandırma](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)
- [Federasyon ve Verilen Belirteçler](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [\<issuerChannelBehaviors>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuerchannelbehaviors-element.md)
