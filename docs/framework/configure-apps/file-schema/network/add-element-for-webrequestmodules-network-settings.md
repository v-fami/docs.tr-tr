---
title: webRequestModules için <add> Öğesi (Ağ Ayarları)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/webRequestModules/add
- http://schemas.microsoft.com/.NetConfiguration/v2.0#add
helpviewer_keywords:
- <webRequestModules>, add element
- webRequestModules, add element
- add element, webRequestModules
- <add> element, webRequestModules
ms.assetid: 47ec4adc-f39f-4bcd-8680-1ec21fd26890
ms.openlocfilehash: 4c1116c088c12ad3859714c8d75704d0156c12f7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61705148"
---
# <a name="add-element-for-webrequestmodules-network-settings"></a>\<Ekle > webRequestModules (ağ ayarları) için
Uygulamaya özel bir Web isteği modülü ekler.  
  
 \<Yapılandırma >  
\<system.net>  
\<webRequestModules >  
\<Ekle >  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<add   
  prefix="URI prefix"   
  type="type_fullname, assembly_fullname"   
/>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|**Öznitelik**|**Açıklama**|  
|-------------------|---------------------|  
|`prefix`|Bu Web isteği modülü tarafından işlenen isteklerin için URI öneki.|  
|`type`|Tam nitelikli tür adı (belirttiği <xref:System.Type.FullName%2A> özelliği) ve derleme adı (belirttiği <xref:System.Reflection.Assembly.FullName%2A> özelliği) bu Web isteği modülü uygulayan bir virgülle ayrılmış.|  
  
### <a name="child-elements"></a>Alt Öğeler  
 Yok.  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|**Öğe**|**Açıklama**|  
|-----------------|---------------------|  
|[webRequestModules](../../../../../docs/framework/configure-apps/file-schema/network/webrequestmodules-element-network-settings.md)|Ağ konaklarından bilgi istemek için modüller belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 `prefix` Özniteliği belirtilen Web isteği modül kullanan URI öneki tanımlar. Web isteği modülleri, HTTP veya FTP gibi belirli bir protokol işlemek için genellikle kayıtlı ancak belirli sunucu veya bir sunucudaki yolu bir isteği işlemek için kaydedilebilir.  
  
 Web isteği modülü URI'si ile eşleşen bir ön eki geçirilir oluşturulduğunda <xref:System.Net.WebRequest.Create%2A?displayProperty=nameWithType> yöntemi.  
  
 Değeri `prefix` özniteliği önde gelen karakterleri geçerli bir URI olmalıdır. Örneğin, `http` veya `http://www.contoso.com`.
  
 Değeri `type` özniteliği geçerli tür adı ve karşılık gelen derleme adı, virgülle ayrılmış olmalıdır.
  
## <a name="configuration-files"></a>Yapılandırma Dosyaları  
 Bu öğe, uygulama yapılandırma dosyası veya makine yapılandırma dosyası (Machine.config) kullanılabilir.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, HTTP için özel bir Web isteği modülü kaydeder. Belirtilen modül için doğru değerlerle PublicKeyToken ve Version değerleri değiştirmelisiniz.  
  
```xml  
<configuration>  
  <system.net>  
    <webRequestModules>  
      <add prefix="http"  
           type="System.Net.HttpRequestCreator, System, Version=2.0.3600.0,  
           Culture=neutral, PublicKeyToken=b77a5c561934e089"  
      />  
    </webRequestModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Net.WebRequest>
- [Ağ Ayarları Şeması](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
