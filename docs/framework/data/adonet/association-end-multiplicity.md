---
title: association end multiplicity
ms.date: 03/30/2017
ms.assetid: 340926ee-aefb-4bef-92cc-453e5251fd03
ms.openlocfilehash: e889394dc28bfe1352bd4c8497d5a74919279fe7
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64592625"
---
# <a name="association-end-multiplicity"></a>association end multiplicity
*İlişki sonu çoğulluk* sayısını tanımlayan [varlık türü](../../../../docs/framework/data/adonet/entity-type.md) bir sonunda olabilir örnekleri bir [ilişkilendirme](../../../../docs/framework/data/adonet/association-type.md).  
  
 Bir ilişkilendirme end çoğulluk aşağıdaki değerlerden biri olabilir:  
  
- bir (1): Bu tam olarak bir varlık türü örneği ilişkilendirme sonunda olup olmadığını gösterir.  
  
- sıfır veya bir (0..1): Sıfır veya bir varlık türü örneklerini ilişkilendirme sonunda bulunduğunu gösterir.  
  
- çok sayıda (\*): sıfır, bir veya daha fazla varlık türü örneklerini ilişkilendirme sonunda bulunduğunu gösterir.  
  
 Bir ilişkilendirme genellikle, ilişki uç Çeşitlilikler tarafından belirlenir. Örneğin, bir ilişki sonu bir (1) ve çok sayıda Çeşitlilikler varsa (\*), ilişkilendirmenin bir-çok ilişkisi adı verilir. Aşağıdaki örnekte `PublishedBy` işbirliğidir bir-çok ilişkisi (bir çok kitap bir yayımcı yayımlar ve bir kitap bir yayımcı tarafından yayımlanır). `WrittenBy` Bir çoktan çoğa ilişki bir ilişkilendirmedir (bir kitap birden çok yazarlar olabilir ve birden çok books Yazar yazabilirsiniz).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki diyagramda iki ilişkilendirmeleri kavramsal bir modelle gösterilmektedir: `PublishedBy` ve `WrittenBy`. İlişkilendirme sona için `PublishedBy` ilişkisi olan `Book` ve `Publisher` varlık türleri. Çokluğu `Publisher` sonudur bir (1) ve çeşitliliğini `Book` sonudur birçok (\*).  
  
 ![Üç varlık türleri ile örnek modeli](./media/association-end-multiplicity/example-model-three-entity-types.gif)  
  
 ADO.NET varlık çerçevesi kavramsal şema tanım dili olarak adlandırılan bir etki alanına özgü dil (DSL) kullanır ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) kavramsal modeller tanımlamak için. Aşağıdaki CSDL tanımlar `PublishedBy` Yukarıdaki diyagramda gösterilen ilişkiyi:  
  
 [!code-xml[EDM_Example_Model#AssociationExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#associationexample)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Varlık Veri Modeli Temel Kavramları](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Varlık Veri Modeli](../../../../docs/framework/data/adonet/entity-data-model.md)
