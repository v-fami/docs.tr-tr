---
title: Visual Basic'de Dize Düzenleme Yöntemlerinin Türleri
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], manipulating [Visual Basic]
- string manipulation
ms.assetid: 905055cd-7f50-48fb-9eed-b0995af1dc1f
ms.openlocfilehash: 44eb101ebdfeb316958a659107190ef1fc84df44
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61938274"
---
# <a name="types-of-string-manipulation-methods-in-visual-basic"></a>Visual Basic'de Dize Düzenleme Yöntemlerinin Türleri
Dizeleri işlemek ve çözümlemek için çeşitli yollar vardır. Bazı yöntemlere Visual Basic dilinin bir parçası olan ve diğerleri de belirlidir `String` sınıfı.  
  
## <a name="visual-basic-language-and-the-net-framework"></a>Visual Basic dili ve .NET Framework  
 Visual Basic yöntemleri, doğal dil işlevleri kullanılır. Kodunuzda nitelik olmadan kullanılabilir. Aşağıdaki örnek, bir Visual Basic dize işleme komut tipik kullanımını gösterir:  
  
 [!code-vb[VbVbalrStrings#44](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#44)]  
  
 Bu örnekte, `Mid` işlevi üzerinde doğrudan bir işlem gerçekleştiren `aString` ve değeri atar `bString`.  
  
 Visual Basic dize düzenleme yöntemlerinin bir listesi için bkz [dize düzenleme özeti](../../../../visual-basic/language-reference/keywords/string-manipulation-summary.md).  
  
### <a name="shared-methods-and-instance-methods"></a>Paylaşılan ve örnek yöntemleri  
 Dize yöntemleri ile işleyebileceğiniz `String` sınıfı. Yöntemleri iki tür vardır `String`: *paylaşılan* yöntemleri ve *örneği* yöntemleri.  
  
#### <a name="shared-methods"></a>Paylaşılan yöntemleri  
 Paylaşılan bir yöntemine gelen kaynaklandığını yöntemdir `String` sınıfının kendisini ve çalışmak için bu sınıfın bir örneğini gerektirmez. Bu yöntemler, sınıfın adıyla nitelendirilmesi (`String`) yerine örneğiyle birlikte `String` sınıfı. Örneğin:  
  
 [!code-vb[VbVbalrStrings#45](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#45)]  
  
 Önceki örnekte <xref:System.String.Copy%2A?displayProperty=nameWithType> yöntemi statik yöntem bir ifade üzerinde çalışan verilir ve çıkan değeri atar `bString`.  
  
#### <a name="instance-methods"></a>Örnek yöntemleri  
 Örnek yöntemleri, aksine, belirli bir örneğini kökü `String` ve örnek adı ile nitelenmelidir. Örneğin:  
  
 [!code-vb[VbVbalrStrings#46](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#46)]  
  
 Bu örnekte, <xref:System.String.Substring%2A?displayProperty=nameWithType> yöntemdir örneğinin bir yöntemin `String` (diğer bir deyişle, `aString`). Üzerinde bir işlem gerçekleştirir `aString` ve bu değeri atar `bString`.  
  
 Daha fazla bilgi için belgelerine bakın <xref:System.String> sınıfı.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Visual Basic'de dizelere giriş](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)
