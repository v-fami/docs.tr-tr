---
title: Visual Basic'te Bileşenler Oluşturma ve Kullanma
ms.date: 07/20/2015
helpviewer_keywords:
- components [Visual Basic]
ms.assetid: ee6a4156-73f7-4e9b-8e01-c74c4798b65c
ms.openlocfilehash: 5f130c4de45f81dfb21c8c87c9e24d22cd4276ce
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65586733"
---
# <a name="creating-and-using-components-in-visual-basic"></a>Visual Basic'te Bileşenler Oluşturma ve Kullanma
A *bileşen* uygulayan bir sınıf <xref:System.ComponentModel.IComponent?displayProperty=nameWithType> arabirimi ya da uygulayan bir sınıftan türetilen doğrudan veya dolaylı olarak <xref:System.ComponentModel.IComponent>. .NET Framework bileşenini yeniden kullanılabilir, diğer nesnelerle etkileşim kurabilir ve dış kaynaklara ve tasarım zamanı desteği üzerinde denetim sağlayan bir nesnedir.  
  
 Bileşenlerin önemli bir özelliği, bir bileşen olan bir sınıf için Visual Studio tümleşik geliştirme ortamında kullanılabilir anlamına gelir designable, olmasıdır. Bir bileşen araç çubuğu, sürüklenen formunuza bırakılan ve tasarım yüzeyinde yönetilebilir. .NET Framework'e bileşenleri için temel tasarım zamanı desteği yerleşik olarak dikkat edin. bir bileşen geliştirici, temel tasarım zamanı işlevselliği yararlanmak için ek bir iş yapmak yok.  
  
 A *denetimi* bileşene, her ikisi de designable gibi benzer. Ancak, bir bileşenin sağlamadığı durumdayken bir kullanıcı arabirimi bir denetim sağlar. Bir denetim temel denetim sınıflarının birinden türetilmelidir: <xref:System.Windows.Forms.Control> veya <xref:System.Web.UI.Control>.  
  
## <a name="when-to-create-a-component"></a>Bir bileşen oluşturma zamanı  
 Sınıfınızın bir tasarım yüzeyi (örneğin, Web Forms Tasarımcısı ve Windows Forms) ancak hiçbir kullanıcı arabirimi olan üzerinde kullanılacaksa, bir bileşen verilecek ve uygulamak <xref:System.ComponentModel.IComponent>, veya doğrudan veya dolaylı olarak uygulayan bir sınıftan türetilen <xref:System.ComponentModel.IComponent>.  
  
 <xref:System.ComponentModel.Component> Ve <xref:System.ComponentModel.MarshalByValueComponent> sınıflardır, temel uygulamaları <xref:System.ComponentModel.IComponent> arabirimi. Bu sınıflar arasındaki ana fark <xref:System.ComponentModel.Component> sınıfı başvuruya göre sıralanmış sırada <xref:System.ComponentModel.IComponent> değere göre sıralanır. Aşağıdaki listede uygulayıcıları için sunduğu geniş kapsamlı yönergeler sağlar.  
  
- Bileşeniniz başvuruya göre sıralanması gerekiyorsa türetilen <xref:System.ComponentModel.Component>.  
  
- Bileşeniniz değere göre sıralanması gerekiyorsa türetilen <xref:System.ComponentModel.MarshalByValueComponent>.  
  
- Tek devralma nedeniyle temel uygulamaları birinden bileşeniniz türetilemez, uygulama <xref:System.ComponentModel.IComponent>.  
  
## <a name="component-classes"></a>Bileşen Sınıfları  
 <xref:System.ComponentModel> Ad alanı, bileşenlerin ve denetimlerin çalışma zamanı ve tasarım zamanı davranışını uygulamak için kullanılan sınıfları sağlar. Bu ad alanı, sınıflar ve öznitelikler ve tür dönüştürücüleri uygulama, veri kaynaklarını bağlama ve bileşenleri lisanslama arabirimler içerir.  
  
 Çekirdek Bileşen sınıfları şunlardır:  
  
- <xref:System.ComponentModel.Component>. Temel bir uygulama için <xref:System.ComponentModel.IComponent> arabirimi. Bu sınıf, uygulamalar arasında paylaşma nesnesi sağlar.  
  
- <xref:System.ComponentModel.MarshalByValueComponent>. Temel bir uygulama için <xref:System.ComponentModel.IComponent> arabirimi.  
  
- <xref:System.ComponentModel.Container>. Temel uygulama <xref:System.ComponentModel.IContainer> arabirimi. Bu sınıf, sıfır veya daha fazla bileşen kapsüller.  
  
 Bileşen Lisanslamayı için kullanılan sınıflar bazıları şunlardır:  
  
- <xref:System.ComponentModel.License>. Tüm lisansları için soyut temel sınıf. Bir bileşenin belirli bir örneği için bir lisans verilir.  
  
- <xref:System.ComponentModel.LicenseManager>. Özellikleri ve yöntemleri bileşene bir lisans eklemek ve yönetmenize olanak sağlayan bir <xref:System.ComponentModel.LicenseProvider>.  
  
- <xref:System.ComponentModel.LicenseProvider>. Bir lisans sağlayıcısı uygulamak için soyut temel sınıf.  
  
- <xref:System.ComponentModel.LicenseProviderAttribute>. Belirtir <xref:System.ComponentModel.LicenseProvider> sınıfı ile kullanmak için sınıf.  
  
 Açıklayan ve bileşenleri kalıcı hale getirmeniz için yaygın olarak kullanılan sınıflar.  
  
- <xref:System.ComponentModel.TypeDescriptor>. Öznitelikler, özellikler ve olaylar gibi bir bileşen için özellikleri hakkında bilgi sağlar.  
  
- <xref:System.ComponentModel.EventDescriptor>. Bir olay hakkında bilgi sağlar.  
  
- <xref:System.ComponentModel.PropertyDescriptor>. Bir özellik hakkında bilgi sağlar.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Denetim ve Bileşen Yazmada Sorun Giderme](../../framework/winforms/controls/troubleshooting-control-and-component-authoring.md)  
 Sık karşılaşılan sorunları düzeltmek açıklanmaktadır.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Windows Forms'ta erişim tasarım zamanı desteği](../../framework/winforms/controls/developing-windows-forms-controls-at-design-time.md)
