---
title: "'Extension' özniteliği yalnızca 'Module', 'Sub' veya 'Function' bildirimlerine uygulanabilir"
ms.date: 07/20/2015
f1_keywords:
- bc36550
- vbc36550
helpviewer_keywords:
- BC36550
ms.assetid: 4387a51f-733c-45d7-abdb-eb64d4f51078
ms.openlocfilehash: 88212fb2c04eab61b719a161ae01ccdda9a6110d
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64640720"
---
# <a name="extension-attribute-can-be-applied-only-to-module-sub-or-function-declarations"></a>'Extension' özniteliği yalnızca 'Module', 'Sub' veya 'Function' bildirimlerine uygulanabilir
Visual Basic'te bir veri türü genişletmek için tek bir standart modül içinde bir genişletme yöntemi tanımlamak için yoludur. Genişletme yöntemi olabilir bir `Sub` yordamı veya `Function` yordamı. Tüm uzantı yöntemleri uzantı özniteliğiyle işaretlenmelidir `<Extension()>`, gelen <xref:System.Runtime.CompilerServices?displayProperty=nameWithType> ad alanı. İsteğe bağlı olarak, bir uzantı yöntemini içeren modül aynı şekilde işaretlenmiş olabilir. Herhangi bir kullanıma uzantısı özniteliği geçerli değil.  
  
 **Hata Kimliği:** BC36550  
  
## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Uzantı özniteliğine kaldırın.  
  
- Uzantınızı kapsayan bir modülde tanımlanmış bir yöntem olarak yeniden tasarlayın.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte tanımlayan bir `Print` yöntemi `String` veri türü.  
  
```  
Imports StringUtility  
Imports System.Runtime.CompilerServices  
Namespace StringUtility  
    <Extension()>   
    Module StringExtensions  
        <Extension()>   
        Public Sub Print (ByVal str As String)  
            Console.WriteLine(str)  
        End Sub  
    End Module  
End Namespace  
```  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Öznitelikler genel bakış](../../../visual-basic/programming-guide/concepts/attributes/index.md)
- [Genişletme Yöntemleri](../../../visual-basic/programming-guide/language-features/procedures/extension-methods.md)
- [Module Deyimi](../../../visual-basic/language-reference/statements/module-statement.md)
