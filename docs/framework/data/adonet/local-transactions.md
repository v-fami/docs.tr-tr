---
title: Yerel İşlemler
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8ae3712f-ef5e-41a1-9ea9-b3d0399439f1
ms.openlocfilehash: f686c20a9afd981405e32854fcc594abac78c85c
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65882037"
---
# <a name="local-transactions"></a>Yerel İşlemler
ADO.NET'te işlemler, böylece bunlar iş tek bir birim olarak yürütmek için birden çok görevleri birbirine bağlayın istediğinizde kullanılır. Örneğin, bir uygulama iki görevleri gerçekleştirir düşünün. İlk olarak bir tablo ile sipariş bilgilerini güncelleştirir. İkinci olarak, Envanter bilgilerini içeren bir tablo güncelleştirir, öğeleri borçlandırarak sıralı. Her iki görev başarısız olursa, her iki güncelleştirmeleri geri alınır.  
  
## <a name="determining-the-transaction-type"></a>İşlem türünü belirleme  
 Bir işlem tek aşamalı işlem ve veritabanı tarafından doğrudan gerçekleştirilir, yerel bir işlem olarak kabul edilir. Bir işlem, işlem İzleyici tarafından düzenlenir ve işlem çözümlemesi için (örneğin, iki aşamalı tamamlama) emniyet mekanizmaları kullanan dağıtılmış bir işlem olarak kabul edilir.  
  
 Her .NET Framework veri sağlayıcıları kendi sahip `Transaction` yerel işlemler gerçekleştirmek için nesne. Bir SQL Server veritabanında gerçekleştirilecek bir işlemi gerekiyorsa, seçin bir <xref:System.Data.SqlClient> işlem. Bir Oracle işlem için kullanmak <xref:System.Data.OracleClient> sağlayıcısı. Ayrıca, bir <xref:System.Data.Common.DbTransaction> işlemleri gerektiren sağlayıcısı-bağımsız kod yazmak için kullanılabilen sınıfı.  
  
> [!NOTE]
> Sunucuda gerçekleştirildiğinde hareketleri en etkili olur. Kapsamlı açık işlemleri kullanımını sağlayan bir SQL Server veritabanı ile çalışıyorsanız, bunları BEGIN TRANSACTION Transact-SQL deyimini kullanarak saklı yordam yazma göz önünde bulundurun.
  
## <a name="performing-a-transaction-using-a-single-connection"></a>Tek bir bağlantı kullanarak işlem gerçekleştirme  
 ADO.NET ile işlemleri denetleme `Connection` nesne. Yerel bir işlem ile başlatabilir `BeginTransaction` yöntemi. İşlem başlamıştır sonra bu işlem ile bir komut listeleme `Transaction` özelliği bir `Command` nesne. Daha sonra tamamlama veya başarı veya hata işlem bileşenlerinin göre veri kaynağında yapılan değişiklikleri geri alma.  
  
> [!NOTE]
>  `EnlistDistributedTransaction` Yöntemi yerel bir işlem için kullanılmamalıdır.  
  
 İşlem kapsamı bağlantı sınırlıdır. Aşağıdaki örnek iki ayrı komutlar olarak içeren açık işlem gerçekleştiren `try` blok. Komutlar Production.ScrapReason tabloya yönelik INSERT deyimleri AdventureWorks SQL Server örnek veritabanında Eğer hiçbir özel durum harekete olduğu konusunda çok hassasız yürütün. Kodda `catch` blok yapar geri işlem bir özel durum oluşturulursa. İşlem iptal edildi veya işlem tamamlanmadan önce bağlantı kapalı ise, otomatik olarak geri alınır.  
  
## <a name="example"></a>Örnek  
 Bir işlem gerçekleştirmek için aşağıdaki adımları izleyin.  
  
1. Çağrı <xref:System.Data.SqlClient.SqlConnection.BeginTransaction%2A> yöntemi <xref:System.Data.SqlClient.SqlConnection> hareketin başlangıcını işaretlemek için nesne. <xref:System.Data.SqlClient.SqlConnection.BeginTransaction%2A> Yöntemi işlem bir başvuru döndürür. Bu başvuru atandığı <xref:System.Data.SqlClient.SqlCommand> kayıtlı nesneler.  
  
2. Ata `Transaction` nesnesini <xref:System.Data.SqlClient.SqlCommand.Transaction%2A> özelliği <xref:System.Data.SqlClient.SqlCommand> yürütülecek. Etkin bir işlem ile bir bağlantı üzerindeki bir komut yürütülürse ve `Transaction` nesne değil atanmış için `Transaction` özelliği `Command` nesnesi, bir özel durum harekete geçirilir.  
  
3. Gerekli komutları yürütün.  
  
4. Çağrı <xref:System.Data.SqlClient.SqlTransaction.Commit%2A> yöntemi <xref:System.Data.SqlClient.SqlTransaction> , işlemi tamamlamak için nesne veya çağrı <xref:System.Data.SqlClient.SqlTransaction.Rollback%2A> işlemi sonlandırmak için yöntemi. Bağlantı kapalı veya önce ya da elden <xref:System.Data.SqlClient.SqlTransaction.Commit%2A> veya <xref:System.Data.SqlClient.SqlTransaction.Rollback%2A> yöntem yürütüldüğünde, işlem geri alındı.  
  
 Aşağıdaki kod örneği, Microsoft SQL Server ile ADO.NET kullanarak işlem mantığı gösterir.  
  
 [!code-csharp[DataWorks SqlTransaction.Local#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlTransaction.Local/CS/source.cs#1)]
 [!code-vb[DataWorks SqlTransaction.Local#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlTransaction.Local/VB/source.vb#1)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [İşlemler ve Eşzamanlılık](../../../../docs/framework/data/adonet/transactions-and-concurrency.md)
- [Dağıtılmış İşlemler](../../../../docs/framework/data/adonet/distributed-transactions.md)
- [SQL Server ile System.Transactions Tümleştirmesi](../../../../docs/framework/data/adonet/system-transactions-integration-with-sql-server.md)
- [ADO.NET yönetilen sağlayıcıları ve DataSet Geliştirici Merkezi](https://go.microsoft.com/fwlink/?LinkId=217917)
