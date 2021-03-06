---
title: Visual Basic'de Genel Yordamlar
ms.date: 07/20/2015
helpviewer_keywords:
- generic methods [Visual Basic], type inference
- generics [Visual Basic], type inference
- procedures [Visual Basic], generic
- generic procedures
- type inference, generics
- generic methods [Visual Basic]
- type inference
- generics [Visual Basic], procedures
- generic procedures [Visual Basic], type inference
ms.assetid: 95577b28-137f-4d5c-a149-919c828600e5
ms.openlocfilehash: 4aed16ce9eb59da54156a0cd5f1594819788521b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61906600"
---
# <a name="generic-procedures-in-visual-basic"></a>Visual Basic'de Genel Yordamlar
A *genel yordam*ayrıca adlı bir *genel yöntem*, en az bir tür parametreyle tanımlanan bir yordam olduğunu. Bu, çağıran kodu yordam çağrıları her zaman veri türleri, gereksinimleri ile uyumlu hale getirmenizi sağlar.  
  
 Bir yordam, yalnızca genel bir sınıf veya yapının genel bir yapı içinde tanımlanan da genel değil. Yordamı, genel olması için ek normal işlem sürebilir herhangi bir parametre olarak en az bir tür parametresi atmanız gerekir. Bir genel sınıf veya yapı jenerik olmayan yordamları ve jenerik olmayan bir sınıf, yapı, içerebilir veya modülü genel yordamlar içerebilir.  
  
 Genel bir yordam, normal parametre listesinde bir ve onun yordamdaki kodu varsa, dönüş türü, tür parametreleri kullanabilirsiniz.  
  
## <a name="type-inference"></a>Tür Çıkarma  
 Herhangi bir tür bağımsız değişkeni sağlamadan genel bir yordam çağırabilir. Bu şekilde çağırırsanız derleyici yordamın türü bağımsız değişkenler için uygun veri türlerini belirlemek çalışır. Bu adlandırılır *anlam çıkarma*. Aşağıdaki kod bir çağrı gösterir, derleyicinin tür geçmelidir algılar `String` tür parametresi için `t`.  
  
 [!code-vb[VbVbalrDataTypes#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDataTypes/VB/Class1.vb#15)]  
  
 Derleyici, tür bağımsız değişkenlerini çağrınızın bağlamından çıkarsanamaz. bir hata bildirir. Bu tür bir hataya olası nedenlerinden biri, bir dizi derece uyuşmazlığı olmasıdır. Örneğin, bir tür parametresi bir dizi olarak normal parametresini tanımlama varsayalım. Genel bir yordamı çağırma sağlayan bir dizi farklı boyut sayısına (sayı) boyut uyuşmazlığı tür çıkarımı başarısız olmasına neden olur. Aşağıdaki kod bir çağrı gösterir, tek boyutlu dizi bekliyor bir yordam için iki boyutlu bir dizi geçirilir.  
  
```vb  
Public Sub demoSub(Of t)(ByVal arg() As t)
End Sub

Public Sub callDemoSub()
    Dim twoDimensions(,) As Integer
    demoSub(twoDimensions)
End Sub
```
  
 Tür çıkarımı, yalnızca tüm tür bağımsız değişkenlerini gt;(yok) çağırabilirsiniz. Bir tür bağımsız değişkeni sağlarsanız, tüm bunları sağlamanız gerekir.  
  
 Tür çıkarımı, yalnızca genel yordamlar için desteklenir. Genel sınıflar, yapılar, arabirimler veya temsilciler tür çıkarımı çağrılamıyor.  
  
## <a name="example"></a>Örnek  
  
### <a name="description"></a>Açıklama  
 Aşağıdaki örnek, genel tanımlar `Function` yordamı belirli bir öğenin bir dizide bulunacak. Bu, bir tür parametresi tanımlar ve parametre listesinde iki parametre oluşturmak için kullanır.  
  
### <a name="code"></a>Kod  
 [!code-vb[VbVbalrDataTypes#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDataTypes/VB/Class1.vb#14)]  
  
### <a name="comments"></a>Açıklamalar  
 Yukarıdaki örnekte karşılaştırma gerektirir `searchValue` her öğeye karşı `searchArray`. Bu yeteneği sağlamak için bu tür parametresi kısıtlaması uygular `T` uygulamak için <xref:System.IComparable%601> arabirimi. Kod <xref:System.IComparable%601.CompareTo%2A> yöntemi yerine `=` işleci, bir tür bağımsız değişkeni için sağlanan garanti olduğundan `T` destekler `=` işleci.  
  
 Test edebilirsiniz `findElement` aşağıdaki kodla yordamı.  
  
 [!code-vb[VbVbalrDataTypes#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDataTypes/VB/Class1.vb#13)]  
  
 Önceki çağrılar `MsgBox` sırasıyla "0", "1" ve "-1" görüntüler.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Visual Basic'de genel türler](../../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)
- [Nasıl yapılır: Farklı Veri Türlerinde Aynı İşlevselliği Sağlayabilen Bir Sınıf Tanımlama](../../../../visual-basic/programming-guide/language-features/data-types/how-to-define-a-class-that-can-provide-identical-functionality.md)
- [Nasıl yapılır: Genel Bir Sınıf Kullanma](../../../../visual-basic/programming-guide/language-features/data-types/how-to-use-a-generic-class.md)
- [Yordamlar](../../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [Yordam Parametreleri ve Bağımsız Değişkenleri](../../../../visual-basic/programming-guide/language-features/procedures/procedure-parameters-and-arguments.md)
- [Tür Listesi](../../../../visual-basic/language-reference/statements/type-list.md)
- [Parametre Listesi](../../../../visual-basic/language-reference/statements/parameter-list.md)
