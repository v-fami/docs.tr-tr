---
title: <message> / <basicHttpBinding>
ms.date: 03/30/2017
ms.assetid: 51cdd329-6461-471a-8747-56c2299b61e5
ms.openlocfilehash: 746acd91074863029211a1ca2584743c464c9ce1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61768985"
---
# <a name="message-of-basichttpbinding"></a>\<İleti >, \<basicHttpBinding >
İleti düzeyi güvenliği ayarlarını tanımlar [ \<basicHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).  
  
 \<system.ServiceModel>  
\<bağlamaları >  
\<basicHttpBinding >  
\<bağlama >  
\<Güvenlik >  
\<İleti >  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
         clientCredentialType="UserName/Certificate" />
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|algorithmSuite|İleti şifreleme ve anahtar-wrap algoritmaları ayarlar. Bu öznitelik türünde <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>, algoritmalar ve anahtar boyutları belirtir. Bu algoritmalar, güvenlik ilkesi dili (WS-SecurityPolicy) belirtiminde belirtilen platformlarla eşlenir.<br /><br /> Varsayılan değer `Basic256` şeklindedir.|  
|clientCredentialType|İleti tabanlı güvenlik yöntemi ile bir istemci kimlik doğrulaması yapılırken kullanılacak kimlik bilgisi türünü belirtir. Varsayılan, `UserName` değeridir.|  
  
## <a name="clientcredentialtype-attribute"></a>clientCredentialType özniteliği  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|UserName|-İstemci kimlik doğrulaması için bir kullanıcı adı kimlik bilgisi ile sunucu gerektirir. Bu kimlik bilgilerini kullanarak belirtilmesi gerekiyor [ \<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md).<br />-WCF parola özeti gönderme veya parolaları ve ileti güvenliği için bu anahtarları kullanarak anahtarlar türetme desteklemez. Bu nedenle, WCF, taşıma, kullanıcı adı kimlik bilgileri kullanılırken korunması gerektiğini zorlar. İçin `basicHttpBinding`, bu SSL kanalı ayarlama gerektirir.|  
|Sertifika|Bir sertifika kullanarak sunucuya istemcinin kimliğinin doğrulanmasını gerektirir. İstemci kimlik bilgisi bu durumda kullanarak belirtilmesi gerekiyor [ \<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) ve [ \<clientCertificate >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-servicecredentials.md). Ayrıca, ileti güvenlik modunu kullanırken, istemcinin hizmet sertifikası ile sağlanması gerekir. Hizmet kimlik bilgisi bu durumda kullanarak belirtilmesi gerekiyor <xref:System.ServiceModel.Description.ClientCredentials> sınıfı veya `ClientCredentials` davranış öğesi ve hizmeti belirterek sertifika kullanarak [ \<serviceCertificate >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md).|  
  
### <a name="child-elements"></a>Alt Öğeler  
 Yok.  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[\<Güvenlik >](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-basichttpbinding.md)|İçin güvenlik özelliklerini tanımlar [ \<basicHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md).|  
  
## <a name="example"></a>Örnek  
 Bu örnek basicHttpBinding ve ileti güvenlik kullanan bir uygulamanın nasıl uygulanacağını gösterir. Aşağıdaki yapılandırma örneği bir hizmet için uç nokta tanımı basicHttpBinding belirtir ve adlı bir bağlama yapılandırmasını başvuran `Binding1`. Hizmetin kendisini istemcinin kimliğini doğrulamak için kullandığı sertifika kümesinde `behaviors` yapılandırma dosyasının altında `serviceCredentials` öğesi. İstemcinin hizmete kendi kimliğini doğrulamak için kullandığı sertifikayı uygulandığı doğrulama modu da kümesinde `behaviors` bölümüne `clientCertificate` öğesi.  
  
 Aynı bağlama ve güvenlik ayrıntıları, istemci yapılandırma dosyasında belirtilir.  
  
```xml  
<system.serviceModel>
  <services>
    <service name="Microsoft.ServiceModel.Samples.CalculatorService"
             behaviorConfiguration="CalculatorServiceBehavior">
      <host>
        <baseAddresses>
          <add baseAddress="http://localhost:8000/ServiceModelSamples/service" />
        </baseAddresses>
      </host>
      <!-- this endpoint is exposed at the base address provided by host: http://localhost:8000/ServiceModelSamples/service -->
      <endpoint address=""
                binding="basicHttpBinding"
                bindingConfiguration="Binding1"
                contract="Microsoft.ServiceModel.Samples.ICalculator" />
      <!-- the mex endpoint is exposed at http://localhost:8000/ServiceModelSamples/service/mex -->
      <endpoint address="mex"
                binding="mexHttpBinding"
                contract="IMetadataExchange" />
    </service>
  </services>
  <bindings>
    <basicHttpBinding>
    <!-- This configuration defines the SecurityMode as Message and
         the clientCredentialType as Certificate. -->
      <binding name="Binding1">
        <security mode = "Message">
          <message clientCredentialType="Certificate" />
        </security>
      </binding>
    </basicHttpBinding>
  </bindings>
  <!--For debugging purposes set the includeExceptionDetailInFaults attribute to true-->
  <behaviors>
    <serviceBehaviors>
      <behavior name="CalculatorServiceBehavior">
        <serviceMetadata httpGetEnabled="True" />
        <serviceDebug includeExceptionDetailInFaults="False" />
        <!-- The serviceCredentials behavior allows one to define a service certificate.
             A service certificate is used by a client to authenticate the service and provide message protection.
             This configuration references the "localhost" certificate installed during the setup instructions. -->
        <serviceCredentials>
          <serviceCertificate findValue="localhost"
                              storeLocation="LocalMachine"
                              storeName="My"
                              x509FindType="FindBySubjectName" />
          <clientCertificate>
            <!-- Setting the certificateValidationMode to PeerOrChainTrust means that if the certificate
               is in the user's Trusted People store, then it will be trusted without performing a
               validation of the certificate's issuer chain. This setting is used here for convenience so that the
               sample can be run without having to have certificates issued by a certification authority (CA).
               This setting is less secure than the default, ChainTrust. The security implications of this
               setting should be carefully considered before using PeerOrChainTrust in production code. -->
            <authentication certificateValidationMode="PeerOrChainTrust" />
          </clientCertificate>
        </serviceCredentials>
      </behavior>
    </serviceBehaviors>
  </behaviors>
</system.serviceModel>
```  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.ServiceModel.BasicHttpMessageSecurity>
- <xref:System.ServiceModel.Configuration.BasicHttpSecurityElement.Message%2A>
- <xref:System.ServiceModel.BasicHttpSecurity.Message%2A>
- <xref:System.ServiceModel.Configuration.BasicHttpMessageSecurityElement>
- [Hizmet ve İstemcileri Güvenli Hale Getirme](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [Bağlamalar](../../../../../docs/framework/wcf/bindings.md)
- [Sistem Tarafından Sağlanan Bağlamaları Yapılandırma](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [Hizmetler ve İstemcileri Yapılandırmak için Bağlamaları Kullanma](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [\<bağlama >](../../../../../docs/framework/misc/binding.md)
