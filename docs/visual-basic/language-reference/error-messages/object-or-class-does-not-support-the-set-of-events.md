---
title: Nesne veya sınıf olay kümesini desteklemiyor
ms.date: 07/20/2015
f1_keywords:
- vbrID459
ms.assetid: 785df3f3-2aae-4a25-af36-1f9879d4e5fd
ms.openlocfilehash: ad9176b5332a75f03968e742501c3fce541055de
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61925768"
---
# <a name="object-or-class-does-not-support-the-set-of-events"></a>Nesne veya sınıf olay kümesini desteklemiyor
Kullanmaya çalıştığınız bir `WithEvents` değişken bir bileşeniyle belirlenen olayları için olay kaynağı olarak çalışamaz. Örneğin, bir nesnenin olaylar indirilir ve ardından başka bir nesne oluşturan istediğinizi `Implements` ilk nesne. Uygulanan nesneden olayları havuz düşünebilirsiniz ancak bu her zaman böyle değildir. `Implements` yalnızca yöntemler ve özellikler için bir arabirim uygular. `WithEvents` Özel için desteklenmeyen `UserControls`tür bilgisini yükseltmek gerekli olduğundan `ObjectEvent` çalışma zamanında kullanılabilir değil.  
  
## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
1. Olayları olay kaynağı olmayan bir bileşen için havuz olamaz.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [WithEvents](../../../visual-basic/language-reference/modifiers/withevents.md)
- [Implements Deyimi](../../../visual-basic/language-reference/statements/implements-statement.md)
