---
title: -moduleassemblyname (C# derleyici seçeneği)
ms.date: 07/20/2015
f1_keywords:
- /moduleassemblyname
helpviewer_keywords:
- moduleassemblyname compiler option [C#]
- /moduleassemblyname compiler option [C#]
- .moduleassemblyname compiler option [C#]
ms.assetid: d464d9b9-f18d-423b-95e9-66c7878fd53a
ms.openlocfilehash: 9e4768b598f6046ffb7a0ac014d8594eac40309f
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64593050"
---
# <a name="-moduleassemblyname-c-compiler-option"></a>-moduleassemblyname (C# derleyici seçeneği)
Genel olmayan türler .netmodule erişebilmeniz için bir derleme belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```console  
-moduleassemblyname:assembly_name  
```  
  
## <a name="arguments"></a>Arguments  
 `assembly_name`  
 .netmodule, genel olmayan türleri derlemenin adını erişebilirsiniz.  
  
## <a name="remarks"></a>Açıklamalar  
 **-moduleassemblyname** .netmodule oluştururken ve aşağıdaki koşullar doğru olduğunda kullanılmalıdır:  
  
- .netmodule var olan bir derlemede ortak olmayan türlere erişmesi gerekir.  
  
- Bildiğiniz .netmodule derlenecek olan derlemenin adı.  
  
- Mevcut bütünleştirilmiş kodu .netmodule derlenecek olan derlemeye arkadaş derleme erişim verildi.  
  
 .Netmodule derleme hakkında daha fazla bilgi için bkz. [-target: module (C# Derleyici Seçenekleri)](../../../csharp/language-reference/compiler-options/target-module-compiler-option.md).  
  
 Arkadaş bütünleştirilmiş kodları hakkında daha fazla bilgi için bkz. [arkadaş derlemeleri](../../../standard/assembly/friend-assemblies.md).  
  
 Bu seçenek geliştirme ortamı içinden erişilebilir değildir; Yalnızca komut satırından derleme yapılırken kullanılabilir.  
  
 Bu derleyici seçeneğini Visual Studio'da kullanılamıyor ve program aracılığıyla değiştirilemez.  
  
## <a name="example"></a>Örnek  
 Bu örnek bir özel tür sahip bir derleme oluşturur ve bu csman_an_assembly adlı bir derlemeye arkadaş derleme erişim sağlar.  
  
```csharp  
// moduleassemblyname_1.cs  
// compile with: -target:library  
using System;  
using System.Runtime.CompilerServices;  
  
[assembly:InternalsVisibleTo ("csman_an_assembly")]  
  
class An_Internal_Class   
{  
    public void Test()   
    {   
        Console.WriteLine("An_Internal_Class.Test called");   
    }  
}  
```  
  
## <a name="example"></a>Örnek  
 Bu örnek, bir derleme moduleassemblyname_1.dll genel olmayan türde erişen bir .netmodule oluşturur. Bu .netmodule csman_an_assembly adı verilen bir derlemeye oluşturulacak bilirseniz, biz belirtebilirsiniz **- moduleassemblyname**, .netmodule arkadaş derleme verilmiş bir derlemede ortak olmayan türlere erişmek izin verme için csman_an_assembly erişin.  
  
```csharp  
// moduleassemblyname_2.cs  
// compile with: -moduleassemblyname:csman_an_assembly -target:module -reference:moduleassemblyname_1.dll  
class B {  
    public void Test() {  
        An_Internal_Class x = new An_Internal_Class();  
        x.Test();  
    }  
}  
```  
  
## <a name="example"></a>Örnek  
 Bu kod örneği, .netmodule ve daha önce oluşturulan derlemeyi başvuran derlemenin csman_an_assembly oluşturur.  
  
```csharp  
// csman_an_assembly.cs  
// compile with: -addmodule:moduleassemblyname_2.netmodule -reference:moduleassemblyname_1.dll  
class A {  
    public static void Main() {  
        B bb = new B();  
        bb.Test();  
    }  
}  
```  
  
**An_Internal_Class.test**

## <a name="see-also"></a>Ayrıca bkz.

- [C# Derleyici Seçenekleri](../../../csharp/language-reference/compiler-options/index.md)
- [Proje ve Çözüm Özelliklerini Yönetme](/visualstudio/ide/managing-project-and-solution-properties)
