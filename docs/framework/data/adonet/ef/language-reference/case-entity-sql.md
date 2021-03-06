---
title: Durum (varlık SQL)
ms.date: 03/30/2017
ms.assetid: 26a47873-e87d-4ba2-9e2c-3787c21efe89
ms.openlocfilehash: e44f48d040fc77bf702759be0c53a618cd84f9fc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61607199"
---
# <a name="case-entity-sql"></a>Durum (varlık SQL)
Bir dizi olarak değerlendirilir `Boolean` sonucu belirlemek için ifadeler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
CASE  
     WHEN Boolean_expression THEN result_expression   
    [ ...n ]   
     [   
    ELSE else_result_expression   
     ]   
END  
```  
  
## <a name="arguments"></a>Arguments  
 `n`  
 Bu çoklu gösteren bir yer tutucudur, `Boolean_expression` ARDINDAN `result_expression` yan tümceleri kullanılabilir.  
  
 ARDINDAN `result_expression`  
 İfade olduğunda döndürülen `Boolean_expression` değerlendiren `true`. `result expression` Herhangi bir geçerli ifade var.  
  
 ELSE `else_result_expression`  
 İfade yok karşılaştırma işlemi olmaması halinde döndürülür `true`. Bu bağımsız değişken atlanırsa ve herhangi bir karşılaştırma işleminin sonucunu veren `true`, servis talebi null döndürür. `else_result_expression` Herhangi bir geçerli ifade var. Veri türlerini `else_result_expression` ve tüm `result_expression` örtük bir dönüştürme olmalıdır veya aynı olmalıdır.  
  
 NE ZAMAN `Boolean_expression`  
 Olan `Boolean` Aranan büyük/küçük harf biçimi kullanıldığında değerlendirilen ifade. `Boolean_expression` herhangi bir geçerli olduğu `Boolean` ifade.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Kümesinden türlerinde en yüksek öncelik türünü döndürüyor `result_expression` ve isteğe bağlı `else_result_expression`.  
  
## <a name="remarks"></a>Açıklamalar  
 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] Case ifadesi benzer [!INCLUDE[tsql](../../../../../../includes/tsql-md.md)] case ifadesi. Case ifadesi, bir dizi hangi ifadesi uygun bir sonuç verir belirlemek için koşullu test yapmak için kullanın. Case ifadesi bu tür bir dizi bir veya daha fazla geçerli `Boolean` doğru sonuç ifadesi belirlemek için ifadeler.  
  
 Durum işlevi değerlendirir `Boolean_expression` her zaman yan tümcesi sırada belirtilen ve döndürür `result_expression` ilk `Boolean_expression` olarak değerlendirilen `true`. Kalan ifade değerlendirilmez. Hayır ise `Boolean_expression` değerlendiren `true`, veritabanı altyapısı döndürür `else_result_expression` ELSE yan belirtilmezse, ya da ELSE yan tümce belirtilirse bir null değer.  
  
 CASE ifadesi, bir çoklu küme döndüremez.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki varlık SQL sorgusu, bir dizi değerlendirmek için CASE ifadesi kullanır. `Boolean` sonucu belirlemek üzere ifadeler. Sorgu, AdventureWorks satış modelini temel alıyor. Derleme ve bu sorguyu çalıştırmak için bu adımları izleyin:  
  
1. Verilen yordamı izleyin [nasıl yapılır: PrimitiveType sonuçları döndüren bir sorgu yürütme](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-primitivetype-results.md).  
  
2. Aşağıdaki sorguda bağımsız değişken olarak geçirmek `ExecutePrimitiveTypeQuery` yöntemi:  
  
 [!code-csharp[DP EntityServices Concepts 2#CASE_WHEN_THEN_ELSE](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#case_when_then_else)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [THEN](../../../../../../docs/framework/data/adonet/ef/language-reference/then-entity-sql.md)
- [SELECT](../../../../../../docs/framework/data/adonet/ef/language-reference/select-entity-sql.md)
- [Entity SQL Başvurusu](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
