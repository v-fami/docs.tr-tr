---
title: örtük - C# başvurusu
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- implicit
- implicit_CSharpKeyword
helpviewer_keywords:
- implicit keyword [C#]
ms.assetid: 34db590e-eb3a-4f11-88d0-ffb3cd753dab
ms.openlocfilehash: d3e1cb9d6fb37617c6e2aa7070b006c594d39762
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61661483"
---
# <a name="implicit-c-reference"></a>implicit (C# Başvurusu)

`implicit` Anahtar sözcüğü, bir kullanıcı tanımlı örtük tür dönüştürme işleci bildirmek için kullanılır. Dönüştürme veri kaybına neden olmayan garanti, kullanıcı tanımlı bir tür ve başka bir türü arasında örtülü dönüştürmeler etkinleştirmek için bunu kullanın.

## <a name="example"></a>Örnek

[!code-csharp[csrefKeywordsConversion#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsConversion/CS/csrefKeywordsConversion.cs#5)]

Örtük dönüştürmeleri gereksiz atamalar ortadan kaldırarak, kaynak kodunun okunabilirliğini artırabilir. Ancak, örtük dönüştürmelerin açıkça bir türden diğerine dönüştürme yapmak programcılar gerektirmediğinden, bakım beklenmeyen sonuçları engellemek için izlenmelidir. Genel olarak, örtük dönüşüm işleçleri, hiçbir zaman özel durumlar ve Programcı tanıma güvenli bir şekilde kullanılabilir böylece hiçbir zaman bilgileri kaybedersiniz. Bir dönüştürme işleci bu ölçütlerin karşılayamazsanız işaretlenmelidir `explicit`. Daha fazla bilgi için [dönüştürme işleçleri kullanarak](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md).

## <a name="c-language-specification"></a>C# dili belirtimi

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Ayrıca bkz.

- [C# başvurusu](../index.md)
- [C# Programlama Kılavuzu](../../programming-guide/index.md)
- [C# Anahtar Sözcükleri](index.md)
- [explicit](explicit.md)
- [İşleci (C# Başvurusu)](operator.md)
- [Nasıl yapılır: Yapılar arasında kullanıcı tanımlı Dönüşümler Uygulama](../../programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)
