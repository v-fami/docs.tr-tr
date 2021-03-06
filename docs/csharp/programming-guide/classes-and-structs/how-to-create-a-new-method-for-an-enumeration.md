---
title: 'Nasıl yapılır: -Numaralandırma için yeni bir yöntem oluşturma C# Programlama Kılavuzu'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- enumerations [C#]
- extension methods [C#], for enums
- enum extensibility [C#]
ms.assetid: 100106f9-1e54-462c-8ebe-3892fe23b6eb
ms.openlocfilehash: 2ca388d19c0e4e1b098076caa5baa0a83cc0dd4c
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65585895"
---
# <a name="how-to-create-a-new-method-for-an-enumeration-c-programming-guide"></a>Nasıl yapılır: Numaralandırma için yeni bir yöntem oluşturma (C# Programlama Kılavuzu)
Belirli numaralandırma türüne özgü işlevsellik eklemek için genişletme yöntemleri kullanabilirsiniz.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte, `Grades` numaralandırması bir öğrenci bir sınıfta alabileceğiniz olası harf dereceleri temsil eder. Adlı bir genişletme yöntemi `Passing` eklenir `Grades` artık o türün her örneğinin "ya da değil, geçirme sınıf temsil edip etmediğini bilebilmesi" yazın.  
  
 [!code-csharp[csProgGuideExtensionMethods#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideExtensionMethods/cs/extensionmethods.cs#2)]  
  
 Unutmayın `Extensions` sınıfı ayrıca dinamik olarak güncelleştirilen bir statik değişken içerir ve dönüş değeri genişletme yöntemi bu değişkenin geçerli değeri yansıtır. Bu, arka planda, bunlar tanımlanır doğrudan statik sınıf üzerinde genişletme yöntemleri çağrılır, gösterir.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [C# Programlama Kılavuzu](../../../csharp/programming-guide/index.md)
- [Genişletme Yöntemleri](../../../csharp/programming-guide/classes-and-structs/extension-methods.md)
