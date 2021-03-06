---
title: 'Nasıl yapılır: Windows Forms DataGridView Denetiminde Veri Biçimlendirmeyi Özelleştirme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], formatting data
- DataGridView control [Windows Forms], cell styles
- cells [Windows Forms], changing colors in DataGridView control [Windows Forms]
- colors [Windows Forms], changing in DataGridView control [Windows Forms]
- data [Windows Forms], formatting in DataGridView control
- DataGridView control [Windows Forms], cell customization
- DataGridView control [Windows Forms], changing cell colors
- Windows Forms, changing colors of DataGridView cells
- DataGridView control [Windows Forms], substituting cell values for display
- data grids [Windows Forms], formatting data
ms.assetid: a6e72c70-ce18-425f-828d-d57be6f96ab6
ms.openlocfilehash: 948e9bf485b42b445491a4da9f8de7ae7974075c
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65592830"
---
# <a name="how-to-customize-data-formatting-in-the-windows-forms-datagridview-control"></a>Nasıl yapılır: Windows Forms DataGridView Denetiminde Veri Biçimlendirmeyi Özelleştirme
Aşağıdaki kod örneği için bir işleyici uygulamak gösterilmiştir <xref:System.Windows.Forms.DataGridView.CellFormatting?displayProperty=nameWithType> hücreler, sütunlar ve değerler bağlı olarak nasıl görüntüleneceğini değiştiren olay.  
  
 İçinde hücreleri `Balance` negatif sayıları içeren sütun, kırmızı bir arka plan verilmiştir. Bu hücre parantezler negatif değerleri görüntülemek için para birimi olarak da biçimlendirebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Verileri biçimlendirme Windows Forms DataGridView denetiminde](how-to-format-data-in-the-windows-forms-datagridview-control.md).  
  
 İçinde hücreleri `Priority` metinsel karşılık gelen yerine sütun ekran görüntüleri hücre değerleri. <xref:System.Windows.Forms.ConvertEventArgs.Value%2A> Özelliği <xref:System.Windows.Forms.DataGridViewCellFormattingEventArgs> metinsel hücre değerini alın ve karşılık gelen görüntü görüntüleme değeri ayarlamak için kullanılır.  
  
## <a name="example"></a>Örnek  
 [!code-csharp[System.Windows.Forms.DataGridViewCustomizeDataFormatting#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCustomizeDataFormatting/cs/customFormatting.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewCustomizeDataFormatting#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCustomizeDataFormatting/vb/customFormatting.vb#00)]  
  
## <a name="compiling-the-code"></a>Kod Derleniyor  
 Bu örnek gerektirir:  
  
- Sistem, System.Drawing ve System.Windows.Forms derlemelere başvuruları.  
  
- <xref:System.Drawing.Bitmap> Adlandırılmış resimler `highPri.bmp`, `mediumPri.bmp`, ve `lowPri.bmp` yürütülebilir dosyayla aynı dizinde bulunan.  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.DataGridView.DefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewBand.DefaultCellStyle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewCellStyle>
- <xref:System.Drawing.Bitmap>
- [Windows Forms DataGridView Denetiminde Verileri Görüntüleme](displaying-data-in-the-windows-forms-datagridview-control.md)
- [Nasıl yapılır: Verileri biçimlendirme Windows Forms DataGridView denetimi](how-to-format-data-in-the-windows-forms-datagridview-control.md)
- [Windows Forms DataGridView Denetimindeki Hücre Stilleri](cell-styles-in-the-windows-forms-datagridview-control.md)
- [Windows Forms DataGridView Denetiminde Veri Biçimlendirme](data-formatting-in-the-windows-forms-datagridview-control.md)
