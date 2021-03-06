---
title: 'Nasıl yapılır: WCF Hizmetini ASP.NET Web Hizmeti İstemcileriyle Birlikte Çalışmak için Yapılandırma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 48e1cd90-de80-4d6c-846e-631878955762
ms.openlocfilehash: 8b43ae8345fe8c4286f00f4b6e4f6373746e8bbe
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65882164"
---
# <a name="how-to-configure-wcf-service-to-interoperate-with-aspnet-web-service-clients"></a>Nasıl yapılır: WCF Hizmetini ASP.NET Web Hizmeti İstemcileriyle Birlikte Çalışmak için Yapılandırma
Bir Windows Communication Foundation (WCF) hizmet uç noktası ile ASP.NET Web hizmeti istemcileriyle birlikte çalışabilen olacak şekilde yapılandırmak için kullanın <xref:System.ServiceModel.BasicHttpBinding?displayProperty=nameWithType> türü, hizmet uç noktası için bağlama türü olarak.  
  
 İsteğe bağlı olarak, HTTPS ve bağlamadaki aktarım düzeyinde istemci kimlik doğrulaması için destek de etkinleştirebilirsiniz. ASP.NET Web hizmeti istemcileri desteklemediği ileti MTOM kodlama, böylece <xref:System.ServiceModel.BasicHttpBinding.MessageEncoding%2A?displayProperty=nameWithType> özelliği olan varsayılan değer olarak sol <xref:System.ServiceModel.WSMessageEncoding.Text?displayProperty=nameWithType>. ASP.Net Web hizmeti istemcileri desteklemediği WS-Security, bu nedenle <xref:System.ServiceModel.BasicHttpBinding.Security%2A?displayProperty=nameWithType> ayarlanmalıdır <xref:System.ServiceModel.BasicHttpSecurityMode.Transport>.  
  
 Meta veriler için bir WCF hizmetini ASP.NET Web hizmeti proxy oluşturma araçları kullanılabilir hale getirmek için (diğer bir deyişle, [Web Hizmetleri Açıklama Dili Aracı (Wsdl.exe)](https://go.microsoft.com/fwlink/?LinkId=73833), [Web Hizmetleri bulma Aracı (Disco.exe)](https://go.microsoft.com/fwlink/?LinkId=73834), ve Visual Studio Web Başvurusu Ekle özelliği), bir HTTP/GET meta veri uç noktası sunmalıdır.  
  
### <a name="to-add-a-wcf-endpoint-that-is-compatible-with-aspnet-web-service-clients-in-code"></a>ASP.NET Web hizmeti istemcileriyle kod ile uyumlu bir WCF uç noktası eklemek için  
  
1. Yeni bir <xref:System.ServiceModel.BasicHttpBinding> örneği  
  
2. İsteğe bağlı olarak Aktarım güvenliği için hizmet uç noktası bağlaması Bu bağlama için güvenlik modunu ayarlama etkinleştirme <xref:System.ServiceModel.BasicHttpSecurityMode.Transport>. Ayrıntılar için lütfen bkz [aktarım güvenliği](../../../../docs/framework/wcf/feature-details/transport-security.md).  
  
3. Yeni bir uygulama uç noktasını kullanarak yeni oluşturduğunuz bağlama örneği, hizmet ana bilgisayar ekleyin. Kod içinde hizmet uç noktası ekleme hakkında daha fazla bilgi için bkz. [nasıl yapılır: Kod içinde hizmet uç noktası oluşturma](../../../../docs/framework/wcf/feature-details/how-to-create-a-service-endpoint-in-code.md).  
  
4. Hizmetiniz için bir HTTP/GET meta veri uç noktası etkinleştirin. Ayrıntılar için bkz. [nasıl yapılır: Kod kullanarak bir hizmet için meta verileri yayımlama](../../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-code.md).  
  
### <a name="to-add-a-wcf-endpoint-that-is-compatible-with-aspnet-web-service-clients-in-a-configuration-file"></a>Bir yapılandırma dosyasında ASP.NET Web hizmeti istemcileriyle uyumlu bir WCF uç noktası eklemek için  
  
1. Yeni bir <xref:System.ServiceModel.BasicHttpBinding> bağlama yapılandırması. Ayrıntılar için bkz [nasıl yapılır: Yapılandırmada hizmet bağlaması belirtme](../../../../docs/framework/wcf/how-to-specify-a-service-binding-in-configuration.md).  
  
2. İsteğe bağlı olarak bu hizmet uç noktası bağlama yapılandırması için Aktarım güvenliği bağlama için güvenlik modunu ayarlama etkinleştirme <xref:System.ServiceModel.BasicHttpSecurityMode.Transport>. Ayrıntılar için bkz [aktarım güvenliği](../../../../docs/framework/wcf/feature-details/transport-security.md).  
  
3. Yeni oluşturduğunuz bağlama yapılandırması kullanarak hizmetiniz için yeni bir uygulama uç noktası yapılandırın. Bir yapılandırma dosyasında bir hizmet uç noktası ekleme hakkında daha fazla bilgi için bkz [nasıl yapılır: Yapılandırma içinde hizmet uç noktası oluşturma](../../../../docs/framework/wcf/feature-details/how-to-create-a-service-endpoint-in-configuration.md).  
  
4. Hizmetiniz için bir HTTP/GET meta veri uç noktası etkinleştirin. Ayrıntılar için bkz. [nasıl yapılır: Bir yapılandırma dosyası kullanarak bir hizmet için meta verileri yayımlama](../../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği, ASP.NET Web hizmeti istemcileriyle kod ile uyumlu bir WCF uç noktası eklemek gösterilmiştir ve bunun yerine yapılandırma dosyalarında.  
  
 [!code-csharp[C_HowTo-WCFServiceAndASMXClient#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto-wcfserviceandasmxclient/cs/program.cs#0)] 
 [!code-vb[C_HowTo-WCFServiceAndASMXClient#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto-wcfserviceandasmxclient/vb/program.vb#0)] 
 [!code-xml[C_HowTo-WCFServiceAndASMXClient#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto-wcfserviceandasmxclient/common/app.config#1)]     
  
## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Kod içinde hizmet uç noktası oluşturma](../../../../docs/framework/wcf/feature-details/how-to-create-a-service-endpoint-in-code.md)
- [Nasıl yapılır: Kod kullanarak bir hizmet için meta verileri yayımlama](../../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-code.md)
- [Nasıl yapılır: Yapılandırmada hizmet bağlaması belirtme](../../../../docs/framework/wcf/how-to-specify-a-service-binding-in-configuration.md)
- [Nasıl yapılır: Yapılandırma içinde hizmet uç noktası oluşturma](../../../../docs/framework/wcf/feature-details/how-to-create-a-service-endpoint-in-configuration.md)
- [Nasıl yapılır: Bir yapılandırma dosyası kullanarak bir hizmet için meta verileri yayımlama](../../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [Aktarım Güvenliği](../../../../docs/framework/wcf/feature-details/transport-security.md)
- [Meta Verileri Kullanma](../../../../docs/framework/wcf/feature-details/using-metadata.md)
