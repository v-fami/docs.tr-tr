---
title: Oracle ve ADO.NET
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8ee8e389-53cf-45cf-80bd-1df63ef34f2e
ms.openlocfilehash: 012a5b55d052f5f06da5c152da79f4676b2bff4e
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65877956"
---
# <a name="oracle-and-adonet"></a>Oracle ve ADO.NET
> [!NOTE]
>  Türlerinde <xref:System.Data.OracleClient> kullanım dışı bırakılmıştır. Türleri geçerli sürümü of.NET Framework içinde desteklenen kalır, ancak gelecekteki bir sürümde kaldırılacak. Microsoft, üçüncü taraf Oracle sağlayıcısı kullanmanızı önerir.  
  
 Bu bölümde, özellikler ve Oracle için .NET Framework veri sağlayıcısı özgü davranışları açıklanmaktadır.  
  
 Oracle için .NET Framework veri sağlayıcısı, Oracle istemci yazılımı tarafından sağlanan Oracle Çağrı Arabirimi (OCI) kullanarak bir Oracle veritabanına erişim sağlar. Veri sağlayıcısı işlevselliği, SQL Server, OLE DB ve ODBC için .NET Framework veri sağlayıcıları benzer olacak şekilde tasarlanmıştır.  
  
 Oracle için .NET Framework veri sağlayıcısı kullanmak için bir uygulama başvurmalıdır <xref:System.Data.OracleClient> gösterildiği gibi ad alanı:  
  
```vb  
Imports System.Data.OracleClient  
```  
  
```csharp  
using System.Data.OracleClient;  
```  
  
 Kodunuzu derlediğinizde de DLL'ye bir başvuru içermelidir. Örneğin, bir C# programı derleme yapıyorsanız, komut satırınızda içermelidir:  
  
```  
csc /r:System.Data.OracleClient.dll  
```  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Sistem Gereksinimleri](../../../../docs/framework/data/adonet/system-requirements-for-the-dotnet-data-provider-for-oracle.md)  
 Oracle için .NET Framework veri sağlayıcısı kullanma gereksinimleri ve bir dizi kullanırken dikkat etmeniz gereken sorunları açıklar.  
  
 [Oracle BFILE](../../../../docs/framework/data/adonet/oracle-bfiles.md)  
 Açıklar <xref:System.Data.OracleClient.OracleBFile> Oracle BDOSYA veri türü ile çalışmak için kullanılan sınıf.  
  
 [Oracle LOB](../../../../docs/framework/data/adonet/oracle-lobs.md)  
 Açıklar <xref:System.Data.OracleClient.OracleLob> Oracle LOB veri türleriyle çalışmak için kullanılan sınıf.  
  
 [Oracle REF CURSOR](../../../../docs/framework/data/adonet/oracle-ref-cursors.md)  
 Oracle REF CURSOR veri türü için destek açıklanır.  
  
 [OracleTypes](../../../../docs/framework/data/adonet/oracletypes.md)  
 Yapıları dahil olmak üzere Oracle veri türleriyle çalışmak için kullanabileceğiniz açıklar <xref:System.Data.OracleClient.OracleNumber> ve <xref:System.Data.OracleClient.OracleString>.  
  
 [Oracle Dizileri](../../../../docs/framework/data/adonet/oracle-sequences.md)  
 Anahtar Oracle sırası sunucu tarafından oluşturulan değerleri almak için destek açıklanır.  
  
 [Oracle Veri Türü Eşlemeleri](../../../../docs/framework/data/adonet/oracle-data-type-mappings.md)  
 Oracle veri türleri ve eşleşmeleri listeler <xref:System.Data.OracleClient.OracleDataReader>.  
  
 [Oracle Dağıtılmış İşlemleri](../../../../docs/framework/data/adonet/oracle-distributed-transactions.md)  
 Açıklayan nasıl <xref:System.Data.OracleClient.OracleConnection> nesne bir işlem etkin olduğunu belirlerse, varolan bir dağıtılmış işlemde otomatik olarak kaydeder.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [ADO.NET Uygulamalarının Güvenliğini Sağlama](../../../../docs/framework/data/adonet/securing-ado-net-applications.md)  
 Güvenli kodlama yöntemleri ADO.NET kullanırken açıklar.  
  
 [DataSets, DataTables ve DataViews](../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)  
 Oluşturma ve kullanma işlemini açıklamaktadır `DataSets`, belirlenmiş `DataSets`, `DataTables`, ve `DataViews`.  
  
 [ADO.NET’te Veri Alma ve Değiştirme](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)  
 ADO.NET'te veri ile nasıl çalışılacağını açıklar.  
  
 [SQL Server ve ADO.NET](../../../../docs/framework/data/adonet/sql/index.md)  
 Özellikler ve SQL Server'a özel işlevler ile nasıl çalışılacağını açıklar.  
  
 [DbProviderFactories](../../../../docs/framework/data/adonet/dbproviderfactories.md)  
 ADO.NET sağlayıcısı-bağımsız kod yazmanıza izin genel sınıfları açıklar.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [ADO.NET](../../../../docs/framework/data/adonet/index.md)
- [ADO.NET yönetilen sağlayıcıları ve DataSet Geliştirici Merkezi](https://go.microsoft.com/fwlink/?LinkId=217917)
