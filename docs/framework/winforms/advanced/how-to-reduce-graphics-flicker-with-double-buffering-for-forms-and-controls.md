---
title: 'Nasıl yapılır: Formlar ve Denetimler için İki Kez Arabelleğe Alma ile Grafik Titreşimini Azaltma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- flicker [Windows Forms], reducing in Windows Forms
- graphics [Windows Forms], reducing double-buffered flicker
ms.assetid: 91083d3a-653f-4f15-a467-0f37b2aa39d6
ms.openlocfilehash: d143d7ec87a214a900264e069b329ea28a92c3e9
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65590388"
---
# <a name="how-to-reduce-graphics-flicker-with-double-buffering-for-forms-and-controls"></a>Nasıl yapılır: Formlar ve Denetimler için İki Kez Arabelleğe Alma ile Grafik Titreşimini Azaltma
İki kez arabelleğe almayı bellek arabelleği birden çok Boya işlemleriyle ilişkili titreşimini sorunları ele almak için kullanır. İki kez arabelleğe alma etkinleştirildiğinde, tüm Boya işlemleri ilk ekranda çizim yüzeyi yerine bir arabelleğe işlenir. Tüm Boya işlemleri tamamlandıktan sonra doğrudan ilişkili çizim yüzeyi ara belleğe kopyalanır. Yalnızca bir grafik işlem ekranda gerçekleştirildiğinden, karmaşık boyama işlemleriyle ilişkili görüntü titremeyi ortadan kalkar. Çoğu uygulama için varsayılan çift .NET Framework tarafından sağlanan arabelleğe alma işlemini en iyi sonuçlar sağlar. Standart Windows Forms denetimleri, varsayılan olarak arabelleğe çift. Varsayılan arabelleğe almayı formlarınızı sıfırladığınızdan çift etkinleştirebilirsiniz ve iki yolla denetimleri yazıldı. Kümelerden yapabilirsiniz <xref:System.Windows.Forms.Control.DoubleBuffered%2A> özelliğini `true`, veya çağırabilirsiniz <xref:System.Windows.Forms.Control.SetStyle%2A> ayarlanacak yöntemi <xref:System.Windows.Forms.ControlStyles.OptimizedDoubleBuffer> bayrak `true`. Her iki yöntem de, varsayılan çift form veya denetim için arabelleğe almayı etkinleştir ve titreşimsiz grafik işleme sağlar. Çağırma <xref:System.Windows.Forms.Control.SetStyle%2A> yöntemi için yazdığınız tüm işleme kodu yalnızca fazla özel denetimler için önerilir.  
  
 Animasyon veya gelişmiş bellek yönetimi gibi daha gelişmiş çift arabelleğe alma senaryoları için kendi çift arabelleğe alma mantığını uygulayabilir. Daha fazla bilgi için [nasıl yapılır: Arabelleğe alınan grafikleri elle yönetme](how-to-manually-manage-buffered-graphics.md).  
  
### <a name="to-reduce-flicker"></a>Titreşimi azaltmak için  
  
- Ayarlama <xref:System.Windows.Forms.Control.DoubleBuffered%2A> özelliğini `true`.  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#31)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#31)]  
  
 \- veya -  
  
- Çağrı <xref:System.Windows.Forms.Control.SetStyle%2A> ayarlanacak yöntemi <xref:System.Windows.Forms.ControlStyles.OptimizedDoubleBuffer> bayrak `true`.  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#32](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#32)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#32](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#32)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.Control.DoubleBuffered%2A>
- <xref:System.Windows.Forms.Control.SetStyle%2A>
- [İki Kez Arabelleğe Alınan Grafikler](double-buffered-graphics.md)
- [Windows Forms’da Grafikler ve Çizim](graphics-and-drawing-in-windows-forms.md)
