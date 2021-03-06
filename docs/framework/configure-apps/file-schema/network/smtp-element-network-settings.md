---
title: <smtp> Öğesi (Ağ Ayarları)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/mailSettings/smtp
- http://schemas.microsoft.com/.NetConfiguration/v2.0#smtp
helpviewer_keywords:
- <smtp> element
- smtp element
ms.assetid: 220b0329-e384-4e0c-86b4-0945ad17efd9
ms.openlocfilehash: 1b5f7406f995a86f0a192dbf3249c067dff570ea
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61674408"
---
# <a name="smtp-element-network-settings"></a>\<SMTP > öğesi (ağ ayarları)
Teslim biçimini, teslim yöntemini yapılandırır ve Kimden e-postaları gönderme için adresi.  
  
 \<Yapılandırma >  
\<system.net>  
\<mailSettings >  
\<SMTP >  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<smtp  
  deliveryFormat="format"  
  deliveryMethod="method"  
  from="from address">
    <specifiedPickupDirectory>...</specifiedPickupDirectory>  
    <network>...</network>  
</smtp>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`deliveryFormat`|Giden e-postalar için teslim etme biçimini belirtir. Kabul edilebilir değerler şunlardır: SevenBit ve uluslararası ' dir.|  
|`deliveryMethod`|E-postalar için teslim etme yöntemini belirtir. Ağ, Pickupdirectoryfromıis ve SpecifiedPickupDirectory bunun kabul edilebilir değerlerdir.|  
|`from`|Belirtir giden e-postalar için adresinden.|  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`specifiedPickupDirectory`|Bir Basit Posta Aktarım Protokolü (SMTP) sunucusu için yerel dizini yapılandırır.|  
|`network`|Dış SMTP sunucusu ağ seçeneklerini yapılandırır.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|**Öğe**|**Açıklama**|  
|-----------------|---------------------|  
|[\<mailSettings > öğesi (ağ ayarları)](../../../../../docs/framework/configure-apps/file-schema/network/mailsettings-element-network-settings.md)|Posta gönderme seçeneklerini yapılandırır.|  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, varsayılan ağ kimlik bilgilerini kullanarak e-posta göndermek için uygun SMTP parametrelerini belirtir.  
  
```xml  
<configuration>  
  <system.net>  
    <mailSettings>  
      <smtp deliveryMethod="Network" deliveryFormat="SevenBit"  from="ben@contoso.com">  
        <network  
          host="localhost"  
          port="25"  
          defaultCredentials="true"  
        />  
      </smtp>  
    </mailSettings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Net.Configuration.SmtpSection?displayProperty=nameWithType>
- <xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType>
- <xref:System.Net.Mail.SmtpDeliveryFormat>
- <xref:System.Net.Mail.SmtpDeliveryMethod>
- [Ağ Ayarları Şeması](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
