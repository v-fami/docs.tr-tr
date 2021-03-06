---
title: -başvuru (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- /reference compiler option [Visual Basic]
- r compiler option [Visual Basic]
- -reference compiler option [Visual Basic]
- /r compiler option [Visual Basic]
- reference compiler option [Visual Basic]
- -r compiler option [Visual Basic]
ms.assetid: 66bdfced-bbf6-43d1-a554-bc0990315737
ms.openlocfilehash: 2394a23ddd59d09ce53c78fc4486fc5bae9e8516
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65583366"
---
# <a name="-reference-visual-basic"></a>-başvuru (Visual Basic)
Derleyicinin tür bilgilerini belirli derlemelerde şu anda derleme proje kullanılabilir hale getirmek neden olur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
-reference:fileList  
' -or-  
-r:fileList  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terim|Tanım|  
|---|---|  
|`fileList`|Gerekli. Derleme dosya adlarının virgülle ayrılmış liste. Dosya adı boşluk içeriyorsa adı tırnak içine alın.|  
  
## <a name="remarks"></a>Açıklamalar  
 İçeri aktardığınız dosya, derleme meta verileri içermelidir. Yalnızca genel türleri derlemenin dışında görünür. [/Addmodule](../../../visual-basic/reference/command-line-compiler/addmodule.md) seçenek, bir modülden meta verileri alır.  
  
 Bir bütünleştirilmiş kodu (bütünleştirilmiş kod: A) başvuruda bulunursanız kendisi başvuran bir derlemeyle (derlemeyi B), başvuru derlemesi B, gerekir:  
  
- Bir derlemeden bir tür bir tür tarafından devralındığında veya derleme B'deki bir arabirim uygular.  
  
- Bir alan, özelliği, olay veya dönüş türü veya parametresi türü derleme b olan yöntemi çağrılır.  
  
 Kullanım [- LIBPATH](../../../visual-basic/reference/command-line-compiler/libpath.md) için bir veya daha fazla, derleme başvuruları bulunduğu dizini belirtin.  
  
 Derleyicinin derlemede (modül değil) bir türü tanıması, türü çözümlemeye zorlanması gerekir. Bunu yapmak nasıl ilişkin bir örnek, bir türün örneğini tanımlamaktır. Yollar, derleyici bir derlemede bulunan tür adlarını çözmek kullanılabilir. Örneğin, bir derleme içinde bulunan bir türden devralıyorsanız, tür adı ardından derleyiciye bildiği.  
  
 Yaygın olarak kullanılan .NET Framework derlemelerine başvuran, nezahrnovat yanıt dosyası varsayılan olarak kullanılır. Kullanma `-noconfig` derleyici nezahrnovat kullanmak istemiyorsanız.  
  
 Kısa formunu da `-reference` olduğu `/r`.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki komut, kaynak dosyası derler `Input.vb` ve başvuru derlemeleri `Metad1.dll` ve `Metad2.dll` üretmek için `Out.exe`.  
  
```console
vbc -reference:metad1.dll,metad2.dll -out:out.exe input.vb  
```  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Visual Basic komut satırı derleyicisi](../../../visual-basic/reference/command-line-compiler/index.md)
- [-noconfig](../../../visual-basic/reference/command-line-compiler/noconfig.md)
- [-target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md)
- [Public](../../../visual-basic/language-reference/modifiers/public.md)
- [Örnek Derleme Komut Satırları](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
