---
title: WPF Denetimlerini Kullanma
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms Designer [Windows Forms], interoperability with WPF
- interoperability [WPF]
ms.assetid: 03c85dce-26ad-44cd-bc1d-8e0cb56de096
ms.openlocfilehash: 149a2da1303e6b801a439494254a416a38b145a7
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211308"
---
# <a name="use-wpf-controls"></a>WPF denetimlerini kullanma

Windows Forms tabanlı uygulamalarınızı Windows Presentation Foundation (WPF) denetimleri kullanabilirsiniz. Bu iki farklı görünümü teknolojileri olsa da, bunlar düzgün çalışmak.

Windows Form Tasarımcısı'nda Visual Studio, Windows Presentation Foundation denetimleri barındırma için bir görsel tasarım ortamı sağlar. Adlı bir özel Windows Forms denetimi tarafından barındırılan bir WPF denetiminde <xref:System.Windows.Forms.Integration.ElementHost>. WPF denetimi form düzeninde katılmak ve klavye ve fare iletileri almak için bu denetim sağlar. Tasarım zamanında düzenleyebilirsiniz <xref:System.Windows.Forms.Integration.ElementHost> herhangi bir Windows Forms denetimi gibi denetim.

WPF tabanlı uygulamalarınızı Windows Forms denetimleri de kullanabilirsiniz. Daha fazla bilgi için [Visual Studio'da XAML tasarım](/visualstudio/designers/designing-xaml-in-visual-studio).

## <a name="in-this-section"></a>Bu Bölümde

[Nasıl yapılır: Tasarım zamanında bir ElementHost denetimini yapıştırın](how-to-copy-and-paste-an-elementhost-control-at-design-time.md)\
Bir Windows formunda Windows Presentation Foundation denetim kopyalama işlemi gösterilmektedir.

[İzlenecek yol: Tasarım zamanında WPF içeriğini Windows Forms'ta düzenleme](walkthrough-arranging-wpf-content-on-windows-forms-at-design-time.md)\
Sabitleme ve dayama çizgileri, gibi Windows Forms düzeni özellikleri Windows Presentation Foundation denetimleri düzenlemek için nasıl kullanılacağını gösterir.

[İzlenecek yol: Windows Forms'ta tasarım zamanında yeni WPF içeriği oluşturma](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md)\
Windows Forms tabanlı uygulamalarda kullanmak için bir Windows Presentation Foundation denetim oluşturma işlemi gösterilmektedir.

[İzlenecek yol: Tasarım zamanında Windows Forms WPF içeriği atama](walkthrough-assigning-wpf-content-on-windows-forms-at-design-time.md)\
Formunuzda görüntülemek istediğiniz Windows Presentation Foundation denetim türlerini seçmek gösterilmektedir.

[İzlenecek yol: WPF içeriği için stil oluşturma](walkthrough-styling-wpf-content.md)\
Windows Form Tasarımcısı arasındaki iş akışını gösterir ve [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)] Windows Presentation Foundation denetimleri için stil uygulamak için.

## <a name="reference"></a>Başvuru

<xref:System.Windows.Forms.Integration.ElementHost>\
Windows Forms tabanlı uygulamalarınızı ana bilgisayar Windows Presentation Foundation denetimler için kullanabileceğiniz bir sınıfı tanımlar.

<xref:System.Windows.Forms.Integration.WindowsFormsHost>\
Ana bilgisayar Windows Forms denetimlerine Windows Presentation Foundation tabanlı uygulamanızda kullanabileceğiniz bir sınıfı tanımlar.

## <a name="related-sections"></a>İlgili bölümler

[Geçiş ve birlikte çalışabilirlik](../../wpf/advanced/migration-and-interoperability.md)\
Windows Presentation Foundation ve Windows Forms teknolojileri arasında birlikte çalışabilirliği açıklar.

[Visual Studio'da XAML tasarım](/visualstudio/designers/designing-xaml-in-visual-studio)\
Visual Studio'da Windows Presentation Foundation denetimleri tasarım açıklar.
