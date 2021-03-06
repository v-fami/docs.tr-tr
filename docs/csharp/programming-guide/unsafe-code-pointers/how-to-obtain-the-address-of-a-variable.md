---
title: 'Nasıl yapılır: - değişkenin adresini edinme C# Programlama Kılavuzu'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- variables [C#], address of
- pointers [C#], & operator
- pointer expressions [C#], address-of operator
ms.assetid: 44fe2cd9-a64f-4ef5-be2a-09ce807c0182
ms.openlocfilehash: bc5776bc57096b88a71ff786915553ae9aa04b7b
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65635056"
---
# <a name="how-to-obtain-the-address-of-a-variable-c-programming-guide"></a>Nasıl yapılır: değişkenin adresini edinme (C# Programlama Kılavuzu)

Sabit bir değişkene değerlendirir, tekli ifade adresini almak için address-of işlecini kullanın `&`:  
  
```csharp  
int number;  
int* p = &number; //address-of operator &  
```  
  
 Address-of işleci yalnızca bir değişkene uygulanabilir. Değişken taşınabilir bir değişken ise kullanabileceğiniz [fixed statement](../../../csharp/language-reference/keywords/fixed-statement.md) adresini almadan önce değişkeni geçici olarak çözmek için. Taşınabilir değişkenleri hakkında daha fazla bilgi için bkz. [sabit ve taşınabilir değişkenleri](/dotnet/csharp/language-reference/language-specification/unsafe-code#fixed-and-moveable-variables). 
  
 Bu değişkeni başlatıldığından emin olmak sizin sorumluluğunuzdur. Değişken başlatılmadı, derleyici bir hata iletisi sorunu değildir.  
  
 Bir sabit bir değer veya adresi alınamıyor.  
  
## <a name="example"></a>Örnek  
 Bu örnekte, bir işaretçi `int`, `p`, bildirilmiş ve bir tamsayı değişkeninin adresi atanan `number`. Değişken `number` atamaya sonucu olarak başlatılır `*p`. Bu atama deyimi, değişkenin başlatılması yorum `number` kaldırılır, ancak hiçbir derleme zamanı hata verilir.  

> [!NOTE]
> Bu örneği derlemek [ `-unsafe` ](../../language-reference/compiler-options/unsafe-compiler-option.md) derleyici seçeneği.
  
 [!code-csharp[address-of-a-variable](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuidePointers/CS/Pointers.cs#8)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [C# Programlama Kılavuzu](../../../csharp/programming-guide/index.md)
- [İşaretçi türleri](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [Türler](../../../csharp/language-reference/keywords/types.md)
- [unsafe](../../../csharp/language-reference/keywords/unsafe.md)
- [fixed Deyimi](../../../csharp/language-reference/keywords/fixed-statement.md)
- [stackalloc](../../../csharp/language-reference/keywords/stackalloc.md)
