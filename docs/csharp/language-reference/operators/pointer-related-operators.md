---
title: İşaretçi işleçleri - ilgili C# başvurusu
description: Hakkında bilgi edinin C# işaretçilerle çalışırken kullanabileceğiniz işleçleri.
ms.date: 05/20/2019
author: pkulikov
f1_keywords:
- ->_CSharpKeyword
helpviewer_keywords:
- pointer related operators [C#]
- address-of operator [C#]
- '& operator [C#]'
- pointer indirection operator [C#]
- dereference operator [C#]
- '* operator [C#]'
- pointer member access operator [C#]
- -> operator [C#]
- pointer element access [C#]
- '[] operator [C#]'
- pointer arithmetic [C#]
- pointer increment [C#]
- pointer decrement [C#]
- pointer comparison [C#]
ms.openlocfilehash: 012e4fe9b8ee49f3b6b7240ac4ccb21dba70a8a9
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65882661"
---
# <a name="pointer-related-operators-c-reference"></a>İşaretçi ilgili işleçleri (C# Başvurusu)

İşaretçiler ile çalışmak için aşağıdaki işleçleri kullanabilirsiniz:

- Birli [ `&` (adres-of)](#address-of-operator-) işleci: değişkenin adresini almak için
- Birli [ `*` (işaretçi yöneltmesi)](#pointer-indirection-operator-) işleci: işaretçi tarafından işaret edilen değişkeni almak için
- [ `->` (Üye erişimi)](#pointer-member-access-operator--) ve [ `[]` (öğe erişimi)](#pointer-element-access-operator-) işleçleri
- Aritmetik işleçler [ `+`, `-`, `++`, ve `--`](#pointer-arithmetic-operators)
- Karşılaştırma işleçleri [ `==`, `!=`, `<`, `>`, `<=`, ve `>=`](#pointer-comparison-operators)

İşaretçi türleri hakkında daha fazla bilgi için bkz. [işaretçi türleri](../../programming-guide/unsafe-code-pointers/pointer-types.md).

> [!NOTE]
> İşaretçiler içeren herhangi bir işlem gerektiren [güvenli](../keywords/unsafe.md) bağlamı. Güvenli olmayan bloklar içeren kod ile derlenmelidir [ `-unsafe` ](../compiler-options/unsafe-compiler-option.md) derleyici seçeneği.

## <a name="address-of-operator-amp"></a>Address-of işleci &amp;

Birli `&` işleci, işlenenin adresini verir:

[!code-csharp[address of local](~/samples/snippets/csharp/language-reference/operators/PointerOperators.cs#AddressOf)]

İşleneni `&` işleci, sabit bir değişken olmalıdır. *Sabit* değişkenlerdir bir işlem tarafından etkilenmez, depolama konumları bulunan değişkenleri [çöp toplayıcı](../../../standard/garbage-collection/index.md). Yukarıdaki örnekte, yerel değişken `number` yığında yer aldığından bir sabit değişkenidir. Atık toplayıcı (örneğin, yeniden konumlandırılması) etkilenen depolama konumları bulunan değişkenleri çağrılır *taşınabilir* değişkenleri. Nesne alanları ve dizi öğeleri taşınabilir değişkenleri örnekleridir. "Düzeltme" veya "sabitleme" taşınabilir değişkenin adresini alabilirsiniz ile [sabit](../keywords/fixed-statement.md) deyimi. Alınan adresi süresi boyunca yalnızca geçerli `fixed` deyim bloğu. Aşağıdaki örnek nasıl kullanılacağını gösterir `fixed` deyimi ve `&` işleci:

[!code-csharp[address of fixed](~/samples/snippets/csharp/language-reference/operators/PointerOperators.cs#AddressOfFixed)]

Bir sabit bir değer veya adresi alınamıyor.

Sabit ve taşınabilir değişkenleri hakkında daha fazla bilgi için bkz. [sabit ve taşınabilir değişkenleri](~/_csharplang/spec/unsafe-code.md#fixed-and-moveable-variables) bölümünü [ C# dil belirtimi](~/_csharplang/spec/introduction.md).

İkili `&` işleci hesaplar [mantıksal AND](boolean-logical-operators.md#logical-and-operator-) Boole işlenenleri, veya [mantıksal bit düzeyinde AND](bitwise-and-shift-operators.md#logical-and-operator-) integral işlenenleri biri.

## <a name="pointer-indirection-operator-"></a>İşaretçi yöneltme işleci *

İşaretçi yöneltme işleci birli `*` işlenenin işaret ettiği değişken alır. Başvuru işleci olarak da bilinen olduğu. İşleneni `*` işleci, bir işaretçi türü olmalıdır.

[!code-csharp[pointer indirection](~/samples/snippets/csharp/language-reference/operators/PointerOperators.cs#PointerIndirection)]

Uygulayamazsınız `*` türündeki bir ifade işlecine `void*`.

İkili `*` işleci hesaplar [ürün](arithmetic-operators.md#multiplication-operator-) sayısal işlenenleri biri.

## <a name="pointer-member-access-operator--"></a>İşaretçi üye erişimi işleci ' ->

`->` İşleci birleştirir [işaretçi yöneltmesi](#pointer-indirection-operator-) ve [üye erişimi](member-access-operators.md#member-access-operator-). Diğer bir deyişle, `x` bir işaretçi türü `T*` ve `y` erişilebilir bir üyesidir `T`, formun bir ifade

```csharp
x->y
```

eşdeğerdir

```csharp
(*x).y
```

Aşağıdaki örnek, kullanımını gösterir. `->` işleci:

[!code-csharp[pointer member access](~/samples/snippets/csharp/language-reference/operators/PointerOperators.cs#MemberAccess)]

Uygulayamazsınız `->` türündeki bir ifade işlecine `void*`.

## <a name="pointer-element-access-operator-"></a>İşaretçi öğesi erişim operator]

Bir ifade için `p` bir işaretçi türü, bir işaretçiyi öğe erişimi formun `p[n]` olarak değerlendirilir `*(p + n)`burada `n` örtük olarak dönüştürülebilir türde olmalıdır `int`, `uint`, `long`, veya `ulong`. Davranışı hakkında bilgi için `+` işaretçisi olan işleç bkz [ekleme veya çıkarma, bir tamsayı değeri ya da bir işaretçiden](#addition-or-subtraction-of-an-integral-value-to-or-from-a-pointer) bölümü.

Aşağıdaki örnek, bir işaretçi ile dizi öğelerini nasıl erişileceğini gösteren ve `[]` işleci:

[!code-csharp[pointer element access](~/samples/snippets/csharp/language-reference/operators/PointerOperators.cs#ElementAccess)]

Örnekte [ `stackalloc` işleci](../keywords/stackalloc.md) bir yığında bellek bloğu ayrılamadı.

> [!NOTE]
> İşaretçi öğesi erişim işleci için işlemleri denetlemez hataları.

Kullanamazsınız `[]` işaretçi türündeki bir ifade ile öğesi erişim için `void*`.

Ayrıca `[]` işleci için [dizi öğesi veya dizin oluşturucu erişim](member-access-operators.md#indexer-operator-).

## <a name="pointer-arithmetic-operators"></a>İşaretçi aritmetik işleçler

İşaretçiler ile aşağıdaki aritmetik işlemleri gerçekleştirebilirsiniz:

- Eklemek veya çıkarmak için veya işaretçiden bir tamsayı değeri
- İki işaretçi çıkarma
- Artırma veya azaltma bir işaretçi

Türü işaretçileri olan işlemleri gerçekleştiremezsiniz `void*`.

Sayısal türler ile desteklenen aritmetik işlemler hakkında daha fazla bilgi için bkz. [aritmetik işleçler](arithmetic-operators.md).

### <a name="addition-or-subtraction-of-an-integral-value-to-or-from-a-pointer"></a>Toplama veya bir tamsayı değeri ya da bir işaretçiden çıkarma

İşaretçisi `p` türü `T*` ve ifade `n` örtük olarak dönüştürülebilir bir türün `int`, `uint`, `long`, veya `ulong`, toplama ve çıkarma tanımlandığı gibi:

- Her ikisi de `p + n` ve `n + p` ifadeler üretmek türünde bir işaretçi `T*` sonuçlarının eklemesini `n * sizeof(T)` tarafından verilen adresine `p`.
- `p - n` Türünde bir işaretçi ifadesi oluşturur `T*` sonuçlarının arasındaki çıkarma işleminin `n * sizeof(T)` tarafından verilen adresinden `p`.

[ `sizeof` İşleci](../keywords/sizeof.md) bir tür bayt cinsinden boyutunu alır.

Aşağıdaki örnek, kullanımını gösterir. `+` işleci bir işaretçi ile:

[!code-csharp[pointer addition](~/samples/snippets/csharp/language-reference/operators/PointerOperators.cs#AddNumber)]

### <a name="pointer-subtraction"></a>İşaretçi çıkarması

İki işaretçileri `p1` ve `p2` türü `T*`, ifade `p1 - p2` tarafından verilen adresler arasındaki farkı verir `p1` ve `p2` bölü `sizeof(T)`. Sonuç türü olan `long`. Diğer bir deyişle, `p1 - p2` olarak hesaplanan `((long)(p1) - (long)(p2)) / sizeof(T)`.

Aşağıdaki örnek, işaretçi çıkarması gösterir:

[!code-csharp[pointer subtraction](~/samples/snippets/csharp/language-reference/operators/PointerOperators.cs#SubtractPointers)]

### <a name="pointer-increment-and-decrement"></a>İşaretçi artırma ve azaltma

`++` Artış işleci [ekler](#addition-or-subtraction-of-an-integral-value-to-or-from-a-pointer) işaretçi işleneniyle 1. `--` Azaltma işleci [çıkarır](#addition-or-subtraction-of-an-integral-value-to-or-from-a-pointer) işaretçi işleneniyle 1.

Her iki işleçler iki biçimde desteklenir: sonek (`p++` ve `p--`) ve önek (`++p` ve `--p`). Sonucu `p++` ve `p--` değeri `p` *önce* işlemi. Sonucu `++p` ve `--p` değeri `p` *sonra* işlemi.

Aşağıdaki örnek, sonek hem önek artırma işleçleri davranışını gösterir:

[!code-csharp[pointer increment](~/samples/snippets/csharp/language-reference/operators/PointerOperators.cs#Increment)]

## <a name="pointer-comparison-operators"></a>İşaretçi Karşılaştırma işleçleri

Kullanabileceğiniz `==`, `!=`, `<`, `>`, `<=`, ve `>=` işlenen bir işaretçi türünü karşılaştırmak için işleçleri dahil olmak üzere `void*`. Bu işleçler, işaretsiz tamsayılar değilmiş gibi iki işlenen tarafından belirtilen adresi karşılaştırın.

Bu işleçler diğer türündeki işlenenler için davranış hakkında daha fazla bilgi için bkz. [eşitlik işleçleri](equality-operators.md) ve [Karşılaştırma işleçleri](comparison-operators.md) makaleler.

## <a name="operator-precedence"></a>İşleç önceliği

Aşağıdaki liste siparişler işaretçi işleçleri en yüksek öncelikten en düşük başlangıç ilgili:

- Sonek artırma `x++` ve azaltma `x--` işleçler ve `->` ve `[]` işleçleri
- Önek artırma `++x` ve azaltma `--x` işleçler ve `&` ve `*` işleçleri
- Eklenebilir `+` ve `-` işleçleri
- Karşılaştırma `<`, `>`, `<=`, ve `>=` işleçleri
- Eşitlik `==` ve `!=` işleçleri

Parantez kullanın `()`İşleç önceliği tarafından belirlenen değerlendirmenin sırasını değiştirmek için.

Tam listesi için C# işleçler, öncelik düzeyine göre sıralanmış bkz [ C# işleçleri](index.md).

## <a name="operator-overloadability"></a>İşleç overloadability

Kullanıcı tanımlı bir tür işaretçisi aşırı yüklenemez ilgili işleçleri `&`, `*`, `->`, ve `[]`.

## <a name="c-language-specification"></a>C# dili belirtimi

Daha fazla bilgi için aşağıdaki bölümlere bakın [ C# dil belirtimi](~/_csharplang/spec/introduction.md):

- [Sabit ve taşınabilir değişkenleri](~/_csharplang/spec/unsafe-code.md#fixed-and-moveable-variables)
- [Address-of işleci](~/_csharplang/spec/unsafe-code.md#the-address-of-operator)
- [İşaretçi yöneltmesi](~/_csharplang/spec/unsafe-code.md#pointer-indirection)
- [İşaretçi üye erişimi](~/_csharplang/spec/unsafe-code.md#pointer-member-access)
- [İşaretçi öğe erişimi](~/_csharplang/spec/unsafe-code.md#pointer-element-access)
- [İşaretçi aritmetiği](~/_csharplang/spec/unsafe-code.md#pointer-arithmetic)
- [İşaretçi artırma ve azaltma](~/_csharplang/spec/unsafe-code.md#pointer-increment-and-decrement)
- [İşaretçi karşılaştırması](~/_csharplang/spec/unsafe-code.md#pointer-comparison)

## <a name="see-also"></a>Ayrıca bkz.

- [C# başvurusu](../index.md)
- [C# Programlama Kılavuzu](../../programming-guide/index.md)
- [C# İşleçleri](index.md)
- [İşaretçi türleri](../../programming-guide/unsafe-code-pointers/pointer-types.md)
- [`unsafe` Anahtar sözcüğü](../keywords/unsafe.md)
- [`fixed` Anahtar sözcüğü](../keywords/fixed-statement.md)
- [`stackalloc` İşleci](../keywords/stackalloc.md)
- [`sizeof` İşleci](../keywords/sizeof.md)
