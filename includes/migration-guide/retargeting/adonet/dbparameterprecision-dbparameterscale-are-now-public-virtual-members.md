---
ms.openlocfilehash: 1721d32f8cdc9b6ea4b4732e38afa56a8a532600
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62093630"
---
### <a name="dbparameterprecision-and-dbparameterscale-are-now-public-virtual-members"></a>DbParameter.Precision ve DbParameter.Scale artık genel sanal üyedir

|   |   |
|---|---|
|Ayrıntılar|<xref:System.Data.Common.DbParameter.Precision> ve <xref:System.Data.Common.DbParameter.Scale> genel sanal özellik olarak uygulanır. Bunlar, karşılık gelen <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Precision> ve <xref:System.Data.Common.DbParameter.System%23Data%23IDbDataParameter%23Scale> belirtik arabirim kullanmalarının yerini alır.|
|Öneri|Bir ADO.NET veritabanı sağlayıcısını yeniden oluştururken, bu farklar 'override' anahtar sözcüğünün Precision ve Scale özelliklerine uygulanmasını gerektirir. Bu yalnızca bileşenler yeniden oluşturulurken gereklidir; mevcut ikililer çalışmaya devam eder.|
|Kapsam|İkincil|
|Sürüm|4.5.1|
|Tür|Yeniden Hedefleme|
|Etkilenen API’ler|<ul><li><xref:System.Data.Common.DbParameter.Precision?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbParameter.Scale?displayProperty=nameWithType></li></ul>|
