---
title: 'Nasıl yapılır: Namespace değiştirmek için tüm XML ağacının (C#)'
ms.date: 07/20/2015
ms.assetid: 1584ff3b-c77d-4241-ab62-80adfb7bfc1b
ms.openlocfilehash: 020d072cfb58c90720317734199d241c6892511f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61668191"
---
# <a name="how-to-change-the-namespace-for-an-entire-xml-tree-c"></a>Nasıl yapılır: Namespace değiştirmek için tüm XML ağacının (C#)
Bazen, program aracılığıyla bir öğe veya öznitelik için ad alanı değiştirmek zorunda. LINQ to XML bu kolaylaştırır. <xref:System.Xml.Linq.XElement.Name%2A?displayProperty=nameWithType> Özelliğini ayarlayabilirsiniz. <xref:System.Xml.Linq.XAttribute.Name%2A?displayProperty=nameWithType> Özelliği ayarlanamaz, ancak öznitelikler kolayca kopyalayabilirsiniz bir <xref:System.Collections.Generic.List%601?displayProperty=nameWithType>mevcut öznitelikleri kaldırın ve ardından yeni istenen ad alanı olan yeni özellikler ekleyin.  
  
 Daha fazla bilgi için [(C#) XML ad alanları ile çalışma](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod, iki XML ağaçlarını hiçbir ad alanında oluşturur. Ardından her ağaçları ad alanı değiştirir ve bunları tek bir ağacına birleştirir.  
  
```csharp  
XElement tree1 = new XElement("Data",  
    new XElement("Child", "content",  
        new XAttribute("MyAttr", "content")  
    )  
);  
XElement tree2 = new XElement("Data",  
    new XElement("Child", "content",  
        new XAttribute("MyAttr", "content")  
    )  
);  
XNamespace aw = "http://www.adventure-works.com";  
XNamespace ad = "http://www.adatum.com";  
// change the namespace of every element and attribute in the first tree  
foreach (XElement el in tree1.DescendantsAndSelf())  
{  
    el.Name = aw.GetName(el.Name.LocalName);  
    List<XAttribute> atList = el.Attributes().ToList();  
    el.Attributes().Remove();  
    foreach (XAttribute at in atList)  
        el.Add(new XAttribute(aw.GetName(at.Name.LocalName), at.Value));  
}  
// change the namespace of every element and attribute in the second tree  
foreach (XElement el in tree2.DescendantsAndSelf())  
{  
    el.Name = ad.GetName(el.Name.LocalName);  
    List<XAttribute> atList = el.Attributes().ToList();  
    el.Attributes().Remove();  
    foreach (XAttribute at in atList)  
        el.Add(new XAttribute(ad.GetName(at.Name.LocalName), at.Value));  
}  
// add attribute namespaces so that the tree will be serialized with  
// the aw and ad namespace prefixes  
tree1.Add(  
    new XAttribute(XNamespace.Xmlns + "aw", "http://www.adventure-works.com")  
);  
tree2.Add(  
    new XAttribute(XNamespace.Xmlns + "ad", "http://www.adatum.com")  
);  
// create a new composite tree  
XElement root = new XElement("Root",  
    tree1,  
    tree2  
);  
Console.WriteLine(root);  
```  
  
 Bu örnek aşağıdaki çıktıyı üretir:  
  
```xml  
<Root>  
  <aw:Data xmlns:aw="http://www.adventure-works.com">  
    <aw:Child aw:MyAttr="content">content</aw:Child>  
  </aw:Data>  
  <ad:Data xmlns:ad="http://www.adatum.com">  
    <ad:Child ad:MyAttr="content">content</ad:Child>  
  </ad:Data>  
</Root>  
```  
  
## <a name="see-also"></a>Ayrıca bkz.

- [(LINQ to XML) XML ağaçlarını değiştirme (C#)](../../../../csharp/programming-guide/concepts/linq/modifying-xml-trees-linq-to-xml.md)
