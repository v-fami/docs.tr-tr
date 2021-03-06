---
title: 'Nasıl yapılır: Otomatik Oluşturulan Sütunları Windows Forms DataGridView Denetiminden Kaldırma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], removing columns
- columns [Windows Forms], removing
ms.assetid: 92e28d98-95a3-446c-9150-41b7c7e5be15
ms.openlocfilehash: 95a39b22f3317e1721fa9f77e874a11431d35625
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64614707"
---
# <a name="how-to-remove-autogenerated-columns-from-a-windows-forms-datagridview-control"></a>Nasıl yapılır: Otomatik Oluşturulan Sütunları Windows Forms DataGridView Denetiminden Kaldırma
Olduğunda, <xref:System.Windows.Forms.DataGridView> denetimi sütunlarını veri kaynağından verileri temel alan otomatik ayarlama, seçmeli olarak bazı sütunlar atlayabilirsiniz. Bunu çağırarak yapmak <xref:System.Windows.Forms.DataGridViewColumnCollection.Remove%2A> metodunda <xref:System.Windows.Forms.DataGridView.Columns%2A> koleksiyonu. Alternatif olarak, ayarlayarak görünümünde sütunları gizleyebilirsiniz <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A> özelliğini `false`. Bu teknik, gizli sütunlarda belirli koşullarda görüntülemek istediğinizde veya görüntülemeden sütunları verilere erişmek gerektiğinde yararlı olur.  
  
### <a name="to-remove-autogenerated-columns"></a>Otomatik oluşturulan sütunları kaldırmak için  
  
- Çağrı <xref:System.Windows.Forms.DataGridViewColumnCollection.Remove%2A> metodunda <xref:System.Windows.Forms.DataGridView.Columns%2A> koleksiyonu.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#111](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#111)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#111](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#111)]  
  
### <a name="to-hide-autogenerated-columns"></a>Otomatik oluşturulan sütunları gizlemek için  
  
- Sütun kümesi <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A> özelliğini `false`.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#112](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#112)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#112](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#112)]  
  
## <a name="example"></a>Örnek  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#110](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#110)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#110](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#110)]  
  
## <a name="compiling-the-code"></a>Kod Derleniyor  
 Bu örnek gerektirir:  
  
- A <xref:System.Windows.Forms.DataGridView> adlı Denetim `dataGridView1` içeren bir tabloya bağlı `Fax` ve `CustomerID` sütunlar gibi `Customers` Northwind örnek veritabanındaki tablo.  
  
- Başvurular <xref:System?displayProperty=nameWithType> ve <xref:System.Windows.Forms?displayProperty=nameWithType> derlemeler.  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.AutoGenerateColumns%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.Columns%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumnCollection.Remove%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A?displayProperty=nameWithType>
- [Windows Forms DataGridView Denetiminde Verileri Görüntüleme](displaying-data-in-the-windows-forms-datagridview-control.md)
