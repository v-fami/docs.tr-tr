---
title: 'Nasıl yapılır: Denetimi Formların Kenarlarına Hizalama'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Dock property [Windows Forms], aligning controls (using code)
- forms [Windows Forms], aligning controls
- controls [Windows Forms], aligning on forms
- custom controls [Windows Forms], docking using code
ms.assetid: 5994cb59-242b-4e75-bd0e-62879c34d702
ms.openlocfilehash: beb8881dbd2aedaefe66510c2942ce6c082b9729
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59329979"
---
# <a name="how-to-align-a-control-to-the-edges-of-forms"></a>Nasıl yapılır: Denetimi Formların Kenarlarına Hizalama
Denetiminiz ayarlayarak formlarınızı kenarına hizalama yapabileceğiniz <xref:System.Windows.Forms.Control.Dock%2A> özelliği. Bu özellik, denetimi forma bulunduğu belirler. <xref:System.Windows.Forms.Control.Dock%2A> Özelliği aşağıdaki değerlere ayarlanabilir:  
  
|Ayar|Denetiminiz etkisi|  
|-------------|----------------------------|  
|<xref:System.Windows.Forms.DockStyle.Bottom>|Formun altına noktaları.|  
|<xref:System.Windows.Forms.DockStyle.Fill>|Formdaki tüm kalan alanı doldurur.|  
|<xref:System.Windows.Forms.DockStyle.Left>|Formun sol tarafına noktaları.|  
|<xref:System.Windows.Forms.DockStyle.None>|Her yerden ve bunu görünür tarafından belirtilen konumda dock yoksa kendi <xref:System.Windows.Forms.Control.Location%2A> özelliği.|  
|<xref:System.Windows.Forms.DockStyle.Right>|Formun sağ tarafına noktaları.|  
|<xref:System.Windows.Forms.DockStyle.Top>|Üst formun noktaları.|  
  
 Visual Studio'da bu özellik için tasarım zamanı desteği yoktur.  
  
### <a name="to-set-the-dock-property-for-your-control-at-run-time"></a>Çalışma zamanında denetiminizi Dock özelliğini ayarlamak için  
  
1. Ayarlama <xref:System.Windows.Forms.Control.Dock%2A> kodunda uygun değere özelliği.  
  
    ```vb  
    ' To set the Dock property internally.  
    Me.Dock = DockStyle.Top  
    ' To set the Dock property from another object.  
    UserControl1.Dock = DockStyle.Top  
    ```  
  
    ```csharp  
    // To set the Dock property internally.  
    this.Dock = DockStyle.Top;  
    // To set the Dock property from another object.  
    UserControl1.Dock = DockStyle.Top;  
    ```  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.Control.Dock%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.Anchor%2A?displayProperty=nameWithType>
- [.NET Framework ile Özel Windows Forms Denetimleri Geliştirme](developing-custom-windows-forms-controls.md)
- [Nasıl yapılır: Sabitleme ve FlowLayoutPanel denetiminde alt denetimleri yerleştirme](how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [Nasıl yapılır: Sabitleme ve TableLayoutPanel denetiminde alt denetimleri yerleştirme](how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [AutoSize Özelliğine Genel Bakış](autosize-property-overview.md)
