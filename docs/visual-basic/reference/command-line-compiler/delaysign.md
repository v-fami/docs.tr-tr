---
title: -delaysign
ms.date: 03/10/2018
helpviewer_keywords:
- delaysign compiler option [Visual Basic]
- -delaysign compiler option [Visual Basic]
- -delaysign compiler option [Visual Basic]
ms.assetid: c76e61a4-1884-4252-9fb2-377f99caa690
ms.openlocfilehash: 770dcad385c522a548a0c6fd3b6ef02dfbac82f5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61649718"
---
# <a name="-delaysign"></a>-delaysign
Derlemenin tamamen veya kısmen imzalanacağını belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
-delaysign[+ | -]  
```  
  
## <a name="arguments"></a>Arguments  
 `+` &#124; `-`  
 İsteğe bağlı. Kullanım `-delaysign-` tam imzalı bir derleme istiyorsanız. Kullanım `-delaysign+` , derleme ve ayrılan alana imzalı karma için ortak anahtar yerleştirmek istiyorsanız. Varsayılan, `-delaysign-` değeridir.  
  
## <a name="remarks"></a>Açıklamalar  
 `-delaysign` Seçeneği ile birlikte kullanılmadığı sürece hiçbir etkiye sahiptir [- keyfile](../../../visual-basic/reference/command-line-compiler/keyfile.md) veya [- keycontaıner](../../../visual-basic/reference/command-line-compiler/keycontainer.md).  
  
 Tam imzalı bir derleme istediğinizde; derleyici bildirimi (derleme meta verileri) içeren ve karmayı özel anahtarla imzalar dosyayı karma hale getirir. Elde edilen dijital imza, bildirimi içeren dosyada depolanır. Bir derlemeyi gecikmeli imzalanmış olduğunda, derleyici işlem değildir ve daha sonra imzanın eklenmesi için dosyada imza ancak yedekleri alanı depolamak.  
  
 Kullanarak örneğin, `-delaysign+`, bir kuruluşta bir geliştirici, test ediciler genel derleme önbelleği ile kaydedebilir veya kullanmak bir derleme sürümlerini imzasız test dağıtabilirsiniz. Derleme üzerinde iş tamamlandığında, kuruluşun özel anahtarı için sorumlu kişi derleme tam olarak imzalayabilirsiniz. Bu compartmentalization, kuruluşunuzun özel anahtarı derlemelerini çalışması tüm geliştiricilerin verirken ifşaatına karşı korur.  
  
 Bkz: [bkz](../../../framework/app-domains/create-and-use-strong-named-assemblies.md) derleme imzalama hakkında daha fazla bilgi.  
  
### <a name="to-set--delaysign-in-the-visual-studio-integrated-development-environment"></a>-Delaysıgn Visual Studio tümleşik geliştirme ortamında ayarlamak için  
  
1. Seçili bir projeyi **Çözüm Gezgini**. Üzerinde **proje** menüsünü tıklatın **özellikleri**.   
  
2. Tıklayın **imzalama** sekmesi.  
  
3. Değer kümesindeki **gecikme yalnızca oturum** kutusu.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Visual Basic komut satırı derleyicisi](../../../visual-basic/reference/command-line-compiler/index.md)
- [-keyfile](../../../visual-basic/reference/command-line-compiler/keyfile.md)
- [-keycontainer](../../../visual-basic/reference/command-line-compiler/keycontainer.md)
- [Örnek Derleme Komut Satırları](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
