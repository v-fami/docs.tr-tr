---
title: "Nasıl yapılır: Bir nesne değişkeni bildirme ve Visual Basic'te bir nesne atama"
ms.date: 07/20/2015
helpviewer_keywords:
- object variables [Visual Basic], declaring
- declaring object variables [Visual Basic]
ms.assetid: 2fa77dde-1fb2-439a-80d4-3e9787649fad
ms.openlocfilehash: e172d62e5bfadded254d5a5fd25b1dcf2da9634d
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64663590"
---
# <a name="how-to-declare-an-object-variable-and-assign-an-object-to-it-in-visual-basic"></a>Nasıl yapılır: Bir nesne değişkeni bildirme ve Visual Basic'te bir nesne atama
Bir değişken bildirmek [nesne veri türü](../../../../visual-basic/language-reference/data-types/object-data-type.md) belirterek `As Object` içinde bir [Dim deyimi](../../../../visual-basic/language-reference/statements/dim-statement.md). Eşittir işaretinden sonra nesne koyarak bir nesne gibi bir değişkene atayın (`=`) bir atama ifadesi veya başlatma yan.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek bildirir bir `Object` değişkeni ve geçerli örnek için atar.  
  
```  
      Dim thisObject As Object  
thisObject = "This is an Object"  
```  
  
 Bildirim ve atamayı bildiriminin bir parçası bir değişkeni başlatarak birleştirebilirsiniz. Aşağıdaki örnek önceki örneğe eşdeğerdir.  
  
```  
Dim thisObject As Object= "This is an Object"  
```  
  
## <a name="compiling-the-code"></a>Kod Derleniyor  
 Bu örnek gerektirir:  
  
- Bir başvuru <xref:System> ad alanı.  
  
- Bir sınıf, yapı veya modül yerleştirileceği `Dim` deyimi.  
  
- Atama ifadesi yerleştirileceği bir yordam.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Değişken Bildirimi](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [Nesne Değişkenleri](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [Nesne Değişken Bildirimi](../../../../visual-basic/programming-guide/language-features/variables/object-variable-declaration.md)
- [Object Veri Türü](../../../../visual-basic/language-reference/data-types/object-data-type.md)
- [Dim Deyimi](../../../../visual-basic/language-reference/statements/dim-statement.md)
- [Yerel Çıkarım](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
- [Option Strict Deyimi](../../../../visual-basic/language-reference/statements/option-strict-statement.md)
