---
title: Mid deyimi (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.MidB
- vb.Mid
helpviewer_keywords:
- substrings [Visual Basic], Mid statement
- strings [Visual Basic], substrings
- Mid statement [Visual Basic]
- strings [Visual Basic], replacing
ms.assetid: 2b82d7a8-9646-4cb0-bec5-80abc98297bf
ms.openlocfilehash: df83fd527612af1a6a4b8131ffa2643ef0d1d7dd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61784245"
---
# <a name="mid-statement"></a>Mid Deyimi
Belirtilen sayıda karakter yerini alan bir `String` başka bir dizeden karakterlerle değişken.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
Mid( _  
   ByRef Target As String, _  
   ByVal Start As Integer, _  
   Optional ByVal Length As Integer _  
) = StringExpression  
```  
  
## <a name="parts"></a>Bölümler  
 `Target`  
 Gerekli. Adını `String` değiştirmek için değişken.  
  
 `Start`  
 Gerekli. `Integer` ifade. Karakter konumunda `Target` burada metin değiştirmesinin. `Start` bir tabanlı bir dizin kullanır.  
  
 `Length`  
 İsteğe bağlı. `Integer` ifade. Değiştirilecek karakterlerin sayısı. Atlanırsa, tüm `String` kullanılır.  
  
 `StringExpression`  
 Gerekli. `String` bölümünü değiştirir ifade `Target`.  
  
## <a name="exceptions"></a>Özel Durumlar  
  
|Özel durum türü|Koşul|  
|--------------------|---------------|  
|<xref:System.ArgumentException>|`Start` < = 0 veya `Length` < 0.|  
  
## <a name="remarks"></a>Açıklamalar  
 Değiştirilen karakter sayısını her zaman eşit veya karakter sayısı küçüktür `Target`.  
  
 Visual Basic sahip bir <xref:Microsoft.VisualBasic.Strings.Mid%2A> işlevi ve bir `Mid` deyimi. Bu öğelerden hem de çalışan bir belirtilen bir dizedeki karakter sayısına ancak `Mid` işlevi çalışırken karakterleri döndürür `Mid` deyimi karakterleri değiştirir. Daha fazla bilgi için bkz. <xref:Microsoft.VisualBasic.Strings.Mid%2A>.  
  
> [!NOTE]
>  `MidB` Visual Basic'in önceki sürümlerindeki deyiminin karakter yerine bayt bir alt dizeyi değiştirir. Esas olarak çift baytlı karakter kümesi (DBCS) uygulamalarında dize dönüştürmek için kullanılır. Tüm Visual Basic dizeleri Unicode biçimindedir ve `MidB` artık desteklenmiyor.  
  
## <a name="example"></a>Örnek  
 Bu örnekte `Mid` deyimi başka bir dizeden karakterlerle belirtilen sayıda karakteri bir dize değişkeniyle değiştirin.  
  
 [!code-vb[VbVbalrStrings#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class1.vb#5)]  
  
## <a name="requirements"></a>Gereksinimler  
 **Namespace:** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)  
  
 **Modül:** `Strings`  
  
 **Derleme:** [!INCLUDE[vbprvbruntime](~/includes/vbprvbruntime-md.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:Microsoft.VisualBasic.Strings.Mid%2A>
- [Dizeler](../../../visual-basic/programming-guide/language-features/strings/index.md)
- [Visual Basic'de dizelere giriş](../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)
