---
title: 'Nasıl yapılır: Görselin Çizim İçeriğini Numaralandırma'
ms.date: 03/30/2017
helpviewer_keywords:
- retrieving the DrawingGroup value of a Visual [WPF]
- enumerating the contents of a Visual [WPF]
ms.assetid: 2974ddb3-2997-4713-8fd2-e93d549c58a8
ms.openlocfilehash: 4f0afc1075fe66c7f154fcef3cd883709db55316
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61947478"
---
# <a name="how-to-enumerate-drawing-content-of-a-visual"></a>Nasıl yapılır: Görselin Çizim İçeriğini Numaralandırma
<xref:System.Windows.Media.Drawing> Nesne içeriğini numaralandırma için nesne modeli sağlar bir <xref:System.Windows.Media.Visual>.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte <xref:System.Windows.Media.VisualTreeHelper.GetDrawing%2A> alınacak yöntemi <xref:System.Windows.Media.DrawingGroup> değerini bir <xref:System.Windows.Media.Visual> ve onu numaralandırır.  
  
> [!NOTE]
>  Görselin içeriklerini sıralanırken alınırken <xref:System.Windows.Media.Drawing> nesneleri ve vektör grafik yönerge listesi olarak işleme verileri temel alınan gösterimini değil. Daha fazla bilgi için [WPF Grafik işlemeye genel bakış](wpf-graphics-rendering-overview.md).  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMRetrieveDrawings](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/EnumerateDrawingsExample.xaml.cs#graphicsmmretrievedrawings)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Media.Drawing>
- <xref:System.Windows.Media.DrawingGroup>
- <xref:System.Windows.Media.VisualTreeHelper>
- [Çizim Nesnelerine Genel Bakış](drawing-objects-overview.md)
- [WPF Grafik İşlemeye Genel Bakış](wpf-graphics-rendering-overview.md)
