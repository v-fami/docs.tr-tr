---
title: Yapılandırma Olmadan AJAX Hizmeti
ms.date: 03/30/2017
ms.assetid: e6db7acd-5679-45d4-b98a-8449c6873838
ms.openlocfilehash: f5ebc952fcc6c2ca4c7272a90dc1929d4b4a0eae
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62002826"
---
# <a name="ajax-service-without-configuration"></a>Yapılandırma Olmadan AJAX Hizmeti
Bu örnek herhangi bir yapılandırma dosyası olmadan temel ASP.NET zaman uyumsuz JavaScript ve XML (AJAX) hizmet (bir Web tarayıcısı istemcisini JavaScript kodunu kullanarak erişebileceğiniz bir hizmeti) oluşturmak için Windows Communication Foundation (WCF) nasıl yapılacağı açıklanır. Ayarlar. Hizmet bir AJAX uç noktası otomatik olarak etkinleştirmeyi .svc dosyasında özel bir sözdizimi kullanır.  
  
 WCF AJAX desteği ASP.NET AJAX ile kullanım için optimize `ScriptManager` denetimi. ASP.NET AJAX ile WCF kullanan bir örnek için bkz: [Ajax örnekleri](ajax.md).  
  
> [!NOTE]
>  Bu örnek için Kurulum yordamı ve derleme yönergelerini, bu konunun sonunda yer alır.  
  
 Bu örnek, hizmet HTTP POST kullanan AJAX oluşturur. Bölümünde anlatıldığı gibi [temel AJAX hizmeti](../../../../docs/framework/wcf/samples/basic-ajax-service.md) örneği <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory> hizmeti barındırmak için kullanılır.  

```svc
<%ServiceHost  
    language=c#  
    Debug="true"  
    Service="Microsoft.Ajax.Samples.CalculatorService  
    Factory="System.ServiceModel.Activation.WebScriptServiceHostFactory"  
%>  
```

 <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory> otomatik olarak ekler bir <xref:System.ServiceModel.Description.WebScriptEndpoint> hizmeti. Hiçbir yapılandırma değişikliği uç noktasına yapılması gerekiyorsa `<system.ServiceModel>` bölümü tamamen kaldırılabilir hizmeti için Web.config dosyasındaki. Web.config dosyası ConfigFreeClientPage.aspx tarafından kullanılan bazı ASP.NET ayarları içerir. Bu durumda değilse, tüm Web.config dosyası kaldırılamadı.  
  
> [!IMPORTANT]
>  Örnekler, bilgisayarınızda yüklü. Devam etmeden önce şu (varsayılan) dizin denetleyin.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Bu dizin mevcut değilse Git [Windows Communication Foundation (WCF) ve .NET Framework 4 için Windows Workflow Foundation (WF) örnekleri](https://go.microsoft.com/fwlink/?LinkId=150780) tüm Windows Communication Foundation (WCF) indirmek için ve [!INCLUDE[wf1](../../../../includes/wf1-md.md)] örnekleri. Bu örnek, şu dizinde bulunur.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Ajax\ConfigFreeAjaxService`  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>Ayarlamak için derleme ve örneği çalıştırma  
  
1. İçindeki kurulum yönergelerini gerçekleştirdiğinizden emin olun [Windows Communication Foundation örnekleri için bir kerelik Kurulum yordamı](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).  
  
2. ' % S'çözüm ConfigFreeAjaxService.sln açıklandığı gibi oluşturmak [Windows Communication Foundation örnekleri derleme](../../../../docs/framework/wcf/samples/building-the-samples.md).  
  
3. Gidin `http://localhost/ServiceModelSamples/ConfigFreeClientPage.aspx` (ConfigFreeClientPage.aspx tarayıcıda proje dizininden açmayın).  
  
> [!NOTE]
>  Bu örnek çalışırken, anonim kimlik doğrulaması ve Windows kimlik doğrulaması aynı anda IIS ServiceModelSamples klasöründe etkin olmadığından emin olun. Lütfen bu durumda, Windows kimlik doğrulaması devre dışı bırakın. Örnek gerçekleştirdikten sonra Windows kimlik doğrulamasını etkinleştirmek ve "iisreset" çalıştırın.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Temel AJAX Hizmeti](../../../../docs/framework/wcf/samples/basic-ajax-service.md)
