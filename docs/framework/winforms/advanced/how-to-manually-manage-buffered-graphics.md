---
title: 'Nasıl yapılır: Arabelleğe Alınan Grafikleri Elle Yönetme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- flicker [Windows Forms], reducing by manually managing graphics
- graphics [Windows Forms], managing buffered
ms.assetid: 4c2a90ee-bbbe-4ff6-9170-1b06c195c918
ms.openlocfilehash: 2cdcebd4e47996841ad58213d9c6252a6a3dd7b6
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65591842"
---
# <a name="how-to-manually-manage-buffered-graphics"></a>Nasıl yapılır: Arabelleğe Alınan Grafikleri Elle Yönetme
Daha gelişmiş çift arabelleğe alma senaryolar için .NET Framework sınıfları kendi iki kez arabelleğe alma mantığını uygulamak için kullanabilirsiniz. Ayırma ve tek bir grafik arabellekleri yönetmekten sorumlu bir sınıfı <xref:System.Drawing.BufferedGraphicsContext> sınıfı. Her uygulamanın kendi varsayılan sahip <xref:System.Drawing.BufferedGraphicsContext> , yöneten tüm çift bu uygulama için arabelleğe varsayılan. Çağırarak bu örneğe bir başvuru alabilirsiniz <xref:System.Drawing.BufferedGraphicsManager.Current%2A>.  
  
### <a name="to-obtain-a-reference-to-the-default-bufferedgraphicscontext"></a>BufferedGraphicsContext varsayılan bir başvuru almak için  
  
- Ayarlama <xref:System.Drawing.BufferedGraphicsManager.Current%2A> özelliği, aşağıdaki kod örneğinde gösterildiği gibi.  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#11)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#11)]  
  
    > [!NOTE]
    >  Çağrı gerekmez `Dispose` metodunda <xref:System.Drawing.BufferedGraphicsContext> , alırsınız başvuru <xref:System.Drawing.BufferedGraphicsManager> sınıfı. <xref:System.Drawing.BufferedGraphicsManager> Tüm bellek ayırma ve dağıtım için varsayılan işleme <xref:System.Drawing.BufferedGraphicsContext> örnekleri.  
  
     Animasyon gibi grafik açısından yoğun uygulamalar için bazen bir adanmış kullanarak performansı artırabilir <xref:System.Drawing.BufferedGraphicsContext> yerine <xref:System.Drawing.BufferedGraphicsContext> tarafından sağlanan <xref:System.Drawing.BufferedGraphicsManager>. Bu, oluşturmak ve uygulama tarafından kullanılan bellek daha büyük olacaktır ancak uygulamanız ile ilişkili tüm diğer arabelleğe alınan grafikleri yönetme performans yükü olmaksızın grafik arabellekleri tek tek yönetmek sağlar.  
  
### <a name="to-create-a-dedicated-bufferedgraphicscontext"></a>Adanmış BufferedGraphicsContext oluşturmak için  
  
- Bildirme ve yeni bir örneğini oluşturma <xref:System.Drawing.BufferedGraphicsContext> , aşağıdaki kod örneğinde gösterildiği gibi sınıf.  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#12)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#12)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Drawing.BufferedGraphicsContext>
- [İki Kez Arabelleğe Alınan Grafikler](double-buffered-graphics.md)
- [Nasıl yapılır: Arabelleğe alınan grafikleri elle işleme](how-to-manually-render-buffered-graphics.md)
