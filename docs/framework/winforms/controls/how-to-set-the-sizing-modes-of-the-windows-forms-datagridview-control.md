---
title: 'Nasıl yapılır: Windows Forms DataGridView Denetiminin Boyutlandırma Modlarını Ayarlama'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], setting sizing modes
- DataGridView control [Windows Forms], sizing modes
ms.assetid: e9ad15e6-b4bb-44aa-a767-3738e9db1651
ms.openlocfilehash: 76d71a7c3c37f53854cf4fd9c6d8300831572d51
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65591636"
---
# <a name="how-to-set-the-sizing-modes-of-the-windows-forms-datagridview-control"></a>Nasıl yapılır: Windows Forms DataGridView Denetiminin Boyutlandırma Modlarını Ayarlama
Aşağıdaki yordamlarda, özelleştirme veya boyutlandırma seçenekleri için birleştirme bazı yaygın senaryolar gösterilmektedir <xref:System.Windows.Forms.DataGridView> denetimi ve bir denetiminde özel sütunlar için.  
  
### <a name="to-create-a-fixed-width-column"></a>Sabit genişlikte sütun oluşturmak için  
  
- Ayarlama <xref:System.Windows.Forms.DataGridViewColumn.AutoSizeMode%2A> özelliğini <xref:System.Windows.Forms.DataGridViewAutoSizeColumnMode.None>, <xref:System.Windows.Forms.DataGridViewColumn.Resizable%2A> özelliğini <xref:System.Windows.Forms.DataGridViewTriState.False>, <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A> özelliğini `true`ve <xref:System.Windows.Forms.DataGridViewColumn.Width%2A> özelliğini uygun bir değer.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewSizingScenarios#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSizingScenarios/CS/sizingscenarios.cs#10)]
     [!code-vb[System.Windows.Forms.DataGridViewSizingScenarios#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSizingScenarios/vb/sizingscenarios.vb#10)]  
  
### <a name="to-create-a-column-that-adjusts-its-size-to-fit-its-content"></a>İçeriği sığdırmak için boyutunu ayarlayan bir sütun oluşturmak için  
  
- Ayarlama <xref:System.Windows.Forms.DataGridViewColumn.AutoSizeMode%2A> bir içerik tabanlı boyutlandırma modunu özelliği.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewSizingScenarios#20](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSizingScenarios/CS/sizingscenarios.cs#20)]
     [!code-vb[System.Windows.Forms.DataGridViewSizingScenarios#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSizingScenarios/vb/sizingscenarios.vb#20)]  
  
### <a name="to-create-fill-mode-columns-for-values-of-varying-size-and-importance"></a>Değişen boyutunu ve önem derecesi değerlerini dolgu modunu sütunları oluşturmak için  
  
- Ayarlama <xref:System.Windows.Forms.DataGridView.AutoSizeColumnsMode%2A?displayProperty=nameWithType> özelliğini <xref:System.Windows.Forms.DataGridViewAutoSizeColumnsMode.Fill> bu değeri geçersiz kılmaz tüm sütunlar için boyutlandırma modunu ayarlamak için. Ayarlama <xref:System.Windows.Forms.DataGridViewColumn.FillWeight%2A> özellikler için kendi ortalama orantılı olan değerleri sütun genişliklerini içerik. Ayarlama <xref:System.Windows.Forms.DataGridViewColumn.MinimumWidth%2A> kısmi içerik görüntüsü emin olmak için önemli sütunların özellikleri.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewSizingScenarios#30](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSizingScenarios/CS/sizingscenarios.cs#30)]
     [!code-vb[System.Windows.Forms.DataGridViewSizingScenarios#30](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSizingScenarios/vb/sizingscenarios.vb#30)]  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği, bu konuda açıklanan boyutlandırma seçenekleri anlamanıza yardımcı olabilecek bir uygulama sağlar.  
  
 [!code-csharp[System.Windows.Forms.DataGridViewSizingScenarios#00](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSizingScenarios/CS/sizingscenarios.cs#00)]
 [!code-vb[System.Windows.Forms.DataGridViewSizingScenarios#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewSizingScenarios/vb/sizingscenarios.vb#00)]  
  
 Bu Tanıtım uygulamasını kullanmak için:  
  
- Formun boyutunu değiştirin. Oranlarını koruma tarafından gösterilen sırada dolgu modunu sütun genişliklerini nasıl değiştiğini gözlemlersiniz <xref:System.Windows.Forms.DataGridViewColumn.FillWeight%2A> özellik değerleri. Bir sütunu nasıl 's gözlemleyin <xref:System.Windows.Forms.DataGridViewColumn.MinimumWidth%2A> form çok küçük olduğunda değiştirmesini engeller.  
  
- Fare ile sütun ayırıcılarını sürükleyerek sütunu boyutları değiştirin. Bazı sütunları yeniden boyutlandırılan ve nasıl yeniden boyutlandırılabilir nasıl olamaz gözlemleyin sütunları yapılamıyor en düşük genişliklerini dar.  
  
## <a name="compiling-the-code"></a>Kod Derleniyor  
 Bu örnek gerektirir:  
  
- Sistem ve System.Windows.Forms öğelerini derlemelerine başvurular.  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn.AutoSizeMode%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewAutoSizeColumnMode>
- <xref:System.Windows.Forms.DataGridViewColumn.Resizable%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.Width%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.FillWeight%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.MinimumWidth%2A?displayProperty=nameWithType>
