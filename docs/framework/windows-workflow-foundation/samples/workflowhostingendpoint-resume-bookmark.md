---
title: WorkflowHostingEndpoint Sürdürme Yer İşareti
ms.date: 03/30/2017
ms.assetid: a708064f-50b0-4751-b44e-d5410d08d451
ms.openlocfilehash: 3c1a3421c87d18e695790cfb3a1f066600748ce9
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64619503"
---
# <a name="workflowhostingendpoint-resume-bookmark"></a>WorkflowHostingEndpoint Sürdürme Yer İşareti
Bu örnek gösterir nasıl <xref:System.ServiceModel.Activities.WorkflowHostingEndpoint> kullanılabilir <xref:System.ServiceModel.Activities.WorkflowServiceHost> iş akışı örnekleri oluşturmak için.  
  
## <a name="demonstrates"></a>Gösteriler  
 <xref:System.ServiceModel.Activities.WorkflowHostingEndpoint>, <xref:System.ServiceModel.Activities.WorkflowServiceHost>  
  
## <a name="discussion"></a>Tartışma  
 Bu örnekte <xref:System.ServiceModel.Activities.WorkflowHostingEndpoint> barındırılan iş akışı örneği oluşturmak için <xref:System.ServiceModel.Activities.WorkflowServiceHost>. <xref:System.ServiceModel.Activities.WorkflowHostingEndpoint> bir genişletilebilirlik noktası <xref:System.ServiceModel.Activities.WorkflowServiceHost> aşağıdaki senaryolarda kullanılabilir:  
  
- Yeni iş akışı örnekleri oluşturma.  
  
- Bir iş akışı örneği yer işaretlerini sürdürme barındırılan bir <xref:System.ServiceModel.Activities.WorkflowServiceHost>.  
  
 Dahil olan örnek uç nokta işlemleri bir iş akışı oluşturmak ve bir örnek kimliği döndürmek için veya belirli bir kimliğe sahip bir örneğini oluşturmak için sağlayan bir sözleşme kullanıma sunar. Örnek konsol uygulaması oluşturan bir <xref:System.ServiceModel.Activities.WorkflowServiceHost> örnek temel iş akışı tanımıyla ve ekler bir `CreationEndpoint` konağa. Ardından `Create` işlemi yeni bir iş akışı örneği oluşturmak için uç nokta.  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>Ayarlamak için derleme ve örneği çalıştırma  
  
1. Çözümü oluşturun.  
  
2. Uygulamayı çalıştırın. `CreationEndpoint` Konsol örnek kimliği iş akışı örneği oluşturulduğunda içeren bir ileti gösterir. "Hello World!" iletisi yer işaretinin sürdürme başarılı iş akışı tarafından yazdırılır.  
  
> [!IMPORTANT]
>  Örnekler, makinenizde zaten yüklü. Devam etmeden önce şu (varsayılan) dizin denetleyin.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Bu dizin mevcut değilse Git [Windows Communication Foundation (WCF) ve .NET Framework 4 için Windows Workflow Foundation (WF) örnekleri](https://go.microsoft.com/fwlink/?LinkId=150780) tüm Windows Communication Foundation (WCF) indirmek için ve [!INCLUDE[wf1](../../../../includes/wf1-md.md)] örnekleri. Bu örnek, şu dizinde bulunur.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Execution\ResumeBookmarkEndpoint`
