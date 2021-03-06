---
title: model-declared function
ms.date: 03/30/2017
ms.assetid: aba87f13-5685-4f6b-ad14-918e8a7d5c2a
ms.openlocfilehash: a0bea36693122c77d9c1abdf4484ee8e68627a0c
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64645867"
---
# <a name="model-declared-function"></a>model-declared function
A *model olarak bildirilen işlev* kavramsal modelde bildirildi, ancak bu kavramsal modelde tanımlı değil, bir işlevdir. İşlevi barındırma veya depolama ortamında tanımlanabilir. Örneğin, bir model olarak bildirilen işlev dolayısıyla kavramsal modelde sunucu tarafında işlevselliği kullanıma sunma, bir veritabanında tanımlı bir işlev eşleştirilmiş olabilir.  
  
 Model olarak bildirilen bir işlevin bildirimi, aşağıdaki bilgileri içerir:  
  
- İşlevin adı. (Gerekli)  
  
- Dönüş değerinin türü. (İsteğe bağlı)  
  
    > [!NOTE]
    >  Dönüş değeri belirtilmişse, dönüş türü void alır.  
  
- Parametre adı ve türü de dahil olmak üzere, parametre bilgileri. (İsteğe bağlı)  
  
## <a name="example"></a>Örnek  
 [ADO.NET Entity Framework](./ef/index.md) kavramsal şema tanım dili olarak adlandırılan bir etki alanına özgü dil (DSL) kullanır ([CSDL](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec)) kavramsal modeller tanımlamak için. CSDL bir model olarak bildirilen bir işlevi bir işlev içeri aktarma uygulamasıdır (kullanarak [Functionımport öğesi](/ef/ef6/modeling/designer/advanced/edmx/csdl-spec#functionimport-element-csdl)). Aşağıdaki CSDL işlev tanımını içeri aktarma ile varlık kapsayıcısı tanımlar. Dönüş türü belirtildiği işlevi için dönüş türü void olduğunu unutmayın.  
  
 [!code-xml[EDM_Example_Model#FunctionImport](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books4.edmx#functionimport)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Varlık Veri Modeli Temel Kavramları](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Varlık Veri Modeli](../../../../docs/framework/data/adonet/entity-data-model.md)
