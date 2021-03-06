---
title: 'İşlemleri Özelleştirme: Genel Bakış'
ms.date: 03/30/2017
ms.assetid: a3546296-1443-4b88-aa6e-d41011041ba7
ms.openlocfilehash: 29fb75271b7bc324d462078e94e4a28534986fba
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62038099"
---
# <a name="customizing-operations-overview"></a>İşlemleri Özelleştirme: Genel Bakış
Varsayılan olarak, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] dinamik SQL ekleme, güncelleştirme ve silme işlemleri eşlemesini göre oluşturur. Ancak, uygulamada genellikle güvenlik, doğrulama ve benzeri sağlamak için kendi iş mantıklarını eklemesini istersiniz.  
  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] Bu işlemler özelleştirmeye yönelik teknikler arasında şunlar yer alır.  
  
## <a name="loading-options"></a>Yükleme Seçenekleri  
 Sorgularınızdaki, veritabanına bağlanmak için ana hedef ilgili ne kadar veri alınır kontrol edebilirsiniz. Bu işlev büyük ölçüde kullanılarak uygulanan <xref:System.Data.Linq.DataLoadOptions>. Daha fazla bilgi için [Ertelenen hemen yükleme](../../../../../../docs/framework/data/adonet/sql/linq/deferred-versus-immediate-loading.md).  
  
## <a name="partial-methods"></a>Kısmi Yöntemler  
 Kendi varsayılan eşlemesinde [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] iş mantığınızı uygulamanıza yardımcı olmak için kısmi yöntemler sağlar. Daha fazla bilgi için [ekleyerek iş mantığı kullanarak kısmi yöntemler](../../../../../../docs/framework/data/adonet/sql/linq/adding-business-logic-by-using-partial-methods.md).  
  
## <a name="stored-procedures-and-user-defined-functions"></a>Saklı yordamları ve kullanıcı tanımlı işlevleri  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] saklı yordamları ve kullanıcı tanımlı işlevleri destekler. Saklı yordamlar, sık sık operations özelleştirmek için kullanılır. Daha fazla bilgi için [saklı yordamlar](../../../../../../docs/framework/data/adonet/sql/linq/stored-procedures.md).  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Insert, Update ve Delete İşlemlerini Özelleştirme](../../../../../../docs/framework/data/adonet/sql/linq/customizing-insert-update-and-delete-operations.md)
