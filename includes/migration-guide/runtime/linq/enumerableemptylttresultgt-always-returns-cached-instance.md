---
ms.openlocfilehash: c9efbefc2bce9e21f328680795e72b62bfcd5cbd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59805326"
---
### <a name="enumerableemptytresult-always-returns-cached-instance"></a>Enumerable.Empty\<TResult > döndürür, örnek her zaman önbelleğe alınmış

|   |   |
|---|---|
|Ayrıntılar|.NET Framework 4.5 içinde başlayan <xref:System.Linq.Enumerable.Empty%60%601> her zaman önbelleğe alınmış bir dahili örnek döndüren <xref:System.Collections.Generic.IEnumerable%601>. Daha önce <xref:System.Linq.Enumerable.Empty%60%601> boş bir önbellek <xref:System.Collections.Generic.IEnumerable%601> API çağrıldı zaman, bazı koşullarda, yani <xref:System.Linq.Enumerable.Empty%60%601> hızlı bir şekilde ve aynı anda farklı çağrıldı türün örneklerinin farklı çağrılar için döndürülemedi API.|
|Öneri|Önceki davranışı belirleyici olduğu için kodu bağımlı beklenmez. Ancak, boş enumerables karşılaştırıldığı ve bazen eşit olması beklenen olası durumda açık boş diziler oluşturulmalıdır (<code>new T[0]</code>) kullanmak yerine <xref:System.Linq.Enumerable.Empty%60%601>.|
|Kapsam|Kenar|
|Sürüm|4,5|
|Tür|Çalışma zamanı|
|Etkilenen API’ler|<ul><li><xref:System.Linq.Enumerable.Empty%60%601?displayProperty=nameWithType></li></ul>|
