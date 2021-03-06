---
title: "Nasıl yapılır: Var olan bir varlığa (WCF Veri Hizmetleri) Dataservicecontext'e ekleme"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, changing data
ms.assetid: e3f2d71d-434c-4e98-91c3-95adae4702b6
ms.openlocfilehash: 511a9bc5352e208697460364e463330fc0ef611a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61793399"
---
# <a name="how-to-attach-an-existing-entity-to-the-dataservicecontext-wcf-data-services"></a>Nasıl yapılır: Var olan bir varlığa (WCF Veri Hizmetleri) Dataservicecontext'e ekleme
Bir varlık içinde veri hizmeti, zaten mevcut olduğunda [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] istemci kitaplığı sağlar, doğrudan varlığı temsil eden bir nesne iliştirmek <xref:System.Data.Services.Client.DataServiceContext> ilk bir sorgu yürütme. Daha fazla bilgi için [veri hizmetini güncelleştirme](../../../../docs/framework/data/wcf/updating-the-data-service-wcf-data-services.md).  
  
 Bu konudaki örnek Northwind örnek veri hizmeti ve otomatik olarak oluşturulan istemci veri hizmeti sınıfları kullanır. Bu hizmet ve istemci veri sınıfları tamamladığınızda oluşturulur [WCF Veri Hizmetleri Hızlı Başlangıç](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, var olan bir oluşturma işlemi gösterilmektedir `Customer` veri hizmetine kaydedilecek değişiklikler içeren nesne. Bir nesne bağlamına bağlı olduğu ve <xref:System.Data.Services.Client.DataServiceContext.UpdateObject%2A> ekli nesnesi olarak işaretlemek için yöntemi çağrıldığında <xref:System.Data.Services.Client.EntityStates.Modified> önce <xref:System.Data.Services.Client.DataServiceContext.SaveChanges%2A> yöntemi çağrılır.  
  
 [!code-csharp[Astoria Northwind Client#AttachObject](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_client/cs/source.cs#attachobject)]
 [!code-vb[Astoria Northwind Client#AttachObject](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_client/vb/source.vb#attachobject)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [WCF Veri Hizmetleri İstemci Kitaplığı](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md)
