---
title: <iriParsing> Öğesi (Uri Ayarları)
ms.date: 03/30/2017
ms.assetid: 953d0b53-445e-41f9-b302-77c4030852ce
ms.openlocfilehash: 7033f4dcda7d2fe73310ae0d36d9b05c090d13d4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61674525"
---
# <a name="iriparsing-element-uri-settings"></a>\<iriParsing > öğesi (Uri ayarları)
Uluslararası kaynak tanımlayıcı (IRI) ayrıştırma için uygulanmış olup olmadığını belirten bir <xref:System.Uri> ve IRI ayrıştırma kurallarını uygulanıp.  
  
## <a name="schema-hierarchy"></a>Şema hiyerarşisi  
 [\<Yapılandırma > öğesi](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
  
 [\<URI > öğesi (Uri ayarları)](../../../../../docs/framework/configure-apps/file-schema/network/uri-element-uri-settings.md)  
  
 [\<iriParsing >](../../../../../docs/framework/configure-apps/file-schema/network/iriparsing-element-uri-settings.md)  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<iriParsing  
  enabled="true|false"  
/>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|**Öğe**|**Açıklama**|  
|-----------------|---------------------|  
|`enabled`|IRI ayrıştırma etkinleştirilip etkinleştirilmeyeceğini belirtir. Varsayılan değer `false` şeklindedir.|  
  
### <a name="child-elements"></a>Alt Öğeler  
 Yok.  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|**Öğe**|**Açıklama**|  
|-----------------|---------------------|  
|[URI](../../../../../docs/framework/configure-apps/file-schema/network/uri-element-uri-settings.md)|.NET Framework web adresleri Tekdüzen Kaynak Tanımlayıcıları (URI'lar) kullanılarak ifade nasıl işlediğini belirten ayarları içerir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Varolan <xref:System.Uri> sınıfı, .NET Framework 3.5 genişletilmişse. 3.0 SP1 ve 2.0 SP1 uluslararası kaynak tanımlayıcı (IRI) ve Uluslararası yapılan etki alanı adı (IDN) desteği sağlamak için. Özellikle IRI ve IDN etkinleştirmediğiniz sürece geçerli kullanıcıların .NET Framework 2.0 davranış herhangi bir değişikliği göremezsiniz destekler. Bu, .NET Framework'ün önceki sürümleriyle uygulama uyumluluğu sağlar.  
  
 IRI desteğini etkinleştirmek için aşağıdaki iki değişiklik gerekmez:  
  
1. Machine.config dosyasının .NET Framework 2.0 dizininde aşağıdaki satırı ekleyin  
  
    ```xml  
    <section name="uri" type="System.Configuration.UriSection, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
    ```  
  
2. IRI ayrıştırma kurallarını uygulanması gerektiğini belirtin. Bu, machine.config veya app.config dosyasında yapılabilir.  
  
 IRI ayrıştırma etkinleştirme (etkin iriParsing = `true`) normalleştirme yapar ve karakter göre en son IRI denetleme kuralları RFC 3987. Varsayılan değer `false` normalleştirme yapın ve RFC 2396 göre denetleme ve RFC 3986'ya (IPv6 değişmez değerleri için) karakter.  
  
### <a name="configuration-files"></a>Yapılandırma Dosyaları  
 Bu öğe, uygulama yapılandırma dosyası veya makine yapılandırma dosyası (Machine.config) kullanılabilir.  
  
## <a name="example"></a>Örnek  
  
### <a name="description"></a>Açıklama  
 Aşağıdaki örnek tarafından kullanılan bir yapılandırma gösterir <xref:System.Uri> IRI ayrıştırma ve IDN adları desteklemek için sınıf.  
  
### <a name="code"></a>Kod  
  
```xml  
<configuration>  
  <uri>  
    <idn enabled="All" />  
    <iriParsing enabled="true" />  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Configuration.IriParsingElement?displayProperty=nameWithType>
- <xref:System.Configuration.UriSection?displayProperty=nameWithType>
- [Ağ Ayarları Şeması](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
