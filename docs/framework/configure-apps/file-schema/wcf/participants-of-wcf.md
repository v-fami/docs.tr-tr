---
title: <participants> WCF
ms.date: 03/30/2017
ms.assetid: d99dbddc-0057-4e18-8e42-f91411d39970
ms.openlocfilehash: f714d7992266dbd6fc0c50a2bfadd61588179577
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61783428"
---
# <a name="participants-of-wcf"></a>\<Katılımcıları > WCF
Çalışma zamanını şuradan doğrudan yayılan izleme kayıtları için dinleme ve bunları hangi şekilde yapılandırılmış olan işleyen katılımcıları izleme listesi yapılandırın. Bu yazma içerir (örneğin, dosya, konsolu ETW), belirli bir çıktısına işleme/kayıtları veya gerekli olabilir herhangi bir birleşimini toplama.  
  
 İş akışı izleme ve izleme katılımcıları daha fazla bilgi için bkz. [takip ve izleme iş akışı](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md) ve [izleme katılımcıları](../../../../../docs/framework/windows-workflow-foundation/tracking-participants.md).  
  
 \<system.serviceModel>  
\<İzleme >  
\<Katılımcıları >  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<tracking>
  <participants>
    <add name="String"
         profileName="String"
         type="String" />
  </participants>
</tracking>
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
 Yok.  
  
### <a name="child-elements"></a>Alt Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[\<Ekle >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/add-of-participants.md)|Bir izleme Katılımcısı için ayarları içerir.|  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[\<İzleme >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/tracking.md)|Bir iş akışı hizmeti için izleme ayarları tanımlamak için bir yapılandırma bölümünü temsil eder.|  
  
## <a name="remarks"></a>Açıklamalar  
 İzleme katılımcıları akışından yayılan izleme verilerini almak için kullanılır ve farklı ortamları depolar. Benzer şekilde, herhangi işleme kayıtları da içinde izleme katılımcı yapılabilir izleme gönderin.  
  
 Aynı anda birden çok izleme katılımcıları izleme olaylarını kullanabilir. Her izleme katılımcı farklı izleme profili ile ilişkilendirilebilir.  
  
 Standart izleme katılımcı, izleme kayıtları bir ETW oturumu Yazar sağlanır. Katılımcı bir iş akışı hizmeti yapılandırma dosyasında bir izleme özgü davranışı ekleyerek yapılandırılır. Etkinleştirme bir ETW İzleme katılımcı olacak şekilde kayıtları izleme Olay Görüntüleyicisi'görüntülemesini sağlar. Gereksinimlerinizi karşılamıyorsa, özel izleme katılımcı de yazabilirsiniz.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki yapılandırma örnek Web.config dosyasında yapılandırılan standart ETW İzleme katılımcı gösterir.  
  
 ETW İzleme katılımcı için ETW İzleme kayıtları yazmak için kullandığı sağlayıcı kimliği tanımlanan `<diagnostics>` bölümü. İzleme katılımcı abone izleme kayıtları belirtmek için ile ilişkili bir profil var. Bu tarafından tanımlanan `profileName` özniteliği `<add>` öğesi. Bunlar tanımlandıktan izleme katılımcı eklenir `<etwTracking>` hizmet davranışı. Böylece bunlar izleme kayıtları almak başlayabilirsiniz bu iş akışı örneğinin uzantıları için seçilen izleme katılımcıları ekleyecektir.  
  
```xml  
<configuration>
  <system.web>
    <compilation targetFrameworkMoniker=".NETFramework,Version=v4.0" />
  </system.web>
  <system.serviceModel>
    <diagnostics etwProviderId="52A3165D-4AD9-405C-B1E8-7D9A257EAC9F" />
    <tracking>
      <participants>
        <add name="EtwTrackingParticipant"
             type="System.Activities.Tracking.EtwTrackingParticipant, System.Activities, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"
             profileName="HealthMonitoring_Tracking_Profile"/>
      </participants>
    </tracking>
    <behaviors>
      <serviceBehaviors>
        <behavior>
          <etwTracking profileName="Sample Tracking Profile"/>
        </behavior>
      </serviceBehaviors>
    </behaviors>
  </system.serviceModel>
</configuration>
```  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.ServiceModel.Activities.Tracking.Configuration.TrackingSection>
- <xref:System.ServiceModel.Activities.Description.EtwTrackingBehavior>
- [İş Akışı Takip ve İzleme](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [İzleme Katılımcıları](../../../../../docs/framework/windows-workflow-foundation/tracking-participants.md)
