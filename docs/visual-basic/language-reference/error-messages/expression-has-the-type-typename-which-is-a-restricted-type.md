---
title: İfade kısıtlanmış bir tür olan '<typename>' türüne sahip ve 'Object' veya 'ValueType' öğesinden devralınan üyelere erişim için kullanılamaz
ms.date: 07/20/2015
f1_keywords:
- bc31393
- vbc31393
helpviewer_keywords:
- BC31393
ms.assetid: 2963cf3f-c527-4aa7-b67c-ee80b6d23186
ms.openlocfilehash: 017a2458562068727674bd3fd9cda8c33d989e8b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61803174"
---
# <a name="expression-has-the-type-typename-which-is-a-restricted-type-and-cannot-be-used-to-access-members-inherited-from-object-or-valuetype"></a>İfade türüne sahip '\<typename >' kısıtlanmış bir tür olan ve 'Object' veya 'ValueType' öğesinden devralınan üyelere erişim için kullanılamaz
Bir ifade, ortak dil çalışma zamanı tarafından (CLR) Kutulu bir türe değerlendirir ancak kutulama gerektiren bir üye erişir.  
  
 *Kutulama* bir türe dönüştürmek için gereken işleme anlamına gelir `Object` veya bazı durumlarda için <xref:System.ValueType>. Ortak dil çalışma zamanı belirli yapı türleri, örneğin kutusunda olamaz <xref:System.ArgIterator>, <xref:System.RuntimeArgumentHandle>, ve <xref:System.TypedReference>.  
  
 Bu ifade, devralınan bir yöntemi çağırmak için kısıtlanmış türdeki kullanmayı dener <xref:System.Object> veya <xref:System.ValueType>, gibi <xref:System.Object.GetHashCode%2A> veya <xref:System.Object.ToString%2A>. Bu yönteme erişmek için Visual Basic bu hataya neden bir örtük Kutulama dönüştürmesi çalıştı.  
  
 **Hata Kimliği:** BC31393  
  
## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
1. İçin alıntı türü değerlendirilen bir ifade bulun.  
  
2. Devralınan bir yöntemi çağırmak için çalışır Ekstrenizi bölümü bulun <xref:System.Object> veya <xref:System.ValueType>.  
  
3. Yöntem çağrısının önlemek için deyimi yeniden yazın.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Örtük ve Açık Dönüştürmeler](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
