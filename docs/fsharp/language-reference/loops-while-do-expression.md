---
title: 'Döngüler: while...do İfadesi'
description: 'Bkz: nasıl sırada... yapmak ifadesi belirtilen test koşulu true olduğu sürece, yinelemeli yürütme (döngü) gerçekleştirmek için kullanılır.'
ms.date: 05/16/2016
ms.openlocfilehash: 5823ace27348ff4d4397a726bf2254f8fa0ee09b
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65641827"
---
# <a name="loops-whiledo-expression"></a>Döngüler: while...do İfadesi

`while...do` İfadesi belirtilen test koşulu true olduğu sürece, yinelemeli yürütme (döngü) gerçekleştirmek için kullanılır.

## <a name="syntax"></a>Sözdizimi

```fsharp
while test-expression do
    body-expression
```

## <a name="remarks"></a>Açıklamalar

*Test ifade* ise; değerlendirilir `true`, *gövde ifadesi* yürütülür ve test ifade tekrar değerlendirilir. *Gövde ifadesi* türüne sahip olmalıdır `unit`. Test ifade ise `false`, yineleme sona erer.

Aşağıdaki örnek, kullanımını gösterir `while...do` ifade.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5301.fs)]

Önceki kodun çıktısı biri son 10'dur bir rastgele sayı 1 ile 20 arasında akışıdır.

```
13 19 8 18 16 2 10
Found a 10!
```

> [!NOTE]
> Kullanabileceğiniz `while...do` sequence ifadeleri ve diğer hesaplama ifadeleri, özelleştirilmiş bir sürümünü durumda `while...do` ifade kullanılır. Daha fazla bilgi için [dizileri](sequences.md), [zaman uyumsuz iş akışları](asynchronous-workflows.md), ve [hesaplama ifadeleri](computation-expressions.md).

## <a name="see-also"></a>Ayrıca bkz.

- [F# Dili Başvurusu](index.md)
- [Döngüler: `for...in` İfade](loops-for-in-expression.md)
- [Döngüler: `for...to` İfade](loops-for-to-expression.md)
