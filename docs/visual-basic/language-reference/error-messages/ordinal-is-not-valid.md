---
title: Sıra sayısı geçerli değil
ms.date: 07/20/2015
f1_keywords:
- vbrID452
ms.assetid: 7459562b-cd4f-4590-95e0-6126ae3589a5
ms.openlocfilehash: 740243c744a7ba5391659894812a00d80555fd80
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64665659"
---
# <a name="ordinal-is-not-valid"></a>Sıra sayısı geçerli değil
Çağrınız bir dinamik bağlantı kitaplığı (DLL) belirtilen bir sayıyı bir yordam adı yerine kullanılacak kullanarak `#num` söz dizimi. Bu hata, aşağıdaki olası nedenleri vardır:  
  
- Dönüştürülecek girişiminde `#num` başarısız bir sıra ifadesi.  
  
- `#num` Belirtilen herhangi bir işlev DLL'de belirtmiyor.  
  
- Bir tür kitaplığı içinde geçersiz bir sıra numarası, iç kullanımından kaynaklanan geçersiz bir bildirim var.  
  
## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
1. İfade geçerli bir sayı temsil ettiğinden emin olun veya yordam adına göre arama.  
  
2. Emin `#num` DLL içinde geçerli bir işlevi tanımlar.  
  
3. Kodu açıklama olarak ekleyerek soruna yordam çağrısı yalıtın. Yazma bir `Declare` yordam ve rapor türü kitaplığı satıcıya sorun için bildirimi.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Declare Deyimi](../../../visual-basic/language-reference/statements/declare-statement.md)
