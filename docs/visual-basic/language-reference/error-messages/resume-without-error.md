---
title: Hatasız devam et
ms.date: 07/20/2015
f1_keywords:
- vbrID20
ms.assetid: f9631804-fd36-4443-b36c-30db827e6176
ms.openlocfilehash: 61332486b20af66af24eac06b222a38353578c16
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62055166"
---
# <a name="resume-without-error"></a>Hatasız devam et
A `Resume` deyimi görünen hata işleme kodu dışında ya da kodu herhangi bir hata oluştu rağmen bir hata işleyicisine Atlanan.  
  
## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
1. Taşıma `Resume` bir hata işleyicisi INTO deyimi veya silin.  
  
2. Etiketlere atlama yordamları arasında oluşamaz yordamı hata işleyicisi tanımlayan etiket için arama. Hedefi olarak belirtilen bir yinelenen etiket bulursanız bir `GoTo` olmayan deyimi bir `On Error GoTo` deyimi, hedeflenen hedefine ile uyuşacak şekilde satır etiketi değiştirin.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Resume Deyimi](../../../visual-basic/language-reference/statements/resume-statement.md)
- [On Error Deyimi](../../../visual-basic/language-reference/statements/on-error-statement.md)
