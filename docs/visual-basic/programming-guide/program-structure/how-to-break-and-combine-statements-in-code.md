---
title: 'Nasıl yapılır: (Visual Basic) kodda deyimleri bölme ve birleştirme'
ms.date: 07/20/2015
f1_keywords:
- vb._
helpviewer_keywords:
- colons (:)
- line continuation
- _ line-continuation character
- ': line separator character'
- Visual Basic code, line breaks in
- Visual Basic code, line breaks
- Visual Basic code, line continuation
- long lines of code
- line terminator
- line-continuation sequence
- underscores [Visual Basic], in code
- statements [Visual Basic], line continuation in
- line breaks [Visual Basic], in code
- line-continuation character [Visual Basic]
- Visual Basic code, line continuation in
- statements [Visual Basic], line breaks in
ms.assetid: dea01dad-a8ac-484a-bb3a-8c45a1b1eccc
ms.openlocfilehash: d3656b924ebaca67c90dc602701c4cef9ce088b4
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64648787"
---
# <a name="how-to-break-and-combine-statements-in-code-visual-basic"></a>Nasıl yapılır: (Visual Basic) kodda deyimleri bölme ve birleştirme
Kodunuzu yazarken, bazen Kod Düzenleyicisi'nde yatay kaydırma başlatılmalarını uzun ifadeleri oluşturabilirsiniz. Bu şekilde etkilememesine rağmen kodunuz, bunu siz veya başka hiç kimse izleyicide göründüğü gibi kod okumanız için için zorlaştırır. Böyle durumlarda, birkaç satıra tek uzun deyim sonu düşünmelisiniz.  
  
### <a name="to-break-a-single-statement-into-multiple-lines"></a>Tek bir deyimde birden çok satıra ayırmak için  
  
- Bir alt çizgi olan satır devamlılığı karakterini kullanın (`_`), satır sonu istediğiniz noktada. Alt çizgi boşlukla hemen önce ve satır Sonlandırıcı (başı) tarafından hemen ardından.  
  
    > [!NOTE]
    >  Satır devamlılığı karakteri atlarsanız, bazı durumlarda, Visual Basic derleyici örtük olarak deyim kodun sonraki satırında devam eder. Kendisi için çıkarabilirsiniz satır devamlılığı karakteri söz dizimi öğeleri listesi için bkz: "Örtük satır devamlılığı" [deyimleri](../../../visual-basic/programming-guide/language-features/statements.md).  
  
     Aşağıdaki örnekte, dört satırı tüm sonlandırma satır devamlılığı karakteri ile ancak son satır deyim ayrılır.  
  
     [!code-vb[VbVbcnConventions#20](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnConventions/VB/Class1.vb#20)]  
  
     Bu sırayı kullanarak kodunuzu okumak, hem çevrimiçi hem de zaman yazdırılan kolaylaştırır.  
  
     Satır devamlılığı karakteri bir satırdaki son karakter olmalıdır. Bunu başka bir şey ile aynı satırda gelemez.  
  
     Satır devamlılığı karakteri burada kullanabilirsiniz için bazı sınırlamalar mevcuttur; Örneğin, ortasında bir bağımsız değişken adı olarak kullanamazsınız. Satır devamlılığı karakteri bir bağımsız değişken listesiyle bozabilir ancak bağımsız değişkenlerin adlarını değişmeden kalır.  
  
     Bir açıklama satır devam karakterini kullanarak devam edemiyor. Derleyici, özel bir anlamı için bir açıklama karakterleri inceleyin değil. Bir çok satırlı açıklama için yorum sembolü yineleyin (`'`) her satırda.  
  
 Her deyim ayrı bir satıra yerleştirme önerilen yöntem olsa da, Visual Basic da aynı satırda birden çok deyime yerleştirmenize olanak sağlar.  
  
### <a name="to-place-multiple-statements-on-the-same-line"></a>Aynı satırda birden çok deyime yerleştirmek için  
  
- Deyimleri bir iki nokta üst üste ile ayırın (`:`), aşağıdaki örnekte olduğu gibi.  
  
     [!code-vb[VbVbcnConventions#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnConventions/VB/Class1.vb#10)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Program Yapısı ve Kod Kuralları](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)
- [Deyimler](../../../visual-basic/programming-guide/language-features/statements.md)
