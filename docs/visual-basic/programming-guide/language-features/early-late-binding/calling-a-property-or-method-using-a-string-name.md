---
title: Bir Dize Adı Kullanarak Bir Özelliği veya Yöntemi Çağırma (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- passing operators [Visual Basic]
- strings [Visual Basic], passing new operators as
- objects [Visual Basic], setting properties
- setting properties, object properties at run time
- method calls [Visual Basic], strings
- methods [Visual Basic], calling with string names
- calling methods [Visual Basic], string names
- properties [Visual Basic], setting at run time
- CallByName function
ms.assetid: 79a7b8b4-b8c7-4ad8-aca8-12a9a2b32f03
ms.openlocfilehash: 92430f23b3d4d6237d0b6ec606ce2cb9b945f6f8
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65590037"
---
# <a name="calling-a-property-or-method-using-a-string-name-visual-basic"></a>Bir Dize Adı Kullanarak Bir Özelliği veya Yöntemi Çağırma (Visual Basic)
Çoğu durumda, tasarım zamanında bir nesnenin yöntemleri ve özellikleri keşfedin ve bunları işlemek için kod yazın. Ancak, bazı durumlarda, bir nesnenin özellikleri ve yöntemleri hakkında önceden bilmeyebilir veya yalnızca bir son kullanıcının özelliklerini belirtin veya çalışma zamanında bir yöntem yürütülemez etkinleştirme esnekliğine isteyebilirsiniz.  
  
## <a name="callbyname-function"></a>CallByName işlevi  
 , Örneğin, bir COM bileşeni için bir işleç geçirerek kullanıcı tarafından girilen ifadeleri değerlendiren bir istemci uygulaması düşünün. Yeni işlevleri yeni işleç gerektiren bileşenine sürekli ekleme varsayalım. Standart nesne erişimi teknikleri kullandığınızda, yeniden derleyin ve yeni işleçleri kullanabilirsiniz önce istemci uygulaması yeniden dağıtmanız gerekir. Bunu önlemek için kullanabileceğiniz `CallByName` işlevini uygulama değiştirmeden yeni işleç dize olarak geçirin.  
  
 `CallByName` İşlev çalışma zamanında bir özelliği veya yöntemi belirtmek için bir dize kullanmanıza imkan tanır. İmzası `CallByName` işlevi şu şekilde görünür:  
  
 *Sonuç* = `CallByName`(*nesne*, *ProcedureName*, *; CallType &*, *bağımsız değişkenleri*())  
  
 İlk bağımsız değişken *nesne*, üzerinde işlem yapmak istediğiniz nesne adını alır. *ProcedureName* çağrılacak yöntem veya özellik yordamın adını içeren bir dize bağımsız değişkeni alır. *; CallType &* çağrılacak yordamı türünü temsil eden sabit bağımsız değişkeni alır: bir yöntem (`Microsoft.VisualBasic.CallType.Method`), bir özelliğin okuma (`Microsoft.VisualBasic.CallType.Get`), veya bir özellik kümesi (`Microsoft.VisualBasic.CallType.Set`). *Bağımsız değişkenleri* isteğe bağlı bağımsız değişken alan bir dizi türü `Object` yordam herhangi bir bağımsız değişken içeren.  
  
 Kullanabileceğiniz `CallByName` sınıflarıyla geçerli çözümünüzden, ancak çoğunlukla COM nesneleri veya nesneler .NET Framework derlemeleri erişmek için kullanılır.  
  
 Adlı bir sınıf içeren bir bütünleştirilmiş kod Başvurusu Ekle varsayalım `MathClass`, adlı yeni bir işlev olan `SquareRoot`aşağıdaki kodda gösterildiği gibi:  
  
 [!code-vb[VbVbalrOOP#53](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#53)]  
  
 Uygulamanızın hangi yöntemin çağrılacağı denetimi ve bağımsız değişkenlerinden metin kutusu denetimleri kullanabilirsiniz. Örneğin, varsa `TextBox1` uyumluluğunun değerlendirilebilmesi için ifade içeriyor ve `TextBox2` olan işlevin adını girmek için kullanılan, çağırmak için aşağıdaki kodu kullanabilirsiniz `SquareRoot` ifade üzerinde işlev `TextBox1`:  
  
 [!code-vb[VbVbalrOOP#54](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#54)]  
  
 İçinde "64" girerseniz `TextBox1`, "SquareRoot" `TextBox2`ve sonra çağrı `CallMath` yordamı, bir sayının karekökünü `TextBox1` değerlendirilir. Örnek kodda çağırır `SquareRoot` (gerekli bir bağımsız değişken olarak değerlendirilecek bir ifade içeren bir dize alan) çalışır ve "8" döndürür `TextBox1` (64 kare kökünü). Elbette, geçersiz bir dize olarak kullanıcı girerse `TextBox2`, bir yöntem yerine bir özelliğin adı dize içeriyor ya da yöntem ek gerekli bağımsız değişken varsa, bir çalışma zamanı hatası oluşur. Kullandığınızda güçlü hata işleme kodu eklemek zorunda `CallByName` bu veya herhangi bir hata tahmin için.  
  
> [!NOTE]
>  Sırada `CallByName` işlevi bazı durumlarda yararlı olabilir, yararlılığını performans etkilerinin karşı yaratmasını önlemelidir — kullanarak `CallByName` bir yordam çağırmak için geç bağlanan çağrı kısmen daha yavaştır. Çağırdığınız gibi bir döngü olduğu gibi içinde tekrar tekrar çağrılan bir işlev ise `CallByName` performansı üzerinde önemli bir etkisi olabilir.  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:Microsoft.VisualBasic.Interaction.CallByName%2A>
- [Nesne Türünü Belirleme](../../../../visual-basic/programming-guide/language-features/early-late-binding/determining-object-type.md)
