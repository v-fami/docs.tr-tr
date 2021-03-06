---
title: 'Nasıl yapılır: RichTextBox İçinde Özel Açılır Menü Konumlandırma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom context menus [WPF], positioning
- positioning custom context menus [WPF]
- RichTextBox control [WPF], positioning custom context menus
- context menus [WPF], positioning
ms.assetid: bf77c930-a546-4573-9a56-9af345ba189a
ms.openlocfilehash: f9407f59c3daafd09fa5b84006f33ef2f3ebd31f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770831"
---
# <a name="how-to-position-a-custom-context-menu-in-a-richtextbox"></a>Nasıl yapılır: RichTextBox İçinde Özel Açılır Menü Konumlandırma
Bu örnek için bir özel bağlam menüsü konumlandırma nasıl gösterir bir <xref:System.Windows.Controls.RichTextBox>.  
  
 Özel bağlam menüsü için uyguladığınızda bir **RichTextBox**, bağlam menüsünü yerleşimini işlenmesinden sorumludur.  Varsayılan olarak, merkezde özel bağlam menüsü açıldığında **RichTextBox**.  
  
## <a name="example"></a>Örnek  
 Varsayılan yerleştirme davranışı geçersiz kılmak için için bir dinleyici eklemek <xref:System.Windows.FrameworkContentElement.ContextMenuOpening> olay.  Aşağıdaki örnekte, program aracılığıyla bunun nasıl yapılacağını gösterir.  
  
 [!code-csharp[RichTextBox_ContextMenu#_AddListener](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBox_ContextMenu/CSharp/app.xaml.cs#_addlistener)]
 [!code-vb[RichTextBox_ContextMenu#_AddListener](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBox_ContextMenu/VisualBasic/app.xaml.vb#_addlistener)]  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, karşılık gelen bir uygulamasını gösterir <xref:System.Windows.FrameworkContentElement.ContextMenuOpening> olay dinleyicisi.  
  
 [!code-csharp[RichTextBox_ContextMenu#_ListenerBody](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBox_ContextMenu/CSharp/app.xaml.cs#_listenerbody)]
 [!code-vb[RichTextBox_ContextMenu#_ListenerBody](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBox_ContextMenu/VisualBasic/app.xaml.vb#_listenerbody)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [RichTextBox Genel Bakış](richtextbox-overview.md)
- [TextBox Genel Bakış](textbox-overview.md)
