---
title: (Varlık SQL) gidin
ms.date: 03/30/2017
ms.assetid: f107f29d-005f-4e39-a898-17f163abb1d0
ms.openlocfilehash: 993c07b824d30c89773c5cfea90c7c194c6b3869
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61760421"
---
# <a name="navigate-entity-sql"></a>(Varlık SQL) gidin

Oluşturulan varlıklar arasında ilişki üzerinden gider.

## <a name="syntax"></a>Sözdizimi

```
navigate(instance-expression, [relationship-type], [to-end [, from-end] ])
```

## <a name="arguments"></a>Arguments

`instance-expression` Bir varlık örneği.

`relationship-type` Kavramsal şema tanım dili (CSDL) dosyasından bir ilişki türü adı. `relationship-type` Olarak nitelenmiş \<ad alanı >.\< ilişki türü adı >.

`to` İlişki sonu.

`from` İlişki başlangıcı.

## <a name="return-value"></a>Dönüş Değeri

Varsa önem düzeyini sonlandırmak için 1, dönüş değeri olacak `Ref<T>`. Varsa önem düzeyini sonlandırmak için n olduğundan, dönüş değeri olacak `Collection<Ref<T>>`.

## <a name="remarks"></a>Açıklamalar

Birinci sınıf yapılardan ilişkisidir [!INCLUDE[adonet_edm](../../../../../../includes/adonet-edm-md.md)] (EDM). İki veya daha fazla varlık türleri ilişkiler oluşturulabilir ve kullanıcılar üzerinde bir bitiş (varlık) arasında ilişki gidebilir. `from` ve `to` ilişki içinde ad çözümlemesi belirsizlik olmaz olduğunda koşullu olarak isteğe bağlıdır.

NAVIGATE O ve C alanında geçerli değil.

Bir gezinti yapısı genel formu aşağıda verilmiştir:

navigate(`instance-expression`, `relationship-type`, [ `to-end` [, `from-end` ] ] )

Örneğin:

```sql
Select o.Id, navigate(o, OrderCustomer, Customer, Order)
From LOB.Orders as o
```

OrderCustomer olduğu `relationship`, müşteri ve sipariş `to-end` (müşteri) ve `from-end` (sıra) ilişki. OrderCustomer oluştu n: 1 ilişki sonra Ref navıgate ifadesi sonuç türü olan\<Müşteri >.

Bu ifadenin daha basit form aşağıda verilmiştir:

```sql
Select o.Id, navigate(o, OrderCustomer)
From LOB.Orders as o
```

Benzer şekilde, aşağıdaki biçimde bir sorguda navıgate ifadesi bir koleksiyon oluşturur < Ref\<sipariş >>.

```sql
Select c.Id, navigate(c, OrderCustomer, Order, Customer)
From LOB.Customers as c
```

Örnek ifade bir varlık/başvuru türü olmalıdır.

## <a name="example"></a>Örnek

Aşağıdaki varlık SQL sorgusu NAVIGATE işleci oluşturulan adresi ve SalesOrderHeader varlık türleri ilişkinin üzerine gitmek için kullanır. Sorgu, AdventureWorks satış modelini temel alıyor. Derleme ve bu sorguyu çalıştırmak için bu adımları izleyin:

1. Verilen yordamı izleyin [nasıl yapılır: StructuralType sonuçları döndüren bir sorgu yürütme](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).

2. Aşağıdaki sorguda bağımsız değişken olarak geçirmek `ExecuteStructuralTypeQuery` yöntemi:

 [!code-csharp[DP EntityServices Concepts 2#NAVIGATE](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#navigate)]

## <a name="see-also"></a>Ayrıca bkz.

- [Entity SQL Başvurusu](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [Nasıl yapılır: Gezinme işleci ile ilişkilerde gezinme](../../../../../../docs/framework/data/adonet/ef/language-reference/navigate-entity-sql.md)
