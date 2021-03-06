---
title: 'Nasıl yapılır: WorkflowServiceHost ile Boşta Davranışı Yapılandırma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1bb93652-d687-46ff-bff6-69ecdcf97437
ms.openlocfilehash: 5b2ebf6ddc5f275bd499a8abf7e68e019a1e0cef
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64586682"
---
# <a name="how-to-configure-idle-behavior-with-workflowservicehost"></a>Nasıl yapılır: WorkflowServiceHost ile Boşta Davranışı Yapılandırma
İş akışı örneği kullanarak teslim edilecek bir ileti için beklediği sırada örneğin dış bazı stimulus tarafından sürdürülmesini bir yer işareti karşılaştıkları olduğunda iş akışları boş Git bir <xref:System.ServiceModel.Activities.Receive> etkinlik. <xref:System.ServiceModel.Activities.Description.WorkflowIdleBehavior> bir hizmet örneği boşta gittiğinde arasında ve örneği kalıcı ya da kaldırıldığında zaman belirtmenizi sağlar bir davranıştır. Bu, bu zaman aralıkları ayarlamanıza olanak tanır, iki özellik içerir. <xref:System.ServiceModel.Activities.Description.WorkflowIdleBehavior.TimeToPersist%2A> bir iş akışı hizmet örneği boşta gittiğinde ve ne zaman iş akışı hizmet örneği kalıcıdır arasındaki zaman aralığını belirtir. <xref:System.ServiceModel.Activities.Description.WorkflowIdleBehavior.TimeToUnload%2A> İş akışı hizmet örneği kaldırıldığında, burada kaldırma örnek deposuna örneği kalıcı ve bellekten kaldırılıyor anlamına gelir ve ne zaman bir iş akışı hizmet örneği arasındaki zaman aralığını boşta giden belirtir. Bu konu nasıl yapılandırılacağını açıklar <xref:System.ServiceModel.Activities.Description.WorkflowIdleBehavior> bir yapılandırma dosyası.  
  
### <a name="to-configure-workflowidlebehavior"></a>WorkflowIdleBehavior yapılandırmak için  
  
1. Ekleme bir <`workflowIdle`> öğesi <`behavior`> öğesi içinde <`serviceBehaviors`> Aşağıdaki örnekte gösterildiği gibi bir öğe.  
  
    ```xml  
    <behaviors>  
      <serviceBehaviors>  
        <behavior name="">  
          <workflowIdle timeToUnload="0:05:0" timeToPersist="0:04:0"/>   
        </behavior>  
      </serviceBehaviors>  
    </behaviors>  
    ```  
  
     `timeToUnload` Özniteliği, bir iş akışı hizmet örneği boşta gittiğinde ve iş akışı hizmeti yüklenmemiş olduğunda arasındaki süreyi belirtir. `timeToPersist` Özniteliği, bir iş akışı hizmet örneği boşta gittiğinde ve ne zaman iş akışı hizmet örneği kalıcıdır arasındaki süreyi belirtir. İçin varsayılan değer `timeToUnload` 1 dakikadır. İçin varsayılan değer `timeToPersist` olduğu <xref:System.TimeSpan.MaxValue>. Boşta örnekleri bellekte tut ancak sağlamlık için kalıcı hale getirmek istiyorsanız, değerleri ayarlamak için `timeToPersist`  <  `timeToUnload`. Öğesinden kaldırılıyor boşta örnekleri önlemek istiyorsanız `timeToUnload` için <xref:System.TimeSpan.MaxValue>. Hakkında daha fazla bilgi için <xref:System.ServiceModel.Activities.Description.WorkflowIdleBehavior>, bkz: [iş akışı hizmeti konak genişletilebilirliği](../../../../docs/framework/wcf/feature-details/workflow-service-host-extensibility.md)  
  
    > [!NOTE]
    >  Önceki yapılandırma örneği Basitleştirilmiş yapılandırma kullanıyor. Daha fazla bilgi için [Basitleştirilmiş yapılandırma](../../../../docs/framework/wcf/simplified-configuration.md).  
  
### <a name="to-change-idle-behavior-in-code"></a>Kodda boşta davranışı değiştirmek için  
  
- Aşağıdaki örnekte, program aracılığıyla kaldırma ve devam ettirmeden önce beklenecek süreyi değiştirir.  
  
     [!code-csharp[Wf_SvcHost_Idle_persist#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/wf_svchost_idle_persist/cs/source.cs#1)]
     [!code-vb[Wf_SvcHost_Idle_persist#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/wf_svchost_idle_persist/vb/source.vb#1)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [İş Akışı Hizmeti Konak Genişletilebilirliği](../../../../docs/framework/wcf/feature-details/workflow-service-host-extensibility.md)
- [Basitleştirilmiş Yapılandırma](../../../../docs/framework/wcf/simplified-configuration.md)
- [İş Akışı Hizmetleri](../../../../docs/framework/wcf/feature-details/workflow-services.md)
