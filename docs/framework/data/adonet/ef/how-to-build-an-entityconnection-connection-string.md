---
title: 'Nasıl yapılır: Bir EntityConnection Bağlantı Dizesi Oluşturma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 5bd1a748-3df7-4d0a-a607-14f25e3175e9
ms.openlocfilehash: 335c85d5234df4dd00d0ee65b2077996411081b3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61606621"
---
# <a name="how-to-build-an-entityconnection-connection-string"></a>Nasıl yapılır: Bir EntityConnection Bağlantı Dizesi Oluşturma
Bu konu nasıl oluşturulacağını gösteren bir örnek sağlar bir <xref:System.Data.EntityClient.EntityConnection>.  
  
### <a name="to-run-the-code-in-this-example"></a>Bu örnekte, kodu çalıştırmak için  
  
1. Ekleme [AdventureWorks satışları modeli](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) projenize ve projenizi kullanmak üzere yapılandırma [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]. Daha fazla bilgi için [nasıl yapılır: Varlık veri modeli Sihirbazı'nı](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100)).  
  
2. Uygulamanız için kod sayfasında, aşağıdakileri ekleyin `using` deyimleri (`Imports` Visual Basic'te):  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek başlatır <xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=nameWithType> için alttaki sağlayıcı, ardından başlatır <xref:System.Data.EntityClient.EntityConnectionStringBuilder?displayProperty=nameWithType> nesne ve bu nesnesi oluşturucusuna iletir <xref:System.Data.EntityClient.EntityConnection>.  
  
 [!code-csharp[DP EntityServices Concepts#BuildingConnectionStringWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#buildingconnectionstringwithentitycommand)]
 [!code-vb[DP EntityServices Concepts#BuildingConnectionStringWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#buildingconnectionstringwithentitycommand)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Bir nesne bağlamına ile EntityConnection kullanın](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738461(v=vs.100))
- [Entity Framework için EntityClient Sağlayıcısı](../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)
