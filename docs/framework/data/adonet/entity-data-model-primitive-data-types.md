---
title: 'Varlık Veri Modeli: Basit Veri Türleri'
ms.date: 03/30/2017
ms.assetid: 7635168e-0566-4fdd-8391-7941b0d9f787
ms.openlocfilehash: 044a0ed981bb9cda3550fb3a3a9f1cb9bff96f25
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61667138"
---
# <a name="entity-data-model-primitive-data-types"></a>Varlık Veri Modeli: Basit Veri Türleri
Varlık veri modeli (EDM) (örneğin, dize, Boolean, Int32 vb.) tanımlamak için kullanılan soyut temel veri türleri kümesi destekler [özellikleri](../../../../docs/framework/data/adonet/property.md) kavramsal modelde. Bu basit veri türleri depolama veya SQL Server veritabanı veya ortak dil çalışma zamanı (CLR) gibi barındırma ortamı desteklenir gerçek ilkel veri türleri için proxy'ler. EDM ilkel veri türleri üzerinde işlemler ve dönüştürmeler semantiği tanımlamıyor; Bu semantiği depolama veya barındırma ortamı tarafından tanımlanır. Genellikle, EDM ilkel veri türleri karşılık gelen Basit veri türleri depolama veya barındırma ortamında eşlenir. Entity Framework EDM ilkel türlerinde SQL Server veri türlerine eşlemelerini nasıl hakkında daha fazla bilgi için bkz: [Entity FrameworkTypes için SqlClient](../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-types.md).  
  
> [!NOTE]
>  EDM ilkel veri türleri koleksiyonunu desteklemiyor.  
  
 EDM yapısal veri türleri hakkında daha fazla bilgi için bkz. [varlık türü](../../../../docs/framework/data/adonet/entity-type.md) ve [karmaşık tür](../../../../docs/framework/data/adonet/complex-type.md).  
  
## <a name="primitive-data-types-supported-in-the-entity-data-model"></a>Varlık veri modeli desteklenen temel veri türleri  
 Aşağıdaki tabloda EDM tarafından desteklenen temel veri türlerini listeler. Tabloda ayrıca [modelleri](../../../../docs/framework/data/adonet/facet.md) her ilkel veri türü için uygulanabilir.  
  
|Basit veri türü|Açıklama|Geçerli modelleri|  
|-------------------------|-----------------|-----------------------|  
|İkili|İkili veriler içerir.|MaxLength, FixedLength, null, varsayılan|  
|Boole değeri|Değeri içeren `true` veya `false`.|Boş değer atanabilir, varsayılan|  
|Bayt|İmzalanmamış 8 bit tam sayı değeri içerir.|Duyarlık, null, varsayılan|  
|DateTime|Tarih ve saati temsil eder.|Duyarlık, null, varsayılan|  
|DateTimeOffset|Bir tarih ve saat olarak GMT'den dakikalar içinde bir uzaklık içerir.|Duyarlık, null, varsayılan|  
|Ondalık|Sabit kesinlik ve ölçek ile sayısal bir değer içeriyor.|Duyarlık, null, varsayılan|  
|Çift|Kayan nokta numarası ile 15 basamaklı duyarlık içerir.|Duyarlık, null, varsayılan|  
|Float|Kayan noktalı sayı yedi basamaklı duyarlık içerir.|Duyarlık, null, varsayılan|  
|Guid|16 baytlık benzersiz bir tanımlayıcı içerir.|Duyarlık, null, varsayılan|  
|Int16|İşaretli 16 bit tam sayı değeri içerir.|Duyarlık, null, varsayılan|  
|Int32|İşaretli 32-bit tamsayı değeri içerir.|Duyarlık, null, varsayılan|  
|Int64|Bir 64-bit işaretli tamsayı değeri içerir.|Duyarlık, null, varsayılan|  
|SByte|İşaretli 8 bit tam sayı değeri içerir.|Duyarlık, null, varsayılan|  
|Dize|Karakter verileri içerir.|Varsayılan Unicode, FixedLength, MaxLength, harmanlaması, boş değer atanabilir, duyarlık|  
|Zaman|Günün bir saati içerir.|Duyarlık, null, varsayılan|  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Varlık Veri Modeli Temel Kavramları](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Varlık Veri Modeli](../../../../docs/framework/data/adonet/entity-data-model.md)
