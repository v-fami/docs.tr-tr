---
title: 'Nasıl yapılır: Windows Forms NumericUpDown Denetiminin Biçimini Ayarlama'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- NumericUpDown control [Windows Forms], formatting values
- up-down controls [Windows Forms], formatting numeric values
ms.assetid: fa7c5557-6bfb-45b2-975d-8887b23b0ba0
ms.openlocfilehash: a5d8de6db8a0d6f62a082fc381a7b855eb948514
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64630597"
---
# <a name="how-to-set-the-format-for-the-windows-forms-numericupdown-control"></a>Nasıl yapılır: Windows Forms NumericUpDown Denetiminin Biçimini Ayarlama
Windows Forms'ta değerlerin nasıl görüntüleneceğini yapılandırabileceğiniz <xref:System.Windows.Forms.NumericUpDown> denetimi. <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> Özelliği belirler kaç sayılar ondalık ayırıcıdan sonra görünür; varsayılan değer 0'dır. <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> Varsayılan özellik, her üç ondalık basamak arasında bir ayırıcı eklenip eklenmeyeceğini belirler; `false`. Denetim değerleri yerine ondalık, onaltılık görüntüleyebilirsiniz <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> özelliği `true`; varsayılan `false`.  
  
### <a name="to-format-the-numeric-value"></a>Sayısal değerini biçimlendirmek için  
  
- Bir ondalık değer ayarlayarak görüntüleyin <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> özelliği bir tamsayı ve ayarı <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> özelliğini `true` veya `false`.  
  
    ```vb  
    NumericUpDown1.DecimalPlaces = 2  
    NumericUpDown1.ThousandsSeparator = True  
    ```  
  
    ```csharp  
    numericUpDown1.DecimalPlaces = 2;  
    numericUpDown1.ThousandsSeparator = true;  
    ```  
  
    ```cpp  
    numericUpDown1->DecimalPlaces = 2;  
    numericUpDown1->ThousandsSeparator = true;  
    ```  
  
     -veya-  
  
- Ayarlayarak bir onaltılık değer görüntüleme <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> özelliğini `true`.  
  
    ```vb  
    NumericUpDown1.Hexadecimal = True  
    ```  
  
    ```csharp  
    numericUpDown1.Hexadecimal = true;  
    ```  
  
    ```cpp  
    numericUpDown1->Hexadecimal = true;  
    ```  
  
    > [!NOTE]
    >  Değeri, onaltılık olarak formda görüntülenir bile herhangi bir test gerçekleştirdiğiniz <xref:System.Windows.Forms.NumericUpDown.Value%2A> özellik ondalık değeri test.  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.NumericUpDown>
- [NumericUpDown Denetimi](numericupdown-control-windows-forms.md)
- [NumericUpDown Denetimine Genel Bakış](numericupdown-control-overview-windows-forms.md)
