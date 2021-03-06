---
title: WCF Veri Hizmetleri Geliştirme ve Dağıtma
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, developing
- WCF Data Services, deploying
- deploying [WCF Data Services
- developing applications [WCF Data Services]
ms.assetid: 6557c0e3-5aea-4f6e-bc14-77ad317a168b
ms.openlocfilehash: ef38bacfd129033aab41f5f516b96b95fac7913f
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65880003"
---
# <a name="develop-and-deploy-wcf-data-services"></a>Geliştirme ve WCF veri hizmetlerini dağıtma

Bu konu, geliştirme ve WCF veri hizmetlerini dağıtma hakkında bilgi sağlar. WCF veri hizmetleri hakkında daha temel bilgiler için bkz: [Başlarken](../../../../docs/framework/data/wcf/getting-started-with-wcf-data-services.md) ve [genel bakış](../../../../docs/framework/data/wcf/wcf-data-services-overview.md).

## <a name="develop-wcf-data-services"></a>WCF Veri Hizmetleri Geliştirme

WCF veri hizmetleri destekleyen bir veri hizmeti oluşturmak için kullandığınızda [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)], geliştirme sırasında aşağıdaki temel görevleri gerçekleştirmeniz gerekir:

1. **Veri modelini tanımlama**

     WCF Veri Hizmetleri, çeşitli çeşitli ilişkisel veritabanlarından geç bağlanan veri türlerine veri kaynaklarından alınan verileri temel alan bir veri modeli tanımlamanızı sağlayan çeşitli veri hizmeti sağlayıcılarını destekler. Daha fazla bilgi için [Veri Hizmetleri sağlayıcıları](../../../../docs/framework/data/wcf/data-services-providers-wcf-data-services.md).

2. **Veri hizmeti oluşturma**

     En temel veri hizmeti devralınan bir sınıfı gösterir <xref:System.Data.Services.DataService%601> türüne sahip bir sınıf `T` varlık kapsayıcısının yani ad alanıyla nitelenen adı. Daha fazla bilgi için [Defining WCF Data Services](../../../../docs/framework/data/wcf/defining-wcf-data-services.md).

3. **Veri hizmetini yapılandırma**

     Varsayılan olarak, WCF Veri Hizmetleri bir varlık kapsayıcısı tarafından kullanılan kaynaklara erişimi devre dışı bırakır. <xref:System.Data.Services.DataServiceConfiguration> Arabirimi, kaynaklara erişimi yapılandırma ve hizmet işlemlerine, desteklenen OData sürümü belirtin ve döndürülebilecek varlık davranışları veya en büyük toplu işleme gibi diğer hizmet kapsamındaki davranışları tanımlamanızı sağlar tek bir yanıt akışında. Daha fazla bilgi için [veri hizmeti yapılandırma](../../../../docs/framework/data/wcf/configuring-the-data-service-wcf-data-services.md).

Bu konu, Visual Studio kullanarak, öncelikli olarak geliştirme ve Veri Hizmetleri dağıtımını kapsar. Verilerinizi OData akışı olarak kullanıma sunmak için WCF Veri Hizmetleri tarafından sağlanan esneklik hakkında daha fazla bilgi için bkz. [Defining WCF Data Services](../../../../docs/framework/data/wcf/defining-wcf-data-services.md).

### <a name="choose-a-development-web-server"></a>Bir geliştirme Web sunucusu seçin

Visual Studio 2015'i kullanarak bir ASP.NET uygulaması veya ASP.NET Web sitesi WCF veri hizmeti geliştirdiğinizde, geliştirme sırasında veri hizmetinin çalıştırılacağı Web sunucularını vardır. Aşağıdaki Web sunucuları, test ve hata ayıklama yerel bilgisayarda veri hizmetlerinizin daha kolay hale getirmek için Visual Studio ile tümleştirin.

1. **Yerel IIS sunucusu**

     Bir ASP.NET uygulamasını veya Internet Information Services (IIS) üzerinde çalışan ASP.NET Web sitesi olan bir veri hizmeti oluşturduğunuzda, geliştirme ve veri hizmetinizi yerel bilgisayarda IIS'yi kullanarak test öneririz. IIS üzerinde veri hizmetinin çalıştırılması, hata ayıklama sırasında HTTP isteklerinin izlenmesini kolaylaştırır. Bu, IIS tarafından dosyalara, veritabanlarına ve veri hizmeti tarafından gerekli kılınan diğer kaynaklara erişmek için gereken hakları önceden belirlemenizi de sağlar. Veri hizmetinizi IIS üzerinde çalıştırmak için size gereken sağlar hem IIS hem de Windows Communication Foundation (WCF) yüklü ve düzgün yapılandırıldığından emin ve dosya sistemi ve veritabanlarında IIS hesaplarına erişim izin verin. Daha fazla bilgi için [nasıl yapılır: IIS üzerinde çalışan bir WCF veri hizmeti geliştirme](../../../../docs/framework/data/wcf/how-to-develop-a-wcf-data-service-running-on-iis.md).

    > [!NOTE]
    > Visual Studio geliştirme ortamının yerel IIS sunucusunu yapılandırmasını etkinleştirmek için yönetici haklarıyla çalıştırmanız gerekir.

2. **Visual Studio geliştirme sunucusu**

     Visual Studio, bir yerleşik Web sunucusu Visual Studio geliştirme ASP.NET projeleri için varsayılan Web sunucusu, içerir. Bu Web sunucusu, ASP.NET projeleri, geliştirme sırasında yerel bilgisayarda çalıştırmak için tasarlanmıştır. [WCF Veri Hizmetleri Hızlı Başlangıç](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md) Visual Studio geliştirme sunucusu içinde çalışan bir veri hizmeti oluşturulacağını gösterir.

     Veri hizmeti geliştirmek için Visual Studio geliştirme sunucusu kullanırken aşağıdaki sınırlamaları bilmeniz gerekir:

    - Bu sunucuya yalnızca yerel bilgisayar üzerinde erişilebilir.

    - Bu sunucunun dinlediği `localhost` ve belirli bir bağlantı noktası, HTTP iletileri için varsayılan bağlantı noktası olan olmayan bağlantı noktası 80. Daha fazla bilgi için [ASP.NET Web projeleri için Visual Studio'daki Web sunucuları](https://docs.microsoft.com/previous-versions/aspnet/58wxa9w5(v=vs.120)).

    - Bu sunucu, geçerli kullanıcı hesabınızın bağlamında veri hizmetini çalıştırır. Örneğin, bir yönetici düzeyinde kullanıcı olarak çalıştırıyorsanız, Visual Studio geliştirme sunucusu içinde çalışan bir veri hizmeti yönetici düzeyinde ayrıcalıkları olacaktır. Bu, veri hizmetinin IIS sunucusuna dağıtıldığında erişim hakkı olmayan kaynaklara erişebilmesini sağlar.

    - Bu sunucu, IIS'nin kimlik doğrulama gibi ek özelliklerini içermez.

    - Bu sunucu öbekli HTTP akışlarını işleyemez gönderildiği olması WCF Veri Hizmetleri istemci tarafından varsayılan veri hizmetinden büyük ikili verilere erişilirken. Daha fazla bilgi için [Akış sağlayıcısı](../../../../docs/framework/data/wcf/streaming-provider-wcf-data-services.md).

    - Bu sunucu işleme süresi olan sorunlar varsa (`.`) bu karakteri anahtar değerlerinde WCF Veri Hizmetleri tarafından desteklenmesine rağmen URL'de karakter.

    > [!TIP]
    > Geliştirme sırasında veri hizmetlerinizi test etmek için Visual Studio geliştirme sunucusunu kullanıyor olsanız da, IIS çalıştıran Web sunucusuna dağıttıktan sonra test etmeniz gerekir.

3. **Windows Azure geliştirme ortamı**

     Visual Studio için Windows Azure Araçları, tümleşik bir Visual Studio içinde Windows Azure hizmetleri geliştirmek için araçlar kümesi içerir. Bu araçlarla, Microsoft Azure'a dağıtılabilen bir veri hizmeti geliştirebilir ve veri hizmetini dağıtımdan önce yerel bilgisayarda test edebilirsiniz. Visual Studio Windows Azure platformunda çalışan bir veri hizmeti geliştirmek için kullanırken bu araçları kullanın. Visual Studio için Windows Azure Araçları'nı indirebilirsiniz [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkID=201848). Windows Azure üzerinde çalışan bir veri hizmeti geliştirme hakkında daha fazla bilgi için gönderiye bakın [Windows azure'da OData hizmeti dağıtma](https://go.microsoft.com/fwlink/?LinkId=201847).

### <a name="development-tips"></a>Geliştirme İpuçları

Bir veri hizmeti geliştirirken, aşağıdakileri dikkate almanız gerekir:

- Kullanıcıların kimliğini doğrulamayı veya belirli kullanıcılar için erişimi kısıtlamayı planlıyorsanız, veri hizmetinizin güvenlik gereksinimlerini belirleyin. Daha fazla bilgi için [WCF Veri Hizmetleri güvenli hale getirme](../../../../docs/framework/data/wcf/securing-wcf-data-services.md).

- HTTP inceleme programı, istek ve yanıt iletilerinin içeriğini denetlemenizi sağlayarak veri hizmetinde hata ayıklarken size epey yardımcı olabilir. Veri hizmetine yapılan HTTP isteklerini ve veri hizmetinden alınan yanıtları denetlemek için ham paketleri görüntüleyebilen herhangi bir ağ paketi çözümleyicisi kullanılabilir.

- Veri hizmetinde hata ayıklarken veri hizmetinden normal işlem sırasında bir hata hakkında daha fazla bilgi almak isteyebilirsiniz. Ayarlayarak veri hizmetinden ek hata bilgileri alabilirsiniz <xref:System.Data.Services.DataServiceConfiguration.UseVerboseErrors%2A> özelliğinde <xref:System.Data.Services.DataServiceConfiguration> için `true` ayarlayarak <xref:System.ServiceModel.Description.ServiceDebugBehavior.IncludeExceptionDetailInFaults%2A> özelliği <xref:System.ServiceModel.Description.ServiceDebugBehavior> verihizmetisınıfındakiözniteliği`true`. Daha fazla bilgi için gönderiye bakın [hata ayıklama WCF Veri Hizmetleri](https://go.microsoft.com/fwlink/?LinkId=201868). WCF HTTP ileti katmanında oluşturulan özel durumları görüntülemek için izlemeyi de etkinleştirebilirsiniz. Daha fazla bilgi için [yapılandırma izleme](../../../../docs/framework/wcf/diagnostics/tracing/configuring-tracing.md).

- Bir veri hizmeti genellikle bir ASP.NET uygulama projesi olarak geliştirilir, ancak Ayrıca, veri hizmeti Visual Studio'daki bir ASP.NET Web sitesi projesi olarak oluşturun. İki proje türü arasındaki farklar hakkında daha fazla bilgi için bkz: [Web Application Projects versus Web sitesi projeleri Visual Studio'da](https://docs.microsoft.com/previous-versions/aspnet/dd547590(v=vs.110)).

- Kullanarak bir veri hizmeti oluşturduğunuzda **Yeni Öğe Ekle** Visual Studio'da veri hizmeti iletişim kutusu, ASP.NET'i IIS'ye tarafından barındırılır. ASP.NET ve IIS veri hizmeti için varsayılan ana bilgisayar olsa diğer barındırma seçenekleri desteklenir. Daha fazla bilgi için [veri hizmetini barındıran](../../../../docs/framework/data/wcf/hosting-the-data-service-wcf-data-services.md).

## <a name="deploy-wcf-data-services"></a>WCF veri hizmetlerini dağıtma

WCF Veri Hizmeti, veri hizmetini barındıran işlemi seçmede esneklik sağlar. Veri hizmetini aşağıdaki platformlara dağıtmak için Visual Studio'yu kullanabilirsiniz:

- **IIS barındırılan Web sunucusu**

    Bir veri hizmeti, bir ASP.NET projesi olarak geliştirilir, bunu bir IIS Web sunucusuna standart ASP.NET dağıtım işlemleri kullanılarak dağıtılabilir.  Visual Studio, ASP.NET'in dağıttığınız veri hizmetini barındıran ASP.NET proje türünü bağlı olarak aşağıdaki dağıtım teknolojileri sağlar.

  - **ASP.NET Web uygulamaları için dağıtım teknolojileri**

    - [Nasıl yapılır: Visual Studio'da bir Web dağıtım paketi oluşturma](https://docs.microsoft.com/previous-versions/aspnet/dd465323(v=vs.110))

    - [Nasıl yapılır: Bir Web dağıtımı kullanarak tek tıklamayla proje Visual Studio'ya Yayımla](https://docs.microsoft.com/previous-versions/aspnet/dd465337(v=vs.110))

  - **ASP.NET Web siteleri için dağıtım teknolojileri**

    - [Nasıl yapılır: Web sitesi kopyalama Web sitesi aracı dosyalarıyla kopyalayın](https://docs.microsoft.com/previous-versions/aspnet/c95809c0(v=vs.100))

    - [Nasıl yapılır: Web siteleri yayımlama](https://docs.microsoft.com/previous-versions/aspnet/20yh9f1b(v=vs.100))

    - [İzlenecek yol: XCOPY kullanarak bir ASP.NET Web uygulaması dağıtma](https://docs.microsoft.com/previous-versions/aspnet/f735abw9(v=vs.100))

     Bir ASP.NET uygulaması için dağıtım seçenekleri hakkında daha fazla bilgi için bkz. [Visual Studio ve ASP.NET Web dağıtımı genel bakış](https://docs.microsoft.com/previous-versions/aspnet/dd394698(v=vs.110)).

    > [!TIP]
    > Veri hizmetini IIS'ye dağıtmayı denemeden önce, IIS çalıştıran Web sunucusuna dağıtımı test ettiğinizden emin olun. Daha fazla bilgi için [nasıl yapılır: IIS üzerinde çalışan bir WCF veri hizmeti geliştirme](../../../../docs/framework/data/wcf/how-to-develop-a-wcf-data-service-running-on-iis.md).

- **Windows Azure**

     Visual Studio için Windows Azure araçlarını kullanarak bir veri hizmeti Windows Azure'a dağıtabilirsiniz. Visual Studio için Windows Azure Araçları'nı indirebilirsiniz [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkID=201848). Post Windows Azure'a veri hizmetini dağıtma hakkında daha fazla bilgi için bkz. [Windows azure'da OData hizmeti dağıtma](https://go.microsoft.com/fwlink/?LinkId=201847).

### <a name="deployment-considerations"></a>Dağıtım Hakkında Önemli Noktalar

Bir veri hizmetini dağıtırken, aşağıdakileri dikkate almanız gerekir:

- Kullanan bir veri hizmeti dağıtırken [!INCLUDE[adonet_ef](../../../../includes/adonet-ef-md.md)] bir SQL Server veritabanına erişmek için sağlayıcı veri yapılarını, verileri yaymak gerekebilir veya her ikisi de verilerinizi dağıtım hizmet. Visual Studio otomatik olarak hedef veritabanında Bunu yapmak için betikler (.sql dosyaları) oluşturabilir ve bu betikleri ASP.NET uygulamasının Web Dağıtım paketine dahil edilebilir. Daha fazla bilgi için [nasıl yapılır: Bir Web uygulaması projesi ile bir veritabanı dağıtma](https://docs.microsoft.com/previous-versions/dd465343(v=vs.100)). Bir ASP.NET Web sitesi için kullanarak bunu yapabilirsiniz **Database Publishing Wizard** Visual Studio'da. Daha fazla bilgi için [bir SQL veritabanı yayımlama](https://docs.microsoft.com/previous-versions/aspnet/bb907585(v=vs.100)).

- WCF Veri Hizmetleri temel bir WCF uygulaması içerdiğinden, Windows Server üzerinde çalışan IIS'ye Dağıtılmış veri hizmetini izlemek için Windows Server Appfabric'i kullanabilirsiniz. Veri hizmetini izlemek için Windows Server AppFabric kullanma hakkında daha fazla bilgi için gönderiye bakın [Windows Server AppFabric ile WCF veri hizmetlerini izleme](https://go.microsoft.com/fwlink/?LinkID=202005).

## <a name="see-also"></a>Ayrıca bkz.

- [Veri Hizmeti Barındırma](../../../../docs/framework/data/wcf/hosting-the-data-service-wcf-data-services.md)
- [WCF Veri Hizmetlerinin Güvenliğini Sağlama](../../../../docs/framework/data/wcf/securing-wcf-data-services.md)
- [WCF Veri Hizmetlerini Tanımlama](../../../../docs/framework/data/wcf/defining-wcf-data-services.md)
