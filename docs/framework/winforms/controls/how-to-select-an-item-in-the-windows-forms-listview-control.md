---
title: 'Nasıl yapılır: Windows Forms ListView Denetiminde Öğe Seçme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- lists [Windows Forms], selecting items
- ListView control [Windows Forms], selecting items
- selection [Windows Forms], in list views
- list views [Windows Forms], selecting items
ms.assetid: ddea918e-1ddf-47f4-bd09-1e9b4c9d0c39
ms.openlocfilehash: 41a30ba6c242d0587e98b458e41ca213e8885bca
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64638197"
---
# <a name="how-to-select-an-item-in-the-windows-forms-listview-control"></a>Nasıl yapılır: Windows Forms ListView Denetiminde Öğe Seçme
Bu örnek program aracılığıyla bir Windows Formları öğeyi seçmek nasıl gösterir <xref:System.Windows.Forms.ListView> denetimi. Program aracılığıyla bir öğe seçtiğinizde otomatik olarak değişmez odağı <xref:System.Windows.Forms.ListView> denetimi. Bu nedenle, genellikle de öğesi bir öğeyi seçerken odaklı olarak ayarlamak istersiniz.  
  
## <a name="example"></a>Örnek  
 [!code-csharp[System.Windows.Forms.ListView.Misc#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListView.Misc/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ListView.Misc#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListView.Misc/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Kod Derleniyor  
 Bu örnek gerektirir:  
  
- A <xref:System.Windows.Forms.ListView> adlı Denetim `listView1` , en az bir öğe içeriyor.  
  
- Başvurular <xref:System?displayProperty=nameWithType> ve <xref:System.Windows.Forms?displayProperty=nameWithType> ad alanları.  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListViewItem.Selected%2A?displayProperty=nameWithType>
