---
title: 'Nasıl yapılır: Windows Forms DataGridView Denetimindeki Verileri Doğrulama'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data [Windows Forms], validation
- DataGridView control [Windows Forms], data validation
- data grids [Windows Forms], validating data
- data validation [Windows Forms], Windows Forms
ms.assetid: d10aef35-701e-4a3c-a684-2a2ed1aeaca6
ms.openlocfilehash: 12fd668e22703271f8c629baf56487dd084cfd8b
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65591037"
---
# <a name="how-to-validate-data-in-the-windows-forms-datagridview-control"></a>Nasıl yapılır: Windows Forms DataGridView Denetimindeki Verileri Doğrulama
Aşağıdaki kod örneği, içinde bir kullanıcı tarafından girilen verileri doğrulamak gösterilmiştir bir <xref:System.Windows.Forms.DataGridView> denetimi. Bu örnekte, <xref:System.Windows.Forms.DataGridView> satırlardan doldurulur `Customers` Northwind örnek veritabanıyla kurulan tablosu. Kullanıcı bir hücreye zaman düzenlediğini `CompanyName` sütununda, değerini test geçerliliğini, boş olmadığını kontrol ederek. Varsa için olay işleyicisini <xref:System.Windows.Forms.DataGridView.CellValidating> olay bulur değeri boş bir dize olduğunu <xref:System.Windows.Forms.DataGridView> kullanıcının boş olmayan bir dize girilene kadar hücre çıkmasını engeller.  
  
 Bu kod örneği tam bir açıklaması için bkz. [izlenecek yol: Doğrulama verileri Windows Forms DataGridView denetiminde](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md).  
  
## <a name="example"></a>Örnek  
 [!code-csharp[System.Windows.Forms.DataGridViewDataValidation#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/CS/datavalidation.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewDataValidation#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewDataValidation/VB/datavalidation.vb#00)]  
  
## <a name="compiling-the-code"></a>Kod Derleniyor  
 Bu örnek gerektirir:  
  
- Sistem, System.Data, System.Windows.Forms ve System.XML derlemesine ilişkin başvurular.  
  
## <a name="net-framework-security"></a>.NET Framework Güvenliği  
 Depolama bağlantı dizesi içinde bir parola gibi hassas bilgileri, uygulamanızın güvenliğini etkileyebilir. Windows Kimlik Doğrulaması (tümleşik güvenlik olarak da bilinir) kullanılarak bir veritabanına erişimi denetlemek için daha güvenli bir yoldur. Daha fazla bilgi için [bağlantı bilgilerini koruma](../../data/adonet/protecting-connection-information.md).  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [İzlenecek yol: Windows Forms DataGridView denetiminde verileri doğrulama](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)
- [Windows Forms DataGridView Denetiminde Veri Girişi](data-entry-in-the-windows-forms-datagridview-control.md)
- [İzlenecek yol: Windows Forms DataGridView denetimine veri girişi sırasında oluşan hataları ele alma](handling-errors-that-occur-during-data-entry-in-the-datagrid.md)
- [Bağlantı Bilgilerini Koruma](../../data/adonet/protecting-connection-information.md)
