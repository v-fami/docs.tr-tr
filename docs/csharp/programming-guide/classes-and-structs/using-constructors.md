---
title: Oluşturucuları - kullanarak C# Programlama Kılavuzu
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- constructors [C#], about constructors
ms.assetid: 464253b2-fd5d-469a-836d-df0fdf2a43f7
ms.openlocfilehash: 1f47459fc5002118d94cc8d389f35c18fa2c611a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61703289"
---
# <a name="using-constructors-c-programming-guide"></a>Oluşturucular Kullanma (C# Programlama Kılavuzu)
Olduğunda bir [sınıfı](../../../csharp/language-reference/keywords/class.md) veya [yapı](../../../csharp/language-reference/keywords/struct.md) olan oluşturulan, kendi Oluşturucu çağrılır. Oluşturucular sınıf veya yapının aynı ada sahip ve bunlar genellikle yeni nesnenin veri üyeleri başlatılamıyor.  
  
 Aşağıdaki örnekte, bir sınıf adlı `Taxi` basit bir oluşturucu kullanılarak tanımlanır. Bu sınıf ile Örneklendirilmiş [yeni](../../../csharp/language-reference/keywords/new.md) işleci. `Taxi` Oluşturucusu tarafından çağrıldığında `new` işleci bellek hemen sonra yeni nesne için ayrılır.  
  
 [!code-csharp[csProgGuideObjects#53](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#53)]  
  
 Herhangi bir parametre alan bir oluşturucu olarak adlandırılan bir *parametresiz oluşturucu*. Varsayılan Oluşturucu çağrılır kullanarak bir nesne örneği her `new` işleci ve herhangi bir bağımsız değişken için sağlanan `new`. Daha fazla bilgi için [örnek oluşturucuları](../../../csharp/programming-guide/classes-and-structs/instance-constructors.md).  
  
 Bir sınıf olmadığı sürece [statik](../../../csharp/language-reference/keywords/static.md), Oluşturucular, genel bir parametresiz oluşturucusu tarafından verilen olmadan sınıfları C# sınıfı örneğini oluşturmada etkinleştirmek için derleyici. Daha fazla bilgi için [statik sınıflar ve statik sınıf üyeleri](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md).  
  
 Bir sınıf oluşturucu özel gibi yaparak oluşturulmasını engelleyebilir:  
  
 [!code-csharp[csProgGuideObjects#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#11)]  
  
 Daha fazla bilgi için [özel oluşturucular](../../../csharp/programming-guide/classes-and-structs/private-constructors.md).  
  
 Oluşturucular için [yapı](../../../csharp/language-reference/keywords/struct.md) türleri sınıf oluşturucuları, benzer ancak `structs` bir derleyici tarafından otomatik olarak sağlandığından, açık parametresiz oluşturucu içeremez. Bu oluşturucu her alanda başlatır `struct` için varsayılan değerleri. Daha fazla bilgi için [varsayılan değerler tablosu](../../../csharp/language-reference/keywords/default-values-table.md). Ancak, bu parametresiz oluşturucu yalnızca, çağrılan `struct` ile örneği `new`. Örneğin, bu kod için parametresiz oluşturucu kullanan <xref:System.Int32>, böylece tamsayı başlatıldığından emin olabilirsiniz:  
  
```csharp  
int i = new int();  
Console.WriteLine(i);  
```  
  
 Kullanmaz çünkü aşağıdaki kod, ancak bir derleyici hatasına neden `new`, ve onu başlatılmamış bir nesne kullanmayı dener:  
  
```  
int i;  
Console.WriteLine(i);  
```  
  
 Alternatif olarak, nesneler temel `structs` (tüm yerleşik sayısal türler dahil) başlatıldı veya atanabilir ve sonra aşağıdaki örnekte olduğu gibi kullanılır:  
  
```  
int a = 44;  // Initialize the value type...  
int b;  
b = 33;      // Or assign it before using it.  
Console.WriteLine("{0}, {1}", a, b);  
```  
  
 Parametresiz oluşturucusu için bir değer türü yöntemini çağırır; dolayısıyla, gerekli değildir.  
  
 Her iki sınıfları ve `structs` parametre oluşturucular tanımlayabilirsiniz. Parametre oluşturucular çağırılır, aracılığıyla bir `new` deyimi veya bir [temel](../../../csharp/language-reference/keywords/base.md) deyimi. Sınıfları ve `structs` birden çok oluşturucular da tanımlayabilirsiniz ve bunların hiçbiri parametresiz bir oluşturucu tanımlamak için gereklidir. Örneğin:  
  
 [!code-csharp[csProgGuideObjects#54](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#54)]  
  
 Bu sınıf aşağıdaki deyimleri kullanarak oluşturulabilir:  
  
 [!code-csharp[csProgGuideObjects#55](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#55)]  
  
 Bir oluşturucu kullanabilirsiniz `base` bir taban sınıfın oluşturucuyu çağırmak için anahtar sözcüğü. Örneğin:  
  
 [!code-csharp[csProgGuideObjects#56](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#56)]  
  
 Blok Oluşturucu için yürütülmeden önce bu örnekte, temel sınıf için oluşturucu çağrılır. `base` Parametrelerle veya parametresiz anahtar sözcüğü kullanılabilir. Oluşturucu herhangi bir parametre için parametre olarak kullanılan `base`, veya bir ifade parçası olarak. Daha fazla bilgi için [temel](../../../csharp/language-reference/keywords/base.md).  
  
 Bir temel sınıf oluşturucusu kullanarak açıkça çağrılmaz, türetilmiş bir sınıf içinde `base` anahtar sözcüğü, parametresiz bir oluşturucusu varsa, çağrıldığında örtük olarak. Bu aşağıdaki Oluşturucusu bildirimleri etkili bir şekilde aynı anlamına gelir:  
  
 [!code-csharp[csProgGuideObjects#58](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#58)]  
  
 [!code-csharp[csProgGuideObjects#57](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#57)]  
  
 Bir temel sınıf parametresiz bir oluşturucu sağlamaz, türetilen sınıfın temel oluşturucu için açık çağrı kullanarak yapmalısınız `base`.  
  
 Bir kurucu kullanarak aynı nesnede başka bir oluşturucu çağırabilirsiniz [bu](../../../csharp/language-reference/keywords/this.md) anahtar sözcüğü. Gibi `base`, `this` parametrelerle veya parametresiz kullanılabilir ve oluşturucu içinde herhangi bir parametre için parametre olarak kullanılabilir `this`, veya bir ifade parçası olarak. Örneğin, önceki örnekte ikinci oluşturucu kullanılarak yazılabilir `this`:  
  
 [!code-csharp[csProgGuideObjects#59](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#59)]  
  
 Kullanımını `this` önceki örnekte anahtar sözcüğü bu oluşturucunun çağrılması neden olur:  
  
 [!code-csharp[csProgGuideObjects#60](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideObjects/CS/Objects.cs#60)]  
  
 Oluşturucular olarak işaretlenebilir [genel](../../../csharp/language-reference/keywords/public.md), [özel](../../../csharp/language-reference/keywords/private.md), [korumalı](../../../csharp/language-reference/keywords/protected.md), [iç](../../../csharp/language-reference/keywords/internal.md), [içkorumalı](../../../csharp/language-reference/keywords/protected-internal.md)veya [korunan özel](../../../csharp/language-reference/keywords/private-protected.md). Bu erişim değiştiricileri kullanıcılar sınıfın sınıf nasıl oluşturabilir tanımlayın. Daha fazla bilgi için [erişim değiştiricileri](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md).  
  
 Bir kurucu kullanarak statik bildirilebilir [statik](../../../csharp/language-reference/keywords/static.md) anahtar sözcüğü. Statik oluşturucular hemen tüm statik alanları erişilir ve statik sınıf üyeleri başlatmak için genellikle kullanılan önce otomatik olarak çağrılır. Daha fazla bilgi için [statik oluşturucular](../../../csharp/programming-guide/classes-and-structs/static-constructors.md).  
  
## <a name="c-language-specification"></a>C# Dil Belirtimi  

Daha fazla bilgi için [örnek oluşturucular](~/_csharplang/spec/classes.md#instance-constructors) ve [statik oluşturucular](~/_csharplang/spec/classes.md#static-constructors) içinde [ C# dil belirtimi](../../language-reference/language-specification/index.md). Dil belirtimi, C# sözdizimi ve kullanımı için kesin bir kaynaktır.
  
## <a name="see-also"></a>Ayrıca bkz.

- [C# Programlama Kılavuzu](../../../csharp/programming-guide/index.md)
- [Sınıflar ve Yapılar](../../../csharp/programming-guide/classes-and-structs/index.md)
- [Oluşturucular](../../../csharp/programming-guide/classes-and-structs/constructors.md)
- [Sonlandırıcılar](../../../csharp/programming-guide/classes-and-structs/destructors.md)
