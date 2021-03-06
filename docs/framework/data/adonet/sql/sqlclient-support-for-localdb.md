---
title: Yerel Veritabanı için SqlClient Desteği
ms.date: 03/30/2017
ms.assetid: cf796898-5575-46f2-ae6e-21e5aa8c4123
ms.openlocfilehash: 23fe0d19ad31c0b09e1a12b5ea25e45a973a14f4
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64645836"
---
# <a name="sqlclient-support-for-localdb"></a>Yerel Veritabanı için SqlClient Desteği
SQL Server kod adı Denali başlayarak adlı LocalDB, SQL Server'ın basit bir sürümü kullanıma sunulacaktır. Bu konuda, bir LocalDB veritabanına bağlanmak nasıl ele alınmaktadır.  
  
## <a name="remarks"></a>Açıklamalar  
 LocalDB yükleme ve uygulamanızı LocalDB örneğini yapılandırmak da dahil olmak üzere LocalDB hakkında daha fazla bilgi için SQL Server Books Online'a bakın.  
  
 LocalDB ile neler yapabileceğinizi özetlemek için:  
  
- Oluşturup LocalDB örnekleri sqllocaldb.exe veya app.config dosyanız ile başlatın.  
  
- SqlCmd.exe eklemek ve bir LocalDB örneğini veritabanlarında değiştirmek için kullanın. Örneğin: `sqlcmd -S (localdb)\myinst`  
  
- Kullanım `AttachDBFilename` LocalDB Örneğiniz için bir veritabanı eklemek için bağlantı dizesi anahtar sözcüğü. Kullanırken `AttachDBFilename`, veritabanı adı belirtmezseniz, `Database` bağlantı dizesi anahtar sözcüğü, bir veritabanı uygulama kapandığında LocalDB örneğinden kaldırılacak.  
  
- LocalDB örneğini bağlantı dizenizi belirtin. Örneğin, örnek adınızdır `myInstance`, bağlantı dizesini içerir:  
  
    ```  
    server=(localdb)\\myInstance  
    ```  
  
 `User Instance=True` bir LocalDB veritabanına bağlanırken izin verilmez.  
  
 Localdb'den indirebileceğiniz [Microsoft SQL Server 2012 Feature Pack'in](https://www.microsoft.com/download/en/details.aspx?id=29065). Sqlcmd.exe LocalDB Örneğinizde verileri değiştirmek için kullanacaksanız, SQL Server 2012 özellik Paketi'nden da edinebilirsiniz SQL Server 2012'den sqlcmd gerekir.  
  
## <a name="programmatically-create-a-named-instance"></a>Adlandırılmış bir örnek program aracılığıyla oluşturma  
 Bir uygulama, adlandırılmış bir örnek oluşturursanız ve bir veritabanı gibi belirtin:  
  
- App.config dosyasında gibi oluşturmak üzere LocalDB örneklerini belirtin.  Örnek uygulamanın sürüm sayısını LocalDB yüklemenizin sürüm numarası aynı olmalıdır.  
  
    ```xml  
    <?xml version="1.0" encoding="utf-8" ?>  
    <configuration>  
      <configSections>  
        <section  
        name="system.data.localdb"  
        type="System.Data.LocalDBConfigurationSection,System.Data,Version=4.0.0.0,Culture=neutral,PublicKeyToken=b77a5c561934e089"/>  
      </configSections>  
      <system.data.localdb>  
        <localdbinstances>  
          <add name="myInstance" version="11.0" />  
        </localdbinstances>  
      </system.data.localdb>  
    </configuration>  
    ```  
  
- Kullanarak örnek adını belirtin `server` bağlantı dizesi anahtar sözcüğü.  Belirtilen örnek adı `server` bağlantı dizesi anahtar kelimesi, app.config dosyasında belirtilen adı eşleşmelidir.  
  
- Kullanım `AttachDBFilename` belirtmek için bağlantı dizesi anahtar sözcüğü. MDF dosyası.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [SQL Server Özellikleri ve ADO.NET](../../../../../docs/framework/data/adonet/sql/sql-server-features-and-adonet.md)
- [ADO.NET yönetilen sağlayıcıları ve DataSet Geliştirici Merkezi](https://go.microsoft.com/fwlink/?LinkId=217917)
