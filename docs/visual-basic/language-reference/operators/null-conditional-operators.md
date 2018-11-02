---
title: Null koşullu işleçleri (Visual Basic)
ms.date: 10/19/2018
helpviewer_keywords:
- null-conditional operators [Visual Basic]
- ?. operator [Visual Basic]
- ?[] operator [C#]
- ?[] operator [Visual Basic]
ms.openlocfilehash: c29362a1e335e18b66821919e266b1ce57774692
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50195981"
---
# <a name="-and--null-conditional-operators-visual-basic"></a><span data-ttu-id="7e3cc-102">?.</span><span class="sxs-lookup"><span data-stu-id="7e3cc-102">?.</span></span> <span data-ttu-id="7e3cc-103">ve? () null koşullu işleçleri (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7e3cc-103">and ?() null-conditional operators (Visual Basic)</span></span>

<span data-ttu-id="7e3cc-104">Sol işlenen null değerini test eder (`Nothing`) üye erişimi gerçekleştirmeden önce (`?.`) ya da dizin (`?()`) döndürür; işlem `Nothing` sol işlenen değerlendirilirse `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="7e3cc-104">Tests the value of the left-hand operand for null (`Nothing`) before performing a member access (`?.`) or index (`?()`) operation; returns `Nothing` if the left-hand operand evaluates to `Nothing`.</span></span> <span data-ttu-id="7e3cc-105">Değer türleri normalde döndürecekti ifadelerinde null koşullu işleci döndürdüğünü unutmayın bir <xref:System.Nullable%601>.</span><span class="sxs-lookup"><span data-stu-id="7e3cc-105">Note that, in the expressions that would ordinarily return value types, the null-conditional operator returns a <xref:System.Nullable%601>.</span></span>

<span data-ttu-id="7e3cc-106">Bu işleçler null denetimleri, özellikle veri yapılarda azalan zaman işlemek için daha az kod yazmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="7e3cc-106">These operators help you write less code to handle null checks, especially when descending into data structures.</span></span> <span data-ttu-id="7e3cc-107">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="7e3cc-107">For example:</span></span>

```vb
Dim length As Integer? = customers?.Length  ' Nothing if customers is Nothing  
Dim first As Customer = customers?(0)  ' Nothing if customers is Nothing  
Dim count As Integer? = customers?(0)?.Orders?.Count()  ' Nothing if customers, the first customer, or Orders is Nothing  
```

<span data-ttu-id="7e3cc-108">Karşılaştırma için ilk kez bir null koşullu işleci olmadan bu ifadelerin alternatif koddur:</span><span class="sxs-lookup"><span data-stu-id="7e3cc-108">For comparison, the alternative code for the first of these expressions without a null-conditional operator is:</span></span>

```vb
Dim length As Integer
If customers IsNot Nothing Then
   length = customers.Length
End If
```

<span data-ttu-id="7e3cc-109">Null koşullu işleçleri short-circuiting.</span><span class="sxs-lookup"><span data-stu-id="7e3cc-109">The null-conditional operators are short-circuiting.</span></span>  <span data-ttu-id="7e3cc-110">Koşullu üye erişimi ve dizin işlemlerini zincirinin tek bir işlemde bir şey döndürürse, rest zincirinin yürütme durdurur.</span><span class="sxs-lookup"><span data-stu-id="7e3cc-110">If one operation in a chain of conditional member access and index operations returns Nothing, the rest of the chain’s execution stops.</span></span>  <span data-ttu-id="7e3cc-111">Aşağıdaki örnekte, C(E) değilse değerlendirilmez `A`, `B`, veya `C` Nothing olarak değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="7e3cc-111">In the following example, C(E) isn't evaluated if `A`, `B`, or `C` evaluates to Nothing.</span></span>

```vb
A?.B?.C?(E);
```

<span data-ttu-id="7e3cc-112">Başka bir null koşullu üye erişimi için temsilciler çok daha az kod ile iş parçacığı güvenli bir şekilde çağırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7e3cc-112">Another use for null-conditional member access is to invoke delegates in a thread-safe way with much less code.</span></span>  <span data-ttu-id="7e3cc-113">Kod aşağıdaki gibi eski yöntem gerektirir:</span><span class="sxs-lookup"><span data-stu-id="7e3cc-113">The old way requires code like the following:</span></span>  

```vb  
Dim handler = AddressOf(Me.PropertyChanged)  
If handler IsNot Nothing  
    Call handler(…)  
```

<span data-ttu-id="7e3cc-114">Yeni yolu çok daha kolaydır:</span><span class="sxs-lookup"><span data-stu-id="7e3cc-114">The new way is much simpler:</span></span>  

```vb
PropertyChanged?.Invoke(…)
```

<span data-ttu-id="7e3cc-115">Derleyici değerlendirmek için kod oluşturur çünkü iş parçacığı açısından güvenli yeni yoludur `PropertyChanged` sonucu geçici bir değişkende tutma yalnızca bir kez.</span><span class="sxs-lookup"><span data-stu-id="7e3cc-115">The new way is thread-safe because the compiler generates code to evaluate `PropertyChanged` one time only, keeping the result in a temporary variable.</span></span> <span data-ttu-id="7e3cc-116">Açıkça çağırmak ihtiyacınız `Invoke` yöntemi hiçbir null koşullu temsilci çağırma söz dizimi olduğundan `PropertyChanged?(e)`.</span><span class="sxs-lookup"><span data-stu-id="7e3cc-116">You need to explicitly call the `Invoke` method because there is no null-conditional delegate invocation syntax `PropertyChanged?(e)`.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7e3cc-117">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="7e3cc-117">See also</span></span>

- [<span data-ttu-id="7e3cc-118">İşleçler (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7e3cc-118">Operators (Visual Basic)</span></span>](index.md)
- [<span data-ttu-id="7e3cc-119">Visual Basic programlama kılavuzu</span><span class="sxs-lookup"><span data-stu-id="7e3cc-119">Visual Basic Programming Guide</span></span>](../../../visual-basic/programming-guide/index.md)
- [<span data-ttu-id="7e3cc-120">Visual Basic Dili Başvurusu</span><span class="sxs-lookup"><span data-stu-id="7e3cc-120">Visual Basic Language Reference</span></span>](../../../visual-basic/language-reference/index.md)  