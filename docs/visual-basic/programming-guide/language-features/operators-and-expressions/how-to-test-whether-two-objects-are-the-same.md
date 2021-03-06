---
title: 'Nasıl yapılır: İki nesnenin aynı (Visual Basic) olup olmadığını test etme'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], reference
- Is operator [Visual Basic], comparing objects
- reference variables [Visual Basic]
- variables [Visual Basic], referring to same object
- objects [Visual Basic], variables referring to same
- Visual Basic code, operators
ms.assetid: f760e828-8704-4256-bc2d-c22a4c93b524
ms.openlocfilehash: 6301228d786fe55e8851b6207dd84819671656f4
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64649675"
---
# <a name="how-to-test-whether-two-objects-are-the-same-visual-basic"></a>Nasıl yapılır: İki nesnenin aynı (Visual Basic) olup olmadığını test etme
Nesnelere atıfta iki değişken varsa, kullanabilirsiniz `Is` veya `IsNot` işleci veya her ikisi de aynı örneğine başvurmadığını belirlemek için.  
  
### <a name="to-test-whether-two-objects-are-the-same"></a>İki nesnenin aynı olup olmadığını test etmek için  
  
- Kullanım [işleci olan](../../../../visual-basic/language-reference/operators/is-operator.md) veya [IsNot işleci](../../../../visual-basic/language-reference/operators/isnot-operator.md) işlenen olarak iki değişken ile.  
  
     [!code-vb[VbVbalrOperators#69](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#69)]  
  
 Olup iki nesnenin aynı örneğe atıfta bağlı olarak belirli bir eylem almak isteyebilirsiniz. Yukarıdaki örnekte denetim karşılaştırır `c` form altformdaki etkin denetimi karşı `f`. Etkin bir denetim yok ya da varsa bir ancak değil aynı denetim örneğine `c`, ardından `If` deyim başarısız olur ve yordamı daha fazla işleme olmadan döndürür.  
  
 Kullanıp `Is` veya `IsNot` kişisel kolaylık sağlamak için bir konudur. Bir diğerinden belirli bir ifadede daha kolay olabilir.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Visual Basic'de Karşılaştırma işleçleri](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)
