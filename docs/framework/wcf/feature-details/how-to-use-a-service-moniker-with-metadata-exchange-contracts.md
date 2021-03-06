---
title: 'Nasıl yapılır: Meta Veri Değişimi Sözleşmeleriyle Hizmet Bilinen Adı Kullanma'
ms.date: 03/30/2017
ms.assetid: c41a07e5-cb9d-45d6-9ea4-34511e227faf
ms.openlocfilehash: 367cbd4a2bfbde3d4ab0a74eeeaf5d5f5662ec27
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61972906"
---
# <a name="how-to-use-a-service-moniker-with-metadata-exchange-contracts"></a>Nasıl yapılır: Meta Veri Değişimi Sözleşmeleriyle Hizmet Bilinen Adı Kullanma
Yeni bazı WCF hizmetlerinde geliştirme sonra bir komut dosyası veya Visual Basic 6.0 bir uygulamadan bu hizmetleri çağıran mümkün olmasını istediğiniz karar verebilirsiniz. Bir WCF istemcisi derleme oluşturma, derleme COM ile kaydetme, derlemeyi GAC'ye yüklemek ve ardından, Visual Basic kodundan başvuru COM türleri için bir yöntem olacaktır. Uygulamayı dağıtırken de WCF istemci bütünleştirilmiş kodu dağıtmak gerekecektir. Ardından, kullanıcı WCF istemci derleme COM ile kaydetme ve GAC'de yerleştirme sahip olur. WCF COM birlikte çalışma bir WCF istemcisi derleme üzerinde bağlı olmadan aynı hizmet çağrıları yapmanıza olanak sağlar. WCF bilinen adını bir meta veri değişimi (Mex) uç noktası türü ayıklamak için hizmet bilinen adı kullanan bir URI belirterek herhangi bir WCF Hizmeti (Visual Basic, VBScript, Visual Basic for Applications (VBA) ve benzeri) herhangi bir COM uyumlu dil çağırmanızı sağlar. hizmeti hakkında bilgi. Bu konu, bir Mex uç noktasını belirtir bir WCF bilinen adını kullanarak çalışmaya WCF başlama örneği çağırmak açıklar.  
  
> [!NOTE]
>  WCF istemci derlemesi tarafından tanımlanan türler gerçekten hiçbir zaman örneği oluşturulur. Derleme yalnızca meta veriler için kullanılır.  
  
### <a name="using-the-service-moniker-with-a-mex-address"></a>Bir Mex adresa ile hizmet bilinen adı kullanma  
  
1. Başlarken örneği oluşturmak ve kendi URL'sine göz atmak için Internet Explorer'ı kullanın (http://localhost/ServiceModelSamples/Service.svc) hizmetinin çalıştığından emin olmak için.  
  
2. Visual Basic komut dosyası veya aşağıdaki kodu içeren bir Visual Basic uygulama oluşturun:  
  
    ```  
    monString = "service:mexaddress=http://localhost/ServiceModelSamples/Service.svc/MEX"  
    monString = monString + ", address=http://localhost/ServiceModelSamples/Service.svc"  
    monString = monString + ", contract=ICalculator, contractNamespace=http://Microsoft.ServiceModel.Samples"  
    monString = monString + ", binding=WSHttpBinding_ICalculator, bindingNamespace=http://Microsoft.ServiceModel.Samples"  
  
    Set calc = GetObject(monString)  
    MsgBox calc.Add(3, 4)  
    ```  
  
3. Visual Basic uygulama veya betik çalıştırın.  
  
    > [!NOTE]
    >  Aradığınız hizmet, hizmetten bulunan meta verileri okuyabilmesi bilinen ad için bir Mex uç noktasını açığa çıkarmalıdır. Daha fazla bilgi için [nasıl yapılır: Bir yapılandırma dosyası kullanarak bir hizmet için meta verileri yayımlama](../../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md).  
  
    > [!NOTE]
    >  Bilinen ad hatalı veya hizmet kullanılamıyor durumunda çağrısı `GetObject` "Geçersiz sözdizimi." belirten bir hata döndürür  Bu hata iletisini alırsanız kullandığınız ad doğru olduğundan ve hizmetin kullanılabilir olduğundan emin olun.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Windows Communication Foundation Hizmeti bilinen adını kaydolmadan kullanma](../../../../docs/framework/wcf/feature-details/use-the-wcf-service-moniker-without-registration.md)
- [Nasıl yapılır: WSDL sözleşmeleriyle hizmet bilinen adı kullanma](../../../../docs/framework/wcf/feature-details/how-to-use-a-service-moniker-with-wsdl-contracts.md)
