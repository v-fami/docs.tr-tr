---
title: LINQ to Entities Sorgu İfadeleri
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d70b502f-6a15-4120-b4fe-500b173ad9cc
ms.openlocfilehash: 234b3059f9109c23b8ecae4da37e15f7f094fbd1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62034196"
---
# <a name="expressions-in-linq-to-entities-queries"></a>LINQ to Entities Sorgu İfadeleri
Tek değer, nesne, yöntemi veya ad alanı için değerlendirilen kodun bir parçasını ifadesidir. Değişmez değer, bir yöntem çağrısı, bir işleci ve işlenenleri veya basit bir ad ifadeleri içerebilir. Basit adları bir değişken, tür üyesi, yöntem parametresi, ad alanı veya tür adı olabilir. İfadeler sırayla parametreleri veya diğer sırayla yöntem çağrılarını parametreleri olan yöntem çağrıları diğer ifadeler kullanan işleçlerini kullanabilirsiniz. Bu nedenle, ifadeleri basitten çok karmaşık değişebilir.  
  
 İçinde [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] sorgu ifadeleri içerebilir türler tarafından izin verilen herhangi bir şey <xref:System.Linq.Expressions> ad alanı, lambda ifadeleri de dahil olmak üzere. Kullanılabilir ifadeler [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] sorgulardır kullanılabilir ifadeler kümesi için sorgu [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)].  Sorguları parçası olan ifadeleri [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)] tarafından desteklenen operations sınırlıdır `ObjectQuery<T>` ve temel alınan veri kaynağı.  
  
 Aşağıdaki örnekte, Karşılaştırmada `Where` yan tümcesi ise bir ifade:  
  
 [!code-csharp[DP L2E Conceptual Examples#WhereExpression](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Conceptual Examples/CS/Program.cs#whereexpression)]
 [!code-vb[DP L2E Conceptual Examples#WhereExpression](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Conceptual Examples/VB/Module1.vb#whereexpression)]  
  
> [!NOTE]
>  Belirli dil yapılarını, C# gibi `unchecked`, hiçbir anlamı olmayan [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)].  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Sabit İfadeler](../../../../../../docs/framework/data/adonet/ef/language-reference/constant-expressions.md)  
  
 [Karşılaştırma İfadeleri](../../../../../../docs/framework/data/adonet/ef/language-reference/comparison-expressions.md)  
  
 [Null Karşılaştırmalar](../../../../../../docs/framework/data/adonet/ef/language-reference/null-comparisons.md)  
  
 [Başlatma İfadeleri](../../../../../../docs/framework/data/adonet/ef/language-reference/initialization-expressions.md)  
  
 [İlişkiler, gezinti özellikleri ve yabancı anahtarlar](/ef/ef6/fundamentals/relationships)  
  
## <a name="see-also"></a>Ayrıca bkz.

- [ADO.NET Entity Framework](../../../../../../docs/framework/data/adonet/ef/index.md)
