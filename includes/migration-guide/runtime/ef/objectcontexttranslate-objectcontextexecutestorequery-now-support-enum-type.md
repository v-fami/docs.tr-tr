---
ms.openlocfilehash: 1d2d6133683360b97569e49402e7c8c4d182b65d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59805261"
---
### <a name="objectcontexttranslate-and-objectcontextexecutestorequery-now-support-enum-type"></a>ObjectContext.Translate ve ObjectContext.ExecuteStoreQuery artık destek enum türü

|   |   |
|---|---|
|Ayrıntılar|.NET Framework 4.0, genel parametre <code>T</code> , <code>ObjectContext.Translate</code> ve <code>ObjectContext.ExecuteStoreQuery</code> yöntemleri bir sabit listesi yüklenemedi. Bu senaryonun artık desteklenmektedir.|
|Öneri|Enum türü .NET Framework 4. 0'ı üzerinde Çevir veya ExecuteStoreQuery çağrıldı, '0' döndürüldü. Bu davranışı arzu olduysa, çağrıları 0 sabiti (veya onu enum eşdeğeri) ile değiştirilmelidir.|
|Kapsam|Kenar|
|Sürüm|4,5|
|Tür|Çalışma zamanı|
|Etkilenen API’ler|<ul><li><xref:System.Data.Objects.ObjectContext.Translate%60%601(System.Data.Common.DbDataReader)?displayProperty=nameWithType></li><li><xref:System.Data.Objects.ObjectContext.Translate%60%601(System.Data.Common.DbDataReader,System.String,System.Data.Objects.MergeOption)?displayProperty=nameWithType></li><li><xref:System.Data.Objects.ObjectContext.ExecuteStoreQuery%60%601(System.String,System.Object[])?displayProperty=nameWithType></li><li><xref:System.Data.Objects.ObjectContext.ExecuteStoreQuery%60%601(System.String,System.String,System.Data.Objects.MergeOption,System.Object[])?displayProperty=nameWithType></li></ul>|
