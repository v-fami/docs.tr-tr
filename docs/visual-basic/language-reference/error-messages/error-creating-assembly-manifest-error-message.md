---
title: 'Derleme bildirimi oluşturulurken hata oldu: <error message>'
ms.date: 07/20/2015
f1_keywords:
- bc30140
- vbc30140
helpviewer_keywords:
- BC30140
ms.assetid: 1beb5aa0-7b79-4c85-946b-5c2d0a41d1d2
ms.openlocfilehash: 0f67b772bab3104c00510954d01b200aadfa9e8a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61803356"
---
# <a name="error-creating-assembly-manifest-error-message"></a>Derleme bildirimi oluşturulurken hata oluştu: \<hata iletisi >
Visual Basic Derleyicisi bir bildirime sahip bir derleme oluşturmak için Assembly Linker (Al.exe Alink olarak da bilinir) çağırır. Bağlayıcı, derleme oluşturma öncesi Emisyonu aşamasında bir hata bildirdi.  
  
 Anahtar dosyası veya belirtilen anahtar kapsayıcısında ile ilgili sorun varsa bu durum oluşabilir. Bir derlemeyi tam imzalamak için ortak ve özel anahtarları hakkında bilgi içeren geçerli bir anahtar dosyası sağlamanız gerekir. Derlemeyi imzala geciktirmek için seçmelisiniz **gecikme yalnızca oturum** onay kutusunu işaretleyin ve ortak anahtar bilgilerini hakkında bilgi içeren geçerli bir anahtar dosyası belirtin. Bir derlemeyi gecikmeli imzalanmış olduğunda, özel anahtarı gerekli değildir. Daha fazla bilgi için [nasıl yapılır: Bir derlemeyi katı bir adla imzalamak](../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).  
  
 **Hata Kimliği:** BC30140  
  
## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
1. Tırnak işaretli hata iletisini inceleyin ve konusuna danışın [Al.exe](../../../framework/tools/al-exe-assembly-linker.md). ek açıklama hatası AL1019 ve öneriler  
  
2. Sorun devam ederse, koşullar hakkında bilgi toplamak ve Microsoft Ürün Destek Hizmetleri bilgilendirir.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Derlemeyi tanımlayıcı bir adla imzalama](../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md)
- [İmzalama Sayfası, Proje Tasarımcısı](/visualstudio/ide/reference/signing-page-project-designer)
- [Al.exe](../../../framework/tools/al-exe-assembly-linker.md)
- [Bizimle İletişime Geçin](/visualstudio/ide/talk-to-us)
