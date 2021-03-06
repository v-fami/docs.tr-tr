---
title: CType İşlevi (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.CType
helpviewer_keywords:
- expression conversion results
- explicit data type conversions [Visual Basic]
- CType function
- conversions [Visual Basic], expression
ms.assetid: dd4b29e7-6fa1-428c-877e-69955420bb72
ms.openlocfilehash: dbf01263723a9e2890dab57d5ffc3d467ed250fc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61801685"
---
# <a name="ctype-function-visual-basic"></a>CType İşlevi (Visual Basic)

Belirtilen veri türü, nesne, yapısı, sınıf veya arabirim için bir ifade açıkça dönüştürülmesinin sonucunu döndürür.

## <a name="syntax"></a>Sözdizimi

```
CType(expression, typename)
```

## <a name="parts"></a>Bölümler

`expression` Herhangi bir geçerli ifade. Varsa değerini `expression` tarafından izin verilen aralığın dışında `typename`, Visual Basic bir özel durum oluşturur.

`typename` Dahilinde geçerli olan herhangi bir ifade bir `As` yan tümcesinde bir `Dim` deyimi, diğer bir deyişle, tüm veri türü, nesne, yapısı, sınıfı veya arabirim adı.

## <a name="remarks"></a>Açıklamalar

> [!TIP]
> Bir tür dönüştürmesi gerçekleştirmek için aşağıdaki işlevler de kullanabilirsiniz:
>
> - Dönüştürme işlevleri gibi yazın `CByte`, `CDbl`, ve `CInt` belirli veri türüne dönüştürme yapan. Daha fazla bilgi için [tür dönüştürme işlevleri](../../../visual-basic/language-reference/functions/type-conversion-functions.md).
> - [DirectCast işleci](../../../visual-basic/language-reference/operators/directcast-operator.md) veya [TryCast işleci](../../../visual-basic/language-reference/operators/trycast-operator.md). Bu işleçler, bir türden devralamaz veya diğer türü uyguluyor gerektirir. Biraz daha iyi performans sağlarlar `CType` ve ondan dönüştürme yaparken `Object` veri türü.

`CType` Bu da dönüştürme kodunun ifadeyi değerlendiren kodun bir parçası olduğu anlamına gelir derlenmiş satır içidir. Bazı durumlarda, dönüştürmeyi gerçekleştirmek için bir yordam çağrılmadığından kod daha hızlı çalışır.

Öğesinden dönüştürme tanımlanmadıysa `expression` için `typename` (örneğin, `Integer` için `Date`), Visual Basic bir derleme zamanı hata iletisi görüntüler.

Çalışma zamanında bir dönüştürme başarısız olursa uygun özel durum oluşturulur. Bir daraltma dönüşümü başarısız olursa bir <xref:System.OverflowException> en yaygın sonuçtur. Dönüştürme tanımlanmamışsa, bir <xref:System.InvalidCastException> oluşturulur. Örneğin, bu durum meydana gelebilir `expression` türünde `Object` ve onun çalışma zamanı tür dönüştürmesi bulunmadığında `typename`.

Veri türü `expression` veya `typename` bir sınıf veya yapı tanımladığınız, tanımlayabileceğiniz `CType` sınıf veya yapıda dönüştürme işleci. Böylece `CType` işlevi gören bir *işleci aşırı*. Bunu yaparsanız, sınıf veya yapı, oluşturulabilecek özel durumlar dahil olmak üzere ve dönüştürmelerin davranışını denetleyebilirsiniz.

## <a name="overloading"></a>Aşırı Yükleme

`CType` İşleci de aşırı yüklenebilir bir sınıf veya yapı, kodunuz dışında tanımlanan. Kodunuz için veya bu tür bir sınıf veya yapı dönüştürüldüyse davranışını anladığınızdan emin olun, `CType` işleci. Daha fazla bilgi için [işleç yordamları](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).

## <a name="converting-dynamic-objects"></a>Dinamik nesneleri dönüştürme

Dinamik nesnelerin tür dönüştürmeleri kullanan kullanıcı tanımlı dinamik dönüştürmeler tarafından gerçekleştirilen <xref:System.Dynamic.DynamicObject.TryConvert%2A> veya <xref:System.Dynamic.DynamicMetaObject.BindConvert%2A> yöntemleri. Dinamik nesnelerle çalışıyorsanız kullanın <xref:Microsoft.VisualBasic.Conversion.CTypeDynamic%2A> dinamik nesneyi dönüştürmek için yöntemi.

## <a name="example"></a>Örnek

Aşağıdaki örnekte `CType` bir ifadeye dönüştürmek için işlevi `Single` veri türü.

[!code-vb[VbVbalrFunctions#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrFunctions/VB/Class1.vb#24)]

Diğer örnekler için [örtük ve açık dönüştürmeler](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md).

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.OverflowException>
- <xref:System.InvalidCastException>
- [Tür Dönüştürme İşlevleri](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [Dönüştürme İşlevleri](../../../visual-basic/language-reference/functions/conversion-functions.md)
- [Operator Deyimi](../../../visual-basic/language-reference/statements/operator-statement.md)
- [Nasıl yapılır: Bir dönüşüm işleci tanımlama](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
- [.NET Framework'te tür dönüştürme](../../../standard/base-types/type-conversion.md)
