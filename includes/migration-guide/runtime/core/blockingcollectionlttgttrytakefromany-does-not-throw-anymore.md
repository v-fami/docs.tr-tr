---
ms.openlocfilehash: 9e8f9c616d5ae4ed17f35665cff21acbbacda457
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59805308"
---
### <a name="blockingcollectionttrytakefromany-does-not-throw-anymore"></a>Blockingcollection'a\<T >. TryTakeFromAny artık oluşturmaz

|   |   |
|---|---|
|Ayrıntılar|Giriş koleksiyonlardan biri tamamlandı, olarak işaretlenmişse <xref:System.Collections.Concurrent.BlockingCollection%601.TryTakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@)> artık -1 döndürür ve <xref:System.Collections.Concurrent.BlockingCollection%601.TakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@)> artık bir özel durum oluşturur. Bu değişiklik, koleksiyonlardan biri boş veya tamamlanmış olduğunda koleksiyonlarla çalışmayı mümkün kılar, ancak diğer koleksiyonda hala alınabilecek öğeler bulunur.|
|Öneri|Denetim akışı amacıyla durumlarda tamamlanmasını engelleyici bir koleksiyon, -1 veya TakeFromAny atma TryTakeFromAny kullanıldıysa, bu tür kod artık kullanılacak değiştirilmelidir <code>.Any(b =&gt; b.IsCompleted)</code> bu koşulunu algılamak için.|
|Kapsam|İkincil|
|Sürüm|4,5|
|Tür|Çalışma zamanı|
|Etkilenen API’ler|<ul><li><xref:System.Collections.Concurrent.BlockingCollection%601.TakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@)?displayProperty=nameWithType></li><li><xref:System.Collections.Concurrent.BlockingCollection%601.TakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Collections.Concurrent.BlockingCollection%601.TryTakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@)?displayProperty=nameWithType></li><li><xref:System.Collections.Concurrent.BlockingCollection%601.TryTakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Collections.Concurrent.BlockingCollection%601.TryTakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@,System.TimeSpan)?displayProperty=nameWithType></li><li><xref:System.Collections.Concurrent.BlockingCollection%601.TryTakeFromAny(System.Collections.Concurrent.BlockingCollection{%600}[],%600@,System.TimeSpan)?displayProperty=nameWithType></li></ul>|
