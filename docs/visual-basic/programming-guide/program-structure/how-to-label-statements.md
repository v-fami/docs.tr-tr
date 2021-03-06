---
title: 'Nasıl yapılır: Etiket ifadeleri (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- colons (:)
- statements [Visual Basic], labels
- ': separator character'
- Visual Basic code, labeling statements
ms.assetid: 38f1ff43-2054-42cb-963b-1998e60c6ed4
ms.openlocfilehash: cbb80d94dc8280aa67859c89daad1520ce4e9669
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64648741"
---
# <a name="how-to-label-statements-visual-basic"></a>Nasıl yapılır: Etiket ifadeleri (Visual Basic)
Deyim blokları virgüllerle ayrılmış kod satırlarının oluşur. Öncesinde tanımlayan bir dize veya tamsayı kod satırlarını söylenebilir olmasını *etiketli*. Deyim etiketleri kullanmak için ifadelerle gibi tanımlamak için kod satırını işaretlemek için kullanılan `On Error Goto`.  
  
 Etiketler, geçerli ya da Visual Basic tanımlayıcıları olabilir — programlama öğeleri tanımlayan olanlar gibi — veya tamsayı sabit değerlerinde. Bir etiket, kaynak kod satırının başında yer almalıdır ve, aynı satırdaki bir deyimi tarafından olup izlenir bakılmaksızın, bir virgül gelmelidir.  
  
 Derleyici, satırın başına zaten tanımlı herhangi bir tanımlayıcı ile eşleşip eşleşmediğini kontrol ederek etiketleri tanımlar. Kullanmıyorsa, derleyici bir etiket olduğu varsayılır.  
  
 Etiketler, kendi bildirim alanına sahip ve diğer tanımlayıcıları ile müdahale etmez. Bir etiketin, yöntemin gövdesi kapsamıdır. Etiket bildirimi herhangi bir belirsiz durumda daha önceliklidir.  
  
> [!NOTE]
>  Etiketleri yalnızca yürütülebilir deyimleri yöntem içinde kullanılabilir.  
  
### <a name="to-label-a-line-of-code"></a>Etiket için bir kod satırı  
  
- Kaynak kod satırının başında, iki nokta arkasından bir tanımlayıcı yerleştirin.  
  
     Örneğin, aşağıdaki kod satırlarını ile etiketlenmiş `Jump` ve `120`sırasıyla:  
  
     [!code-vb[VbVbalrStatements#708](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#708)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Deyimler](../../../visual-basic/programming-guide/language-features/statements.md)
- [Bildirilen Öğe Adları](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [Program Yapısı ve Kod Kuralları](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)
