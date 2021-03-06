---
title: Continue Deyimi (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.continue
helpviewer_keywords:
- Continue statement [Visual Basic]
- loops, transferring to next iteration
ms.assetid: 3ad00103-358b-4af3-a3a8-1b9ea0e995d3
ms.openlocfilehash: 5523be69f2901851c86f6c0263548e3577507ff9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61638252"
---
# <a name="continue-statement-visual-basic"></a>Continue Deyimi (Visual Basic)
Hemen bir döngünün sonraki yinelemesine için aktarımları denetimi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Continue { Do | For | While }  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Aktarabilir miyim içinde bir `Do`, `For`, veya `While` Bu döngünün sonraki yinelemesine döngü. Denetim aktarma için eşdeğer olan hemen döngü koşul testi geçer `For` veya `While` deyimi veya `Do` veya `Loop` içeren ifade `Until` veya `While` yan tümcesi.  
  
 Kullanabileceğiniz `Continue` aktarımlarına izin veren döngü herhangi bir konumda. Aktarım Denetimi verme kuralları ile aynıdır [GoTo deyimi](../../../visual-basic/language-reference/statements/goto-statement.md).  
  
 Örneğin, bir döngü içinde tamamen bağımsız bir `Try` bloğu bir `Catch` bloğu veya `Finally` bloğu kullanabilirsiniz `Continue` döngü dışına aktarmak için. Diğer yandan Eğer `Try`... `End Try` yapısı döngü içinde bulunan, kullanamazsınız `Continue` kontrolünü dışarı aktarmak için `Finally` bloğunda kullanabilirsiniz, dışarı aktarmak için bir `Try` veya `Catch` yalnızca tamamen tanesi aktarırsanız engelle `Try`... `End Try` yapısı.  
  
 İç içe döngüleri aynı tür, örneğin varsa bir `Do` döngü içindeki başka `Do` döngüsü, bir `Continue Do` ifade en içteki bir sonraki yinelemesine atlar `Do` içerdiği döngü. Kullanamazsınız `Continue` aynı tür içeren bir döngünün sonraki yinelemesine atlanacak.  
  
 Farklı türlerde iç içe döngüleri örnek varsa bir `Do` döngü içinde bir `For` döngüsü kullanarak ya da döngünün sonraki yinelemesine atlayabilirsiniz `Continue Do` veya `Continue For`.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneğinde `Continue While` bölen sıfırsa bir dizi için bir sonraki sütununu atlama deyimi. `Continue While` İçinde bir `For` döngü. İçin aktarır `While col < lastcol` en içteki sonraki yinelemesine deyimi `While` içeren döngü `For` döngü.  
  
 [!code-vb[VbVbalrStatements#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#14)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Do...Loop Deyimi](../../../visual-basic/language-reference/statements/do-loop-statement.md)
- [For...Next Deyimi](../../../visual-basic/language-reference/statements/for-next-statement.md)
- [While...End While Deyimi](../../../visual-basic/language-reference/statements/while-end-while-statement.md)
- [Try...Catch...Finally Deyimi](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
