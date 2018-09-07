---
title: Belge Açıklamaları için Önerilen XML Etiketleri (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlDocComment
helpviewer_keywords:
- tags, XML
- XML comments, recommended tags [Visual Basic]
- comments, recommended XML tags
ms.assetid: 294e0736-ff1e-498e-af83-6db71ed41a72
ms.openlocfilehash: 3b2dec4224006d35fb9add11e170b9dcbeeafcf3
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43881288"
---
# <a name="recommended-xml-tags-for-documentation-comments-visual-basic"></a><span data-ttu-id="26950-102">Belge Açıklamaları için Önerilen XML Etiketleri (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="26950-102">Recommended XML Tags for Documentation Comments (Visual Basic)</span></span>
<span data-ttu-id="26950-103">Visual Basic Derleyicisi, bir XML dosyasına kod belge açıklamaları işleyebilir.</span><span class="sxs-lookup"><span data-stu-id="26950-103">The Visual Basic compiler can process documentation comments in your code to an XML file.</span></span> <span data-ttu-id="26950-104">Belgeleme XML dosyasını işlemek için ek araçları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26950-104">You can use additional tools to process the XML file into documentation.</span></span>  
  
 <span data-ttu-id="26950-105">XML açıklamaları kod yapıları türleri gibi izin verilen ve tür üyelerini.</span><span class="sxs-lookup"><span data-stu-id="26950-105">XML comments are allowed on code constructs such as types and type members.</span></span> <span data-ttu-id="26950-106">Üyeleri yorum hiçbir sınırlama olsa kısmi türleri için XML açıklamaları, türü yalnızca bir parçası olabilir.</span><span class="sxs-lookup"><span data-stu-id="26950-106">For partial types, only one part of the type can have XML comments, although there is no restriction on commenting its members.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="26950-107">Belge açıklamaları ad alanları için uygulanamaz.</span><span class="sxs-lookup"><span data-stu-id="26950-107">Documentation comments cannot be applied to namespaces.</span></span> <span data-ttu-id="26950-108">Nedeni, bir ad alanı, çeşitli derlemeler yayılabilir ve tüm derlemeleri, aynı anda yüklü olmak zorunda olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="26950-108">The reason is that one namespace can span several assemblies, and not all assemblies have to be loaded at the same time.</span></span>  
  
 <span data-ttu-id="26950-109">Derleyici, geçerli bir XML değil herhangi bir etiket işler.</span><span class="sxs-lookup"><span data-stu-id="26950-109">The compiler processes any tag that is valid XML.</span></span> <span data-ttu-id="26950-110">Aşağıdaki kullanıcı belgeleri, yaygın olarak kullanılan işlevler sunar.</span><span class="sxs-lookup"><span data-stu-id="26950-110">The following tags provide commonly used functionality in user documentation.</span></span>  
  
||||  
|---|---|---|  
|[<span data-ttu-id="26950-111">\<c ></span><span class="sxs-lookup"><span data-stu-id="26950-111">\<c></span></span>](../../../visual-basic/language-reference/xmldoc/c.md)|[<span data-ttu-id="26950-112">\<kod ></span><span class="sxs-lookup"><span data-stu-id="26950-112">\<code></span></span>](../../../visual-basic/language-reference/xmldoc/code.md)|[<span data-ttu-id="26950-113">\<Örnek ></span><span class="sxs-lookup"><span data-stu-id="26950-113">\<example></span></span>](../../../visual-basic/language-reference/xmldoc/example.md)|  
|<span data-ttu-id="26950-114">[\<Özel Durum >](../../../visual-basic/language-reference/xmldoc/exception.md) <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="26950-114">[\<exception>](../../../visual-basic/language-reference/xmldoc/exception.md) <sup>1</sup></span></span>|<span data-ttu-id="26950-115">[\<Ekle >](../../../visual-basic/language-reference/xmldoc/include.md) <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="26950-115">[\<include>](../../../visual-basic/language-reference/xmldoc/include.md) <sup>1</sup></span></span>|[<span data-ttu-id="26950-116">\<listesi ></span><span class="sxs-lookup"><span data-stu-id="26950-116">\<list></span></span>](../../../visual-basic/language-reference/xmldoc/list.md)|  
|[<span data-ttu-id="26950-117">\<para ></span><span class="sxs-lookup"><span data-stu-id="26950-117">\<para></span></span>](../../../visual-basic/language-reference/xmldoc/para.md)|<span data-ttu-id="26950-118">[\<param >](../../../visual-basic/language-reference/xmldoc/param.md) <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="26950-118">[\<param>](../../../visual-basic/language-reference/xmldoc/param.md) <sup>1</sup></span></span>|[<span data-ttu-id="26950-119">\<paramref ></span><span class="sxs-lookup"><span data-stu-id="26950-119">\<paramref></span></span>](../../../visual-basic/language-reference/xmldoc/paramref.md)|  
|<span data-ttu-id="26950-120">[\<izni >](../../../visual-basic/language-reference/xmldoc/permission.md) <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="26950-120">[\<permission>](../../../visual-basic/language-reference/xmldoc/permission.md) <sup>1</sup></span></span>|[<span data-ttu-id="26950-121">\<REMARKS ></span><span class="sxs-lookup"><span data-stu-id="26950-121">\<remarks></span></span>](../../../visual-basic/language-reference/xmldoc/remarks.md)|[<span data-ttu-id="26950-122">\<döndürür ></span><span class="sxs-lookup"><span data-stu-id="26950-122">\<returns></span></span>](../../../visual-basic/language-reference/xmldoc/returns.md)|  
|<span data-ttu-id="26950-123">[\<bkz: >](../../../visual-basic/language-reference/xmldoc/see.md) <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="26950-123">[\<see>](../../../visual-basic/language-reference/xmldoc/see.md) <sup>1</sup></span></span>|<span data-ttu-id="26950-124">[\<SeeAlso >](../../../visual-basic/language-reference/xmldoc/seealso.md) <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="26950-124">[\<seealso>](../../../visual-basic/language-reference/xmldoc/seealso.md) <sup>1</sup></span></span>|[<span data-ttu-id="26950-125">\<Summary ></span><span class="sxs-lookup"><span data-stu-id="26950-125">\<summary></span></span>](../../../visual-basic/language-reference/xmldoc/summary.md)|  
|<span data-ttu-id="26950-126">[\<typeparam >](../../../visual-basic/language-reference/xmldoc/typeparam.md) <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="26950-126">[\<typeparam>](../../../visual-basic/language-reference/xmldoc/typeparam.md) <sup>1</sup></span></span>|[<span data-ttu-id="26950-127">\<Değer ></span><span class="sxs-lookup"><span data-stu-id="26950-127">\<value></span></span>](../../../visual-basic/language-reference/xmldoc/value.md)||  
  
 <span data-ttu-id="26950-128">(<sup>1</sup> derleyici sözdizimini doğrular.)</span><span class="sxs-lookup"><span data-stu-id="26950-128">(<sup>1</sup> The compiler verifies syntax.)</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="26950-129">Açılı belgeleri açıklama metninde görünmesini istiyorsanız kullanın `&lt;` ve `&gt;`.</span><span class="sxs-lookup"><span data-stu-id="26950-129">If you want angle brackets to appear in the text of a documentation comment, use `&lt;` and `&gt;`.</span></span> <span data-ttu-id="26950-130">Örneğin, dize `"&lt;text in angle brackets&gt;"` olarak görünür `<text in angle brackets>`.</span><span class="sxs-lookup"><span data-stu-id="26950-130">For example, the string `"&lt;text in angle brackets&gt;"` will appear as `<text in angle brackets>`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26950-131">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="26950-131">See Also</span></span>  
 [<span data-ttu-id="26950-132">XML ile Kodunuzu Belgeleme</span><span class="sxs-lookup"><span data-stu-id="26950-132">Documenting Your Code with XML</span></span>](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md)  
 [<span data-ttu-id="26950-133">/doc</span><span class="sxs-lookup"><span data-stu-id="26950-133">/doc</span></span>](../../../visual-basic/reference/command-line-compiler/doc.md)  
 [<span data-ttu-id="26950-134">Nasıl yapılır: XML Belgesi Oluşturma</span><span class="sxs-lookup"><span data-stu-id="26950-134">How to: Create XML Documentation</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-create-xml-documentation.md)