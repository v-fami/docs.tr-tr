---
title: "'<interfacename>. <membername>' taban sınıfı tarafından zaten uygulanmış '<baseclassname>'. Yeniden uygulanmasına <type> varsayıldı"
ms.date: 07/20/2015
f1_keywords:
- vbc42015
- bc42015
helpviewer_keywords:
- BC42015
ms.assetid: 658c070a-113e-4bd8-b294-12c243191160
ms.openlocfilehash: 5943eff5fa7e68da9905e3e589eea264c06943c1
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64593313"
---
# <a name="interfacenamemembername-is-already-implemented-by-the-base-class-baseclassname-re-implementation-of-type-assumed"></a>'\<InterfaceName >. \<membername >' taban sınıfının tarafından zaten uygulanmış\<baseclassname >'. Yeniden uygulanmasına \<türü > varsayıldı
Bir özellik, yordam veya türetilmiş bir sınıf içinde olay kullanan bir `Implements` temel sınıfta zaten uygulanmış bir arabirim üyesi belirleme yan tümcesi.  
  
 Türetilmiş bir sınıf, taban sınıfı tarafından uygulanan bir arabirim üyesi yeniden uygulayın. Bu temel sınıf uygulamasına geçersiz kılma ile aynı değildir. Daha fazla bilgi için [uygular](../../../visual-basic/language-reference/statements/implements-clause.md).  
  
 Varsayılan olarak, bu iletiyi bir uyarıdır. Uyarıları gizleme veya uyarıları hata olarak değerlendirmesini hakkında daha fazla bilgi için bkz: [Visual Basic'teki uyarıları yapılandırma](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **Hata Kimliği:** BC42015  
  
## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Arabirim üyesini yeniden uygulayın yapmak istiyorsanız, herhangi bir eylemde bulunmanız gerekmez. Türetilmiş sınıfınızın kodda erişen reimplemented üye kullanılmadıkça `MyBase` temel sınıf uygulamasına erişmek için anahtar sözcüğü.  
  
- Arabirim üyesini yeniden uygulayın düşünmüyorsanız kaldırmak `Implements` özellik, yordam veya olay bildiriminin from yan tümcesi.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Arabirimler](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
