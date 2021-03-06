---
title: 'Nasıl yapılır: Numaralandırmalar (Visual Basic) bildirme'
ms.date: 07/20/2015
helpviewer_keywords:
- declarations [Visual Basic], enumerations
- enumerations [Visual Basic], declaring
- declaring enumerations [Visual Basic]
ms.assetid: db4ca1c3-f429-4c81-ae81-29e0157b29fd
ms.openlocfilehash: c74b75adf0f56dd198375cb1ff24656d39ec074c
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64610573"
---
# <a name="how-to-declare-enumerations-visual-basic"></a>Nasıl yapılır: Numaralandırmalar (Visual Basic) bildirme
Numaralandırma ile oluşturma `Enum` bir sınıf veya modül bildirimleri bölümünde bildirimi. Bir yöntem içinde bir listelemeyi bildiremezsiniz. Uygun erişim düzeyini belirtmek için kullanın `Private`, `Protected`, `Friend`, veya `Public`.  
  
 Bir `Enum` türünde bir ad ve bir temel türü bir dizi alanları, her bir sabiti temsil eden. Ad geçerli bir Visual Basic .NET niteleyici olmalıdır. Temel alınan türü tamsayı türlerinin biri olmalıdır:`Byte`, `Short`, `Long` veya `Integer`. `Integer` varsayılandır. Numaralandırmalar, her zaman kesin olarak belirlenmiştir ve tamsayı sayı türleri ile değiştirilebilir değildir.  
  
 Numaralandırmalar, kayan nokta değerlerine sahip olamaz. Bir kayan nokta değeri ile numaralandırma atanırsa `Option Strict On`, bir derleyici hatası sonuçları. Varsa `Option Strict` olduğu `Off`, değer otomatik olarak dönüştürülür `Enum` türü.  
  
 Bilgi adları ve nasıl kullanılacağını `Imports` ad niteliği gereksiz, yapmak bildirimini [numaralandırmalar ve ad niteliği](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md).  
  
### <a name="to-declare-an-enumeration"></a>Bir numaralandırmayı bildirmek için  
  
1. Kod erişim düzeyi içeren bir bildirimi yazma `Enum` anahtar sözcüğü ve her biri farklı bir bildirir geçerli bir ad, aşağıdaki örneklerde gösterildiği gibi `Enum`.  
  
     [!code-vb[VbEnumsTask#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#3)]  
  
2. Sabitleri sabit listesi tanımlayın. Varsayılan olarak, bir listedeki ilk sabit değerine ayarlanır `0`, ve sonraki sabit bir değer bir önceki sabiti fazlasını başlatılır. Örneğin, aşağıdaki sabit `Days`, adlı bir sabit içeriyor `Sunday` değerle `0`, adlı bir sabit `Monday` değerle `1`, adlı bir sabit `Tuesday` değeriyle`2`ve benzeri.  
  
     [!code-vb[VbEnumsTask#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#4)]  
  
3. Değerleri bir numaralandırma sabitlerini için bir atama ifadesi kullanarak açıkça atayabilirsiniz. Negatif sayılar dahil olmak üzere, herhangi bir tamsayı değeri atayabilirsiniz. Örneğin, sıfırdan küçük değerleri hata koşullarını göstermek için sabitleriyle isteyebilirsiniz. Aşağıdaki listedeki sabiti `Invalid` değeri açıkça atanan `–1`ve sabit `Sunday` değeri atanır `0`. Listedeki ilk sabit olduğundan `Saturday` değerine de başlatılır `0`. Değerini `Monday` olduğu `1` (bir değerinden daha fazla `Sunday`); değerini `Tuesday` olduğu `2`ve benzeri.  
  
     [!code-vb[VbEnumsTask#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#5)]  
  
### <a name="to-declare-an-enumeration-as-an-explicit-type"></a>Açık bir tür olarak bir numaralandırmayı bildirmek için  
  
- Sabit listesi türünü kullanarak belirtin `As` yan tümcesi, aşağıdaki örnekte gösterildiği gibi.  
  
     [!code-vb[VbEnumsTask#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#6)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Sabit Listeleri ve Ad Niteliği](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)
- [Nasıl yapılır: Bir numaralandırma üyesine başvurma](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)
- [Nasıl yapılır: Visual Basic'de numaralandırma yoluyla yineleme yapma](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-iterate-through-an-enumeration.md)
- [Nasıl yapılır: Bir numaralandırma değeriyle ilişkili dizeyi belirleme](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-determine-the-string-associated-with-an-enumeration-value.md)
- [Sabit Listesi Ne Zaman Kullanılır?](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)
- [Sabitlere Genel Bakış](../../../../visual-basic/programming-guide/language-features/constants-enums/constants-overview.md)
- [Sabit ve Değişmez Değerli Veri Türleri](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md)
- [Sabitler ve Sabit Listeleri](../../../../visual-basic/language-reference/constants-and-enumerations.md)
