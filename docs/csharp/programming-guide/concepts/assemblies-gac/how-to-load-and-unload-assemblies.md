---
title: 'Nasıl yapılır: Yükleme ve yüklemelerini kaldırma derlemeleri (C#)'
ms.date: 07/20/2015
ms.assetid: 6a4f490f-3576-471f-9533-003737cad4a3
ms.openlocfilehash: 52f7173efe497ab286c607db681f256983adc077
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61703185"
---
# <a name="how-to-load-and-unload-assemblies-c"></a>Nasıl yapılır: Yükleme ve yüklemelerini kaldırma derlemeleri (C#)
Programınız tarafından başvurulan derlemeler otomatik olarak derleme zamanında yüklenir, ancak geçerli uygulama etki alanına çalışma zamanında belirli derlemeleri yüklemek mümkündür. Daha fazla bilgi için [nasıl yapılır: Bir uygulama etki alanına derlemeler yükleme](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md).  
  
 Tüm içerdiği uygulama etki alanlarının kaldırmadan tek bir derlemeyi kaldırmak için hiçbir yolu yoktur. Derleme kapsamı dışında kalsa bile içerdiği tüm uygulama etki alanları kaldırılana kadar gerçek derleme dosyası yüklü kalır.  
  
 Bazı derlemeler, ancak diğerlerini kaldırmak istiyorsanız, yeni bir uygulama etki alanı oluşturma, bu etki alanı içinde kod yürütme ve ardından, uygulama etki alanı kaldırılırken göz önünde bulundurun. Daha fazla bilgi için [nasıl yapılır: Bir uygulama etki alanını boşaltma](../../../../framework/app-domains/how-to-unload-an-application-domain.md).  
  
### <a name="to-load-an-assembly-into-an-application-domain"></a>Uygulama etki alanına bir derlemeyi yüklemek için  
  
1. Bazı yük sınıflarda yer yöntemleri kullanmak <xref:System.AppDomain> ve <xref:System.Reflection>. Daha fazla bilgi için [nasıl yapılır: Bir uygulama etki alanına derlemeler yükleme](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md).  
  
### <a name="to-unload-an-application-domain"></a>Uygulama etki alanını kaldırmak için  
  
1. Tüm içerdiği uygulama etki alanlarının kaldırmadan tek bir derlemeyi kaldırmak için hiçbir yolu yoktur. Kullanım `Unload` yönteminden <xref:System.AppDomain> uygulama etki alanları kaldırmak için. Daha fazla bilgi için [nasıl yapılır: Bir uygulama etki alanını boşaltma](../../../../framework/app-domains/how-to-unload-an-application-domain.md).  
  
## <a name="see-also"></a>Ayrıca bkz.

- [C# Programlama Kılavuzu](../../../../csharp/programming-guide/index.md)
- [.NET’te bütünleştirilmiş kodlar](../../../../standard/assembly/index.md)
- [Nasıl yapılır: Uygulama etki alanına derlemeler yükleme](../../../../framework/app-domains/how-to-load-assemblies-into-an-application-domain.md)
