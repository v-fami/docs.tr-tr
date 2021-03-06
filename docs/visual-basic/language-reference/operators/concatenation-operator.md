---
title: '&amp; İşleci (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.&
helpviewer_keywords:
- And (&) operator
- ampersand operator (&)
- '& operator'
- concatenation operators [Visual Basic], syntax
- strings [Visual Basic], concatenating
ms.assetid: fefc3d00-cbf1-475c-8c5e-6fb213b3f85a
ms.openlocfilehash: dd85363447e9b405241d608550d9484b4760a739
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61778592"
---
# <a name="amp-operator-visual-basic"></a>&amp; İşleci (Visual Basic)
İki ifadenin dize birleştirmesini oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
result = expression1 & expression2  
```  
  
## <a name="parts"></a>Bölümler  
 `result`  
 Gerekli. Tüm `String` veya `Object` değişkeni.  
  
 `expression1`  
 Gerekli. Herhangi bir ifade bir veri türüyle için widens `String`.  
  
 `expression2`  
 Gerekli. Herhangi bir ifade bir veri türüyle için widens `String`.  
  
## <a name="remarks"></a>Açıklamalar  
 Veri türü `expression1` veya `expression2` değil `String` ancak için widens `String`, dönüştürülür `String`. Veri türlerinden birini değil genişletmek için `String`, derleyici bir hata oluşturur.  
  
 Veri türü `result` olduğu `String`. Bir veya iki ifadeleri sonucunu verirse [hiçbir şey](../../../visual-basic/language-reference/nothing.md) veya bir değere sahip <xref:System.DBNull.Value?displayProperty=nameWithType>, değerini içeren bir dize olarak kabul edilir "".  
  
> [!NOTE]
>  `&` İşleci olabilir *aşırı*, işleneni, sınıf veya yapı türüne sahip olduğunda bir sınıf veya yapı davranışını tanımlayabilirsiniz, anlamına gelir. Kodunuz bu tür bir sınıf veya yapı üzerinde bu işleç kullanıyorsa, yeniden tanımlanan davranışını anladığınızdan emin olun. Daha fazla bilgi için [işleç yordamları](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
> [!NOTE]
>  (&) Karakteri de değişken türü olarak tanımlamak için kullanılabilir `Long`. Daha fazla bilgi için [tür karakterleri](../../../visual-basic/programming-guide/language-features/data-types/type-characters.md).  
  
## <a name="example"></a>Örnek  
 Bu örnekte `&` dize birleştirme zorlamak için işleci. Sonucu, iki dizeyi işlenenlere birleşimi temsil eden bir dize değeridir.  
  
 [!code-vb[VbVbalrOperators#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#2)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [&= İşleci](../../../visual-basic/language-reference/operators/and-assignment-operator.md)
- [Birleştirme İşleçleri](../../../visual-basic/language-reference/operators/concatenation-operators.md)
- [Visual Basic'de İşleç önceliği](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [İşlevselliğe Göre Listelenmiş İşleçler](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Visual Basic'de birleştirme işleçleri](../../../visual-basic/programming-guide/language-features/operators-and-expressions/concatenation-operators.md)
