---
title: 'Nasıl yapılır: BindingSource Bileşenini Kullanarak Bağlı Verileri Formlar Arasında Paylaşma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- examples [Windows Forms], BindingSource component
- data binding [Windows Forms], sharing data across forms
- BindingSource component [Windows Forms], examples
- BindingSource [Windows Forms], using with multiple forms
ms.assetid: a1a49630-db9c-4485-b888-1f62a373a4f7
ms.openlocfilehash: 28eceaec72053d70885d54bc09179cff743ff71c
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65591443"
---
# <a name="how-to-share-bound-data-across-forms-using-the-bindingsource-component"></a>Nasıl yapılır: BindingSource Bileşenini Kullanarak Bağlı Verileri Formlar Arasında Paylaşma
Kullanarak formlar arasında verileri kolayca paylaşabilirsiniz <xref:System.Windows.Forms.BindingSource> bileşeni. Örneğin, veri kaynağı verileri özetleyen bir salt okunur ve veri kaynağındaki geçerli seçilmiş öğe hakkındaki ayrıntılı bilgileri içeren başka bir düzenlenebilir formunda görüntülemek isteyebilirsiniz. Bu örnekte, bu senaryo gösterilmektedir.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneğinde nasıl paylaşacağınızı gösterir bir <xref:System.Windows.Forms.BindingSource> ve bağlı verileri formlar arasında. Bu örnekte, paylaşılan <xref:System.Windows.Forms.BindingSource> alt formunun oluşturucuya geçirilir. Alt formun ana biçiminde geçerli seçilmiş öğe için veri düzenlemesine olanak tanır.  
  
> [!NOTE]
>  <xref:System.Windows.Forms.BindingSource.BindingComplete> Olayı <xref:System.Windows.Forms.BindingSource> bileşeni örnekte iki eşitlenmiş kalmasını sağlamak için gerçekleştirilir. Neden hakkında daha fazla bilgi için bu gerçekleştirilir, bkz: [nasıl yapılır: Birden çok denetimin eşitlenmiş kalmasını aynı veri kaynağına bağlanan](../multiple-controls-bound-to-data-source-synchronized.md).  
  
 [!code-csharp[System.Windows.Forms.BindingSourceMultipleForms#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.BindingSourceMultipleForms/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.BindingSourceMultipleForms#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.BindingSourceMultipleForms/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Kod Derleniyor  
 Bu örnek gerektirir:  
  
- Sistem, System.Windows.Forms, System.Drawing, System.Data ve System.Xml derlemesine ilişkin başvurular.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [BindingSource Bileşeni](bindingsource-component.md)
- [Windows Forms Veri Bağlama](../windows-forms-data-binding.md)
- [Nasıl yapılır: Hataları ve ortaya çıkan özel durumlar veri bağlama ile işleme](how-to-handle-errors-and-exceptions-that-occur-with-databinding.md)
