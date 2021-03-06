---
title: Hizmet Denetleme Davranışı
ms.date: 03/30/2017
ms.assetid: 59bf0cda-e496-4418-a3a1-2f0f6e85f8ce
ms.openlocfilehash: 1719db9749336d584627280aba3412557b164356
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61787458"
---
# <a name="service-auditing-behavior"></a>Hizmet Denetleme Davranışı
Bu örnek nasıl kullanılacağını gösterir <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior> hizmet işlemleri sırasında güvenlik olaylarının denetlenmesini etkinleştirme. Bu örnek dayanır [Başlarken](../../../../docs/framework/wcf/samples/getting-started-sample.md). Hizmet ve istemci kullanarak yapılandırılmış [ \<wsHttpBinding >](../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md). `mode` Özniteliği [ \<Güvenlik >](../../../../docs/framework/configure-apps/file-schema/wcf/security-of-custombinding.md) ayarlanmış `Message` ve `clientCredentialType` ayarlanmış `Windows`. Bu örnekte, istemci bir konsol uygulaması (.exe) ve hizmet Internet Information Services (IIS) tarafından barındırılır.  
  
> [!NOTE]
>  Bu örnek için Kurulum yordamı ve derleme yönergelerini, bu konunun sonunda yer alır.  
  
 Hizmet yapılandırma dosyasını kullanan `serviceSecurityAudit` denetimini yapılandırmak için öğesi.  
  
```xml  
<behaviors>  
  <serviceBehaviors>  
    <behavior name="CalculatorServiceBehavior">  
      ...  
<!-- serviceSecurityAudit allows specification of audit location   
     and whether to audit success, failure or both. This service   
     logs success and failure of messageAuthentication   
     to the default location -->  
     <serviceSecurityAudit auditLogLocation ="Default" messageAuthenticationAuditLevel = "SuccessOrFailure" />  
    </behavior>  
  </serviceBehaviors>  
</behaviors>  
```  
  
 Örneği çalıştırdığınızda, işlem isteklerini ve yanıtlarını istemci konsol penceresinde görüntülenir. Konsol penceresinde istemci kapatmak için ENTER tuşuna basın.  
  
 Sonuçta elde edilen denetim günlüklerini, Olay Görüntüleyicisi'ni çalıştırarak görülebilir. Varsayılan olarak, Windows XP, Windows Server 2003 ve Windows Vista sırasında uygulama günlüğünde denetim olaylarının görülebilir denetim olayları güvenlik günlüğünde görülebilir. Windows Server 2008 ve Windows 7, denetim olayları uygulamaları ve Hizmetleri günlüklerinde görülebilir. Denetim olayları konumunu ayarlayarak belirtilebilir `auditLogLocation` özniteliği için "Uygulama" veya "Güvenlik". Daha fazla bilgi için [nasıl yapılır: Güvenlik olaylarını denetleme](../../../../docs/framework/wcf/feature-details/how-to-audit-wcf-security-events.md). Olayları, nesne erişimi etkinleştirmek için "Başarılı" ve "Başarısız" ayarlanmalıdır LocalSecurityPolicy -> güvenlik günlüğüne yazılır  
  
 Olay günlüğüne baktığımda denetim olayları "ServiceModel denetim 3.0.0.0" kaynağıdır. Hizmet yetkilendirme Denetim kayıtlarını "ServiceAuthorization" kategorisi ileti kimlik doğrulama Denetim kayıtlarını "MessageAuthentication" kategorisi bulunur.  
  
 İleti, ileti olup süresi doldu ve istemci hizmeti için olup olmadığını doğrulanabilir oynanmış olmadığını ileti kimlik doğrulaması olaylarının kapsar. Bunlar kimlik doğrulaması başarılı oldu veya istemci kimliği ile birlikte başarısız hakkında bilgi sağlar ve uç nokta ileti birlikte iletiyle ilişkili eylemi için gönderildi.  
  
 Hizmet yetkilendirme denetim olaylarını hizmet Yetkilendirme Yöneticisi tarafından yapılan yetkilendirme kararı kapsar. Yetkilendirme başarılı olup olmadığını hakkında bilgi sağladıkları veya istemci kimliği ile birlikte başarısız oldu, uç nokta ileti, ileti öğesinden oluşturulan yetkilendirme Bağlam tanıtıcısı ile ilişkili eylem gönderildi gelen ileti ve erişim kararı Yetkilendirme Yöneticisi türünü.  
  
### <a name="to-set-up-build-and-run-the-sample"></a>Ayarlamak için derleme ve örneği çalıştırma  
  
1. Gerçekleştirdiğinizden emin olmak [Windows Communication Foundation örnekleri için bir kerelik Kurulum yordamı](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).  
  
2. Çözüm C# veya Visual Basic .NET sürümünü oluşturmak için yönergeleri izleyin. [Windows Communication Foundation örnekleri derleme](../../../../docs/framework/wcf/samples/building-the-samples.md).  
  
3. Tek veya çoklu bilgisayar yapılandırmasında örneği çalıştırmak için yönergeleri izleyin. [Windows Communication Foundation örneklerini çalıştırma](../../../../docs/framework/wcf/samples/running-the-samples.md).  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Denetim](../../../../docs/framework/wcf/feature-details/auditing-security-events.md)
- [Nasıl yapılır: Güvenlik olaylarını denetleme](../../../../docs/framework/wcf/feature-details/how-to-audit-wcf-security-events.md)
