---
title: Bu 'Sub New' öğesinin ilk deyimi 'MyBase.New' veya 'MyClass.New' için bir çağrı olmalıdır (Parametreler Olmadan Erişilebilir Yapıcı Yok)
ms.date: 07/20/2015
f1_keywords:
- bc30148
- vbc30148
helpviewer_keywords:
- BC30148
ms.assetid: 4426e8fc-cb39-4eb8-ba95-503cd32fcc89
ms.openlocfilehash: 160e4d512a1533b3c89a1af50b47600ca6df51c2
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64592052"
---
# <a name="first-statement-of-this-sub-new-must-be-a-call-to-mybasenew-or-myclassnew-no-accessible-constructor-without-parameters"></a>Bu 'Sub New' öğesinin ilk deyimi 'MyBase.New' veya 'MyClass.New' için bir çağrı olmalıdır (Parametreler Olmadan Erişilebilir Yapıcı Yok)
Bu 'Sub New' öğesinin ilk deyimi 'MyBase.New' veya 'MyClass.New' çağrısı olmalıdır, çünkü temel sınıfı\<basename >', '\<derivedname >' bir erişilebilir 'Sub bağımsız değişken olmadan çağrılabilecek New' yok.  
  
 Türetilen bir sınıfta bir temel sınıf oluşturucusu her Oluşturucu çağırmanız gerekir (`MyBase.New`). Temel sınıfın türetilmiş sınıflar için erişilebilir olan parametresiz bir oluşturucu varsa `MyBase.New` otomatik olarak çağrılabilir. Aksi halde bir temel sınıf oluşturucusunu parametrelerle çağrılması gerekir ve bu otomatik olarak yapılamaz. Bu durumda, her türetilmiş sınıf oluşturucusunun ilk deyimi gerekir parametreli bir kurucu taban sınıfını çağırın veya bir temel sınıf oluşturucusunu çağırma kılan türetilmiş bir sınıf içindeki başka bir oluşturucusunu çağırın.  
  
 **Hata Kimliği:** BC30148  
  
## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Her iki çağrı `MyBase.New` gerekli parametreleri belirtin veya bu tür bir çağrıda bir eş oluşturucusunu çağırın.  
  
     Örneğin, temel sınıf olarak bildirilen bir oluşturucusu varsa `Public Sub New(ByVal index as Integer)`, ilk ifade türetilen sınıf oluşturucusu olabilir `MyBase.New(100)`.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Devralma Temelleri](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
