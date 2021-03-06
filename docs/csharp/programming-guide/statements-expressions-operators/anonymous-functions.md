---
title: Anonim işlevler - C# Programlama Kılavuzu
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- lambda expressions [C#], as anonymous functions
- anonymous functions [C#]
- anonymous methods [C#]
ms.assetid: 6ce3f04d-0c71-4728-9127-634c7e9a8365
ms.openlocfilehash: 338f4b34a5de84d4ce2eb9e0bd6f4c9ebe360fa4
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65584269"
---
# <a name="anonymous-functions-c-programming-guide"></a>Anonim İşlevler (C# Programlama Kılavuzu)
Bir anonim işlev bir "satır içi" deyimi veya bir temsilci türünün beklendiği her yerde kullanılabilir ifade ' dir. Adlandırılmış bir temsilci başlatmak veya bir yöntem parametresi olarak bir adlandırılmış bir temsilci türü yerine geçirmek için kullanabilirsiniz.  
  
 Aşağıdaki konular, ayrı ayrı ele alınmıştır anonim İşlevler, iki tür vardır:  
  
- [Lambda ifadeleri](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md).  
  
- [Anonim Metotlar](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md)  
  
    > [!NOTE]
    >  Lambda ifadeleri ifade ağaçları ve temsilciler bağlı olabilir.  
  
## <a name="the-evolution-of-delegates-in-c"></a>C'de temsilciler evrimi\#
 C# 1. 0'bir temsilci örneğini açıkça, kod içinde başka bir yerde tanımlanmış bir yöntemle başlatarak oluşturuldu. C# 2.0 içinde bir temsilci çağrısı yürütülebilecek Adlandırılmamış satır içi deyim blokları yazmak için bir yol olarak anonim yöntemler kavramını sundu. Anonim yöntemler için kavram benzer, ancak daha ifadesel ve kısa olan lambda ifadeleri, C# 3.0 sunmuştur. Bu iki özellik topluca olarak bilinen *anonim işlevler*. Genel olarak, sürüm 3.5 ve daha sonraki .NET Framework sürümünü hedefleyen uygulamalar, lambda ifadeleri kullanmanız gerekir.  
  
 Aşağıdaki örnek, C# 3.0 için C# 1.0 temsilci oluşturma gelişimini gösterir:  
  
 [!code-csharp[csProgGuideLINQ#65](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideLINQ/CS/csRef30LangFeatures_2.cs#65)]  
  
## <a name="c-language-specification"></a>C# Dil Belirtimi  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Deyimler, İfadeler ve İşleçler](../../../csharp/programming-guide/statements-expressions-operators/index.md)
- [Lambda İfadeleri](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md)
- [Temsilciler](../../../csharp/programming-guide/delegates/index.md)
- [İfade ağaçları (C#)](../concepts/expression-trees/index.md)
