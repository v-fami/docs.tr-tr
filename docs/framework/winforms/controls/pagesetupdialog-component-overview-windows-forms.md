---
title: PageSetupDialog Bileşenine Genel Bakış (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- PageSetupDialog
helpviewer_keywords:
- Page Setup dialog box [Windows Forms], displaying
- PageSetupDialog component
ms.assetid: 791caacb-a5ca-4fca-bad9-1a5721ad697c
ms.openlocfilehash: 989183b6152dfccb6167d89433317cea596d83c5
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211737"
---
# <a name="pagesetupdialog-component-overview-windows-forms"></a>PageSetupDialog Bileşenine Genel Bakış (Windows Forms)

Windows Forms <xref:System.Windows.Forms.PageSetupDialog> sayfa ayrıntıları yazdırma için Windows tabanlı uygulamalar ayarlamak için kullanılan bir önceden yapılandırılmış bir iletişim kutusu bir bileşendir. Windows tabanlı uygulamanızda basit bir çözüm olarak kullanıcılar yerine kendi iletişim kutusu yapılandırma sayfası tercihleri ayarlamak için kullanın. Kenarlık ve kenar boşluğu ayarlamaları, üstbilgiler, altbilgiler ve dikey veya yatay hizalama ayarlamak kullanıcıların etkinleştirebilirsiniz. Standart Windows iletişim kutularında bağlı olarak, temel işlevleri kullanıcılarına hemen tanıdık uygulamalar oluşturun.

## <a name="key-properties-and-methods"></a>Anahtar özellikleri ve yöntemleri

Kullanım <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> çalışma zamanında iletişim kutusunu görüntülemek için yöntemi. Bu bileşen için ya da tek bir sayfayla ilişkili ayarlayabileceğiniz özelliklerine sahip (<xref:System.Drawing.Printing.PrintDocument> sınıfı) veya herhangi bir belge (<xref:System.Drawing.Printing.PageSettings> sınıfı). Ayrıca, <xref:System.Windows.Forms.PageSetupDialog> bileşeni, depolanmış belirli bir yazıcı ayarlarını belirlemek için kullanılabilir <xref:System.Drawing.Printing.PrinterSettings> sınıfı.

Bir forma eklendiğinde <xref:System.Windows.Forms.PageSetupDialog> bileşeni Tepsi Visual Studio'da Windows Form Tasarımcısı'nın altındaki görünür.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.PageSetupDialog>
- [PageSetupDialog bileşeni](pagesetupdialog-component-windows-forms.md)
