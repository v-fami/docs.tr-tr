---
title: 'Nasıl yapılır: Birincil Anahtarları Temsil Etme'
ms.date: 03/30/2017
ms.assetid: 63c65289-6539-42b2-8493-891c232018fa
ms.openlocfilehash: dcb8929c9cd9a7b88f19d760b70117a1092760f9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61877207"
---
# <a name="how-to-represent-primary-keys"></a>Nasıl yapılır: Birincil Anahtarları Temsil Etme
Kullanım [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A> özelliği <xref:System.Data.Linq.Mapping.ColumnAttribute> bir özellik veya alan için bir veritabanı sütunu birincil anahtar temsil etmek için belirtmek için özniteliği.  
  
 Kod örnekleri için bkz: <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A>.  
  
> [!NOTE]
>  [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] Hesaplanan sütunlar, birincil anahtar olarak desteklemez.  
  
### <a name="to-designate-a-property-or-field-as-a-primary-key"></a>Bir özellik veya alan bir birincil anahtar olarak atamak için  
  
1. Ekleme <xref:System.Data.Linq.Mapping.ColumnAttribute.IsPrimaryKey%2A> özelliğini <xref:System.Data.Linq.Mapping.ColumnAttribute> özniteliği.  
  
2. Değeri olarak belirtin `true`.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [LINQ to SQL Nesne Modeli](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
- [Nasıl yapılır: Kod Düzenleyicisi'ni kullanarak varlık sınıflarını özelleştirme](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
