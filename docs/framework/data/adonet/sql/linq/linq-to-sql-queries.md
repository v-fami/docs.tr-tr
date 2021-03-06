---
title: LINQ to SQL Sorguları
ms.date: 03/30/2017
ms.assetid: f4897aaa-7f44-4c20-a471-b948c2971aae
ms.openlocfilehash: 6142a1c4713010a75ed8413b935678fce92e40be
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65583662"
---
# <a name="linq-to-sql-queries"></a>LINQ to SQL Sorguları
Tanımladığınız [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] yaptığınız gibi aynı sözdizimini kullanarak sorguları [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)]. Tek fark, sorgularınızdaki başvurulan nesneler öğeleri veritabanındaki eşlendiğine ' dir. Daha fazla bilgi için [(C#) LINQ sorgularına giriş](~/docs/csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md).  
  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] eşdeğer SQL sorguları yazma sorguları çevirir ve işlem sunucusuna gönderir. Özellikle, uygulamanızın kullandığı [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] API istek sorgu yürütme için. [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] Sağlayıcısı ardından sorgu SQL metne dönüştürür ve temsilciler ADO sağlayıcısına yürütme. ADO sağlayıcı olarak sorgu sonuçlarını döndürür bir `DataReader`. [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] Sağlayıcısı ADO sonuçları çeviren bir <xref:System.Linq.IQueryable> kullanıcı nesneleri koleksiyonu.  
  
> [!NOTE]
>  Birçok yöntem ve .NET Framework yerleşik türleri işleçlerini SQL için doğrudan Çeviriler var. Bu, [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)] çeviremez çalışma zamanı özel durumlarını oluşturur. Daha fazla bilgi için [SQL-CLR tür eşlemesi](../../../../../../docs/framework/data/adonet/sql/linq/sql-clr-type-mapping.md).  
  
 Aşağıdaki tabloda benzerlik gösterir ve arasındaki farklar [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)] ve [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] sorgu öğeleri.  
  
|Öğe|LINQ Query|[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] Sorgu|  
|----------|----------------|----------------------------------------------------------------------|  
|Sorgu (için dizileri döndüren sorgular) içeren yerel değişkenini dönüş türü|Genel `IEnumerable`|Genel `IQueryable`|  
|Veri kaynağını belirtme|Kullanan `From` (Visual Basic) veya `from` (C#) yan tümcesi|Aynı|  
|Filtreleme|Kullanan `Where` / `where` yan tümcesi|Aynı|  
|Gruplandırma|Kullanan `Group…By` / `groupby` yan tümcesi|Aynı|  
|(Yansıtma) seçme|Kullanan `Select` / `select` yan tümcesi|Aynı|  
|Ertelenmiş hemen yürütme|Bkz: [LINQ sorgularına giriş (C#)](~/docs/csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md)|Aynı|  
|Birleştirmeler uygulama|Kullanan `Join` / `join` yan tümcesi|Kullanabileceğiniz `Join` / `join` yan tümcesi, ancak daha etkili bir şekilde kullandığı <xref:System.Data.Linq.Mapping.AssociationAttribute> özniteliği. Daha fazla bilgi için [sorgulama arasında ilişkiler](../../../../../../docs/framework/data/adonet/sql/linq/querying-across-relationships.md).|  
|Uzaktan yerel yürütme karşılaştırması||Daha fazla bilgi için [uzak vs. Yerel yürütme](../../../../../../docs/framework/data/adonet/sql/linq/remote-vs-local-execution.md).|  
|Önbelleğe alınan sorgulama karşılaştırması akış|Bir yerel bellek senaryosunda uygulanamaz||  
  
## <a name="see-also"></a>Ayrıca bkz.

- [LINQ sorguları (C#) giriş](~/docs/csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md)
- [Temel LINQ Sorgu İşlemleri](~/docs/csharp/programming-guide/concepts/linq/basic-linq-query-operations.md)
- [LINQ Sorgu İşlemlerinde Tür İlişkileri](~/docs/csharp/programming-guide/concepts/linq/type-relationships-in-linq-query-operations.md)
- [Sorgu Kavramları](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)
