---
title: 'Nasıl yapılır: Veri Bağlantılı Windows Forms DataGridView Denetiminde Sütunları Otomatik Olarak Oluşturma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], autogenerating columns
- columns [Windows Forms], autogenerating
- DataGridView control [Windows Forms], data-bound columns
ms.assetid: 699f6f9e-6aa5-4811-902b-6a2c57dec7d6
ms.openlocfilehash: eb74c1ef1661fc8bd7a57f079f10d24a7eef8187
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64639758"
---
# <a name="how-to-autogenerate-columns-in-a-data-bound-windows-forms-datagridview-control"></a>Nasıl yapılır: Veri Bağlantılı Windows Forms DataGridView Denetiminde Sütunları Otomatik Olarak Oluşturma
Aşağıdaki kod örneği, bir bağlı veri kaynağından sütunları görüntülemek gösterilmiştir bir <xref:System.Windows.Forms.DataGridView> denetimi. Zaman <xref:System.Windows.Forms.DataGridView.AutoGenerateColumns%2A> özellik değeri `true` (varsayılan), bir <xref:System.Windows.Forms.DataGridViewColumn> veri kaynağı tablosu içindeki her bir sütun için oluşturulur.  
  
 Varsa <xref:System.Windows.Forms.DataGridView> denetimi ayarladığınızda sütunu zaten var. <xref:System.Windows.Forms.DataGridViewComboBoxColumn.DataSource%2A> özelliği, mevcut bağlı sütun veri kaynağında sütunları karşılaştırılan ve bir eşleşme olduğunda korunur. Bağlanmamış sütunlar her zaman korunur. Var olan veri kaynağında eşleşme bağlı sütun kaldırılır. Vygenerovat sloupce var olduğu eşleşme denetiminde veri kaynağı içindeki yeni <xref:System.Windows.Forms.DataGridViewColumn> sonuna eklenen nesneleri <xref:System.Windows.Forms.DataGridView.Columns%2A> koleksiyonu.  
  
## <a name="example"></a>Örnek  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#020](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#020)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#020](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#020)]  
  
## <a name="compiling-the-code"></a>Kod Derleniyor  
 Bu örnek gerektirir:  
  
- A <xref:System.Windows.Forms.DataGridView> adlı Denetim `customersDataGridView`.  
  
- A <xref:System.Data.DataSet> adlı nesne `customersDataSet` adlı bir tablo olan `Customers`.  
  
- Başvurular <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, <xref:System.Data?displayProperty=nameWithType>, ve <xref:System.Xml?displayProperty=nameWithType> derlemeler.  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.AutoGenerateColumns%2A?displayProperty=nameWithType>
- [Windows Forms DataGridView Denetiminde Verileri Görüntüleme](displaying-data-in-the-windows-forms-datagridview-control.md)
- [Nasıl yapılır: Otomatik oluşturulan sütunları Windows Forms DataGridView denetiminden kaldırma](remove-autogenerated-columns-from-a-wf-datagridview-control.md)
