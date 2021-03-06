---
title: IsFalse İşleci (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.isfalse
helpviewer_keywords:
- AndAlso operator [Visual Basic]
- IsFalse operator [Visual Basic]
ms.assetid: 37fc9dbf-e5cc-4570-b93f-7213447974df
ms.openlocfilehash: 9f25c406038486224c2c4708c86ef86889c44c15
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62013549"
---
# <a name="isfalse-operator-visual-basic"></a>IsFalse İşleci (Visual Basic)
Bir ifade olup olmadığını belirler `False`.  
  
 Çağıramazsınız `IsFalse` açıkça kodunuzu kullanabilirsiniz, ancak Visual Basic derleyici Bu kod oluşturmak için `AndAlso` yan tümceleri. Bir sınıf veya yapı tanımlayın ve ardından bu türde bir değişken kullanmak, bir `AndAlso` yan tümcesi tanımlamalıdır `IsFalse` Bu sınıf ya da yapı üzerinde.  
  
 Derleyici göz önünde bulundurur `IsFalse` ve `IsTrue` işleçleri bir *çifti eşleşen*. Başka bir deyişle, bir tanesi tanımlarsanız, ayrıca diğeri tanımladığınız gerekir.  
  
> [!NOTE]
>  `IsFalse` İşleci olabilir *aşırı*, kendi işleneninin türü, sınıfın veya yapının olduğunda bir sınıf veya yapı davranışını tanımlayabilirsiniz, anlamına gelir. Kodunuz bu tür bir sınıf veya yapı üzerinde bu işleç kullanıyorsa, yeniden tanımlanan davranışını anladığınızdan emin olun. Daha fazla bilgi için [işleç yordamları](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği için tanımları içeren bir yapının anahat tanımlar `IsFalse` ve `IsTrue` işleçleri.  
  
 [!code-vb[VbVbalrOperators#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#28)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [IsTrue İşleci](../../../visual-basic/language-reference/operators/istrue-operator.md)
- [Nasıl yapılır: Bir işleci tanımlama](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [AndAlso İşleci](../../../visual-basic/language-reference/operators/andalso-operator.md)
