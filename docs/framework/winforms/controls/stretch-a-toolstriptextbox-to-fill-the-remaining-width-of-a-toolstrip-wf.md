---
title: "Nasıl yapılır: Bir toolstrip'nin kalan genişliğini (Windows Forms) doldurmak için"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text boxes [Windows Forms], stretching in ToolStrip control [Windows Forms]
- ToolStrip control [Windows Forms], stretching a text box
ms.assetid: 0e610fbf-85fe-414c-900c-9704a5dd5cc6
ms.openlocfilehash: 7a9fd703206caadf2d9c63d92567f8b1c3b51e61
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64751425"
---
# <a name="how-to-stretch-a-toolstriptextbox-to-fill-the-remaining-width-of-a-toolstrip-windows-forms"></a>Nasıl yapılır: Bir toolstrip'nin kalan genişliğini (Windows Forms) doldurmak için
Ayarladığınızda <xref:System.Windows.Forms.ToolStrip.Stretch%2A> özelliği bir <xref:System.Windows.Forms.ToolStrip> denetimini `true`, denetimi uçtan uca, kapsayıcı doldurur ve kapsayıcısı boyutlandırdığında yeniden boyutlandırır. Bu yapılandırmada, bir öğesi denetiminde gibi esnetme yararlı bir <xref:System.Windows.Forms.ToolStripTextBox>kullanılabilir alanı dolduracak şekilde ve denetim boyutlandırdığında yeniden boyutlandırabilirsiniz. Görünümünü ve davranışını Microsoft® Internet Explorer Adres çubuğuna benzer elde etmek istiyorsanız bu uzatma gibi yararlı olur.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği, türetilen bir sınıf sağlar <xref:System.Windows.Forms.ToolStripTextBox> adlı `ToolStripSpringTextBox`. Bu sınıf geçersiz kılmalar <xref:System.Windows.Forms.ToolStripTextBox.GetPreferredSize%2A> üst kullanılabilir genişliğini hesaplamak için gereken yöntemini <xref:System.Windows.Forms.ToolStrip> diğer tüm öğelerin birleşik genişliğini çıkarılmasıyla denetim. Bu kod örneği de sağlayan bir <xref:System.Windows.Forms.Form> sınıfı ve bir `Program` yeni davranış göstermek için sınıf.  
  
 [!code-csharp[ToolStripSpringTextBox#00](~/samples/snippets/csharp/VS_Snippets_Winforms/ToolStripSpringTextBox/cs/ToolStripSpringTextBox.cs#00)]
 [!code-vb[ToolStripSpringTextBox#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ToolStripSpringTextBox/vb/ToolStripSpringTextBox.vb#00)]  
  
## <a name="compiling-the-code"></a>Kod Derleniyor  
 Bu örnek gerektirir:  
  
- Sistem, System.Drawing ve System.Windows.Forms derlemelere başvuruları.  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.Stretch%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.ToolStripTextBox>
- <xref:System.Windows.Forms.ToolStripTextBox.GetPreferredSize%2A?displayProperty=nameWithType>
- [ToolStrip Denetim, Mimarisi](toolstrip-control-architecture.md)
- [Nasıl yapılır: Bir StatusStrip içinde Spring özelliğini etkileşimli kullanma](how-to-use-the-spring-property-interactively-in-a-statusstrip.md)
