---
title: 'Nasıl yapılır: Windows Forms DataGridView Denetiminde Yeni Satırlar İçin Varsayılan Değerleri Belirtme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], default values for new rows
- DataGridView control [Windows Forms], data entry
- rows [Windows Forms], specifying default values
- DataGridView control [Windows Forms], default values for new rows
ms.assetid: 8d127963-d9f8-4e4e-9f7f-beb66688f1f2
ms.openlocfilehash: 879c035366c4686ceff3250a63c6ae8d8d3cfec4
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64651956"
---
# <a name="how-to-specify-default-values-for-new-rows-in-the-windows-forms-datagridview-control"></a>Nasıl yapılır: Windows Forms DataGridView Denetiminde Yeni Satırlar İçin Varsayılan Değerleri Belirtme
Uygulamaya yeni eklenen satırlar için değerleri varsayılan doldururken daha kolay veri girişi yapabilirsiniz. İle <xref:System.Windows.Forms.DataGridView> sınıfı doldurabilirsiniz varsayılan değerlerle <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> olay. Kullanıcı yeni kayıtlar için satır girdiğinde bu olay tetiklenir. Kodunuzu bu olay işlediğinde, seçtiğiniz değerlere sahip istenen hücreleri doldurabilirsiniz.  
  
 Aşağıdaki kod örneği kullanarak yeni satırlar için varsayılan değerlerin nasıl belirtileceğini gösterir <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> olay.  
  
## <a name="example"></a>Örnek  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#120](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#120)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#120](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#120)]  
  
## <a name="compiling-the-code"></a>Kod Derleniyor  
 Bu örnek gerektirir:  
  
- A <xref:System.Windows.Forms.DataGridView> adlı Denetim `dataGridView1`.  
  
- A `NewCustomerId` benzersiz oluşturmak için işlevi `CustomerID` değerleri.  
  
- Başvurular <xref:System?displayProperty=nameWithType> ve <xref:System.Windows.Forms?displayProperty=nameWithType> derlemeler.  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded?displayProperty=nameWithType>
- [Windows Forms DataGridView Denetiminde Veri Girişi](data-entry-in-the-windows-forms-datagridview-control.md)
- [Windows Forms DataGridView Denetiminde Yeni Kayıtlar için Satır Kullanma](using-the-row-for-new-records-in-the-windows-forms-datagridview-control.md)
