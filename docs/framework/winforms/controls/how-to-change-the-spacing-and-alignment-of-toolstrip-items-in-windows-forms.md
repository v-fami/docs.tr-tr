---
title: "Nasıl yapılır: Windows Forms'da ToolStrip Öğelerinin Aralık ve Hizalamasını Değiştirme"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], aligning items
- examples [Windows Forms], toolbars
- toolbars [Windows Forms], aligning items
ms.assetid: cd483466-0f49-43df-addf-e2b5fcd64027
ms.openlocfilehash: c7a874659be8dbaec66b78e1e065bcbec21da3b4
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64650872"
---
# <a name="how-to-change-the-spacing-and-alignment-of-toolstrip-items-in-windows-forms"></a>Nasıl yapılır: Windows Forms'da ToolStrip Öğelerinin Aralık ve Hizalamasını Değiştirme
<xref:System.Windows.Forms.ToolStrip> Denetimi boyutlandırma, aralıkları gibi düzen özellikleri tam olarak destekler <xref:System.Windows.Forms.ToolStripItem> denetimleri birbirine göre denetimlerin düzenlemesini üzerinde <xref:System.Windows.Forms.ToolStrip>ve denetimleri göreli aralığını <xref:System.Windows.Forms.ToolStrip>.  
  
 Çünkü varsayılan değerini <xref:System.Windows.Forms.ToolStripItem.AutoSize%2A> özelliği `true`, denetimleri boyutta otomatik olarak ayarlamadığınız sürece <xref:System.Windows.Forms.ToolStripItem.AutoSize%2A> özelliğini `false`.  
  
### <a name="to-manually-size-a-toolstripitem"></a>El ile ToolStripItem boyutlandırmak için  
  
1. Ayarlama <xref:System.Windows.Forms.ToolStripItem.AutoSize%2A> özelliğini `false` ilişkili denetimi.  
  
    ```vb  
    ToolStripButton1.AutoSize = False  
    ```  
  
    ```csharp  
    toolStripButton1.AutoSize = false;  
    ```  
  
2. Ayarlama <xref:System.Windows.Forms.ToolStripItem.Size%2A> özelliği ilişkili için istediğiniz şekilde <xref:System.Windows.Forms.ToolStripItem>.  
  
### <a name="to-set-the-spacing-of-a-toolstripitem"></a>ToolStripItem aralığını ayarlamak için  
  
1. Piksel cinsinden istenen değerleri eklemek <xref:System.Windows.Forms.ToolStripItem.Margin%2A> ilişkili denetiminin özelliği.  
  
     Değerlerini <xref:System.Windows.Forms.ToolStripItem.Margin%2A> özelliği şu sırayla bitişik öğelerin ve öğe aralığını belirtin: Sol, üst, sağ ve alt.  
  
    ```vb  
    ToolStripTextBox1.Margin = New System.Windows.Forms.Padding _  
        (3, 0, 3, 0)  
    ```  
  
    ```csharp  
    toolStripTextBox1.Margin = new System.Windows.Forms.Padding   
        (3, 0, 3, 0);  
    ```  
  
### <a name="to-align-a-toolstripitem-to-the-right-side-of-the-toolstrip"></a>ToolStrip sağ tarafına ToolStripItem hizalamak için  
  
1. Ayarlama <xref:System.Windows.Forms.ToolStripItem.Alignment%2A> özelliğini <xref:System.Windows.Forms.ToolStripItemAlignment.Right> ilişkili denetimi. Varsayılan olarak, <xref:System.Windows.Forms.ToolStripItem.Alignment%2A> ayarlanır <xref:System.Windows.Forms.ToolStripItemAlignment.Left>, denetimleri sol tarafıyla hizalar <xref:System.Windows.Forms.ToolStrip>.  
  
    ```vb  
    ToolStripSplitButton1.Alignment = _  
        System.Windows.Forms.ToolStripItemAlignment.Right  
    ```  
  
    ```csharp  
    toolStripSplitButton1.Alignment =   
        System.Windows.Forms.ToolStripItemAlignment.Right;  
    ```  
  
### <a name="to-arrange-toolstrip-items-on-the-toolstrip"></a>ToolStrip öğeler şeridindeki düzenlemek için  
  
- Ayarlama <xref:System.Windows.Forms.ToolStrip.LayoutStyle%2A> değere <xref:System.Windows.Forms.ToolStripLayoutStyle> istediğiniz.  
  
    ```vb  
    ToolStripDropDown1.LayoutStyle = _  
        System.Windows.Forms.ToolStripLayoutStyle.Flow  
    ```  
  
    ```csharp  
    toolStripDropDown1.LayoutStyle =   
        System.Windows.Forms.ToolStripLayoutStyle.Flow;  
    ```  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.Control.Layout>
- <xref:System.Windows.Forms.ToolStrip.LayoutCompleted>
- <xref:System.Windows.Forms.ToolStrip.LayoutSettings%2A>
- <xref:System.Windows.Forms.ToolStripItem.TextImageRelation%2A>
- <xref:System.Windows.Forms.ToolStripItem.Placement%2A>
- <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A>
- [ToolStrip Denetimine Genel Bakış](toolstrip-control-overview-windows-forms.md)
- [ToolStrip Denetim, Mimarisi](toolstrip-control-architecture.md)
- [ToolStrip Teknoloji Özeti](toolstrip-technology-summary.md)
