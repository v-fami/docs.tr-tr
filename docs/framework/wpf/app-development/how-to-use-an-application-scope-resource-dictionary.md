---
title: 'Nasıl yapılır: Uygulama Kapsamı Kaynak Sözlüğü Kullanma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- dictionaries [WPF], resource
- resource dictionaries [WPF], application-scope
- application-scope resource dictionaries
ms.assetid: 53857682-bd2c-4f2c-8f25-1307d0b451a2
ms.openlocfilehash: 589e28b3c05496e3fc17055b98240e389faed068
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62007493"
---
# <a name="how-to-use-an-application-scope-resource-dictionary"></a>Nasıl yapılır: Uygulama Kapsamı Kaynak Sözlüğü Kullanma
Bu örnekte, tanımlamak ve bir özel uygulama kapsamı kaynak sözlüğü kullanma gösterilmektedir.  
  
## <a name="example"></a>Örnek  
 <xref:System.Windows.Application> Paylaşılan kaynaklar için bir uygulama kapsamı store kullanıma sunar: <xref:System.Windows.Application.Resources%2A>. Varsayılan olarak, <xref:System.Windows.Application.Resources%2A> örneği ile özelliğinin başlatıldığı <xref:System.Windows.ResourceDictionary> türü. Almanıza ve ayarlamanıza, uygulama kapsamı özelliklerini kullanarak, bu örneği kullanmak <xref:System.Windows.Application.Resources%2A>. Daha fazla bilgi için [nasıl yapılır: GET ve Set uygulama kapsamı kaynak](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/aa348547(v=vs.100)).
  
 Kullanılarak ayarlanan birden fazla kaynak varsa <xref:System.Windows.Application.Resources%2A>, bunun yerine özel bir kaynak sözlüğü bu kaynakları saklamak ve ayarlamak için kullanabileceğiniz <xref:System.Windows.Application.Resources%2A> onunla yerine. XAML kullanarak bir özel kaynak sözlüğü bildirdiğiniz nasıl gösterir.
  
 [!code-xaml[HOWTOResourceDictionaries#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/MyResourceDictionary.xaml#1)]  
  
 Kullanarak tüm kaynak sözlüklerini takas <xref:System.Windows.Application.Resources%2A> uygulama kapsamı Temalar desteklemek, burada her teması saklanmış olduğu tek bir kaynak sözlüğü sağlar. Aşağıdaki örnek nasıl ayarlanacağını gösterir <xref:System.Windows.ResourceDictionary>.  
  
 [!code-xaml[HOWTOResourceDictionaries#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/App.xaml#2)]  
  
 Kaynak sözlüğünden tarafından kullanıma sunulan uygulama kapsamı kaynak nasıl alabileceğiniz aşağıdaki gösterilir <xref:System.Windows.Application.Resources%2A> XAML içinde.  
  
 [!code-xaml[HOWTOResourceDictionaries#4](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/MainWindow.xaml#4)]  
  
 Aşağıdaki nasıl da kaynak kodu alabilirsiniz gösterir.  
  
 [!code-csharp[HOWTOResourceDictionaries#3](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToResourceDictionaries/CSharp/MainWindow.xaml.cs#3)]
 [!code-vb[HOWTOResourceDictionaries#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToResourceDictionaries/VB/MainWindow.xaml.vb#3)]  
  
 Kullanırken yapmak için iki nokta vardır <xref:System.Windows.Application.Resources%2A>. İlk olarak, sözlük *anahtar* bir nesne olduğundan, bir özellik değerini alırken ve tam olarak aynı nesne örneğini kullanmanız gerekir. (Anahtar bir dize kullanarak büyük küçük harfe duyarlı olduğunu unutmayın.) İkincisi, sözlük *değer* bir nesne olduğundan, bir özellik değeri alınırken değeri istenen türe dönüştürmek gerekir.  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.ResourceDictionary>
- <xref:System.Windows.Application.Resources%2A>
- [XAML Kaynakları](../advanced/xaml-resources.md)
- [Birleştirilmiş Kaynak Sözlükleri](../advanced/merged-resource-dictionaries.md)
