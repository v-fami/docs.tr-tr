---
title: .NET Framework ile Birden Çok Platform için Geliştirme
ms.date: 07/18/2018
ms.technology: dotnet-standard
ms.assetid: b153baaa-130c-4169-860b-e580591de91e
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c2167f74c5d1dd9f49995b6407e65feb474084dc
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65641431"
---
# <a name="developing-for-multiple-platforms-with-the-net-framework"></a>.NET Framework ile Birden Çok Platform için Geliştirme

.NET Framework ve Visual Studio kullanarak, hem Microsoft hem de Microsoft olmayan platformlar için uygulamaları geliştirebilirsiniz.
  
## <a name="options-for-cross-platform-development"></a>Platformlar arası geliştirme için seçenekleri

[!INCLUDE[standard](../../../includes/pcl-to-standard.md)]
  
 Birden çok platform için geliştirme için kaynak kodu veya ikili dosyaları paylaşabilir ve .NET Framework kodu ve Windows çalışma zamanı API'ları arasındaki çağrıları yapabilir.  
  
|İsterseniz...|Kullan...|  
|-----------------------|------------|  
|Windows Phone 8.1 ve Windows 8.1 uygulamalar arasında kaynak kodu paylaşmak|**Paylaşılan projeleri** (Evrensel uygulamaları şablonu Visual Studio 2013 Update 2).<br /><br /> -Şu anda hiçbir Visual Basic desteği.<br /># Kullanarak-platforma özgü kod ayırabilirsiniz`if` deyimleri.<br /><br /> Ayrıntılar için bkz:<br /><br /> -   [Kodlamaya başlayın](/windows/uwp/get-started/create-uwp-apps)<br />-   [Evrensel XAML uygulamaları oluşturmak için Visual Studio kullanarak](https://devblogs.microsoft.com/visualstudio/using-visual-studio-to-build-universal-xaml-apps/) (blog gönderisi)<br />-   [XAML yakınsanmış uygulamalar oluşturmak için Visual Studio kullanarak](https://channel9.msdn.com/Events/Build/2014/3-591) (video)|  
|İkili dosyalar farklı platformları hedefleyen uygulamalar arasında paylaşma|**Taşınabilir sınıf kitaplığı projeleri** platformdan kod için.<br /><br /> -Bu yaklaşım genellikle iş mantığını uygulayan kodu için kullanılır.<br />-Visual Basic veya C# kullanabilirsiniz.<br />-API desteği, platforma göre değişiklik gösterir.<br />-Windows 8.1 ve Windows Phone 8.1 hedefleyen taşınabilir sınıf kitaplığı projeleri, Windows çalışma zamanı API'ları ve XAML destekler. Bu özellikler, taşınabilir Sınıf Kitaplığı'nın eski sürümlerinde kullanılamaz.<br />-Gerekli olursa, arabirimler veya soyut sınıflar kullanarak platforma özgü kodu soyut.<br /><br /> Ayrıntılar için bkz:<br /><br /> -   [Taşınabilir sınıf kitaplığı](cross-platform-development-with-the-portable-class-library.md)<br />-   [Sizin için taşınabilir sınıf kitaplıkları iş yapmak için nasıl](https://blogs.msdn.microsoft.com/dsplaisted/2012/08/27/how-to-make-portable-class-libraries-work-for-you/) (blog gönderisi)<br />-   [MVVM ile taşınabilir sınıf kitaplığı kullanma](using-portable-class-library-with-model-view-view-model.md) <br />-   [Birden çok platformu hedefleyen kitaplıklar için uygulama kaynakları](app-resources-for-libraries-that-target-multiple-platforms.md) <br />-   [.NET portability Analyzer](https://marketplace.visualstudio.com/items?itemName=ConnieYau.NETPortabilityAnalyzer) (Visual Studio uzantısı)|  
|Windows 8.1 dışındaki platformlara yönelik uygulamalar ve Windows Phone 8.1 arasında kaynak kod paylaşma|**Bağlantı olarak ekleme** özelliği.<br /><br /> -Bu yaklaşım, her iki uygulama için ortak ancak yok taşınabilirlik, herhangi bir nedenden dolayı uygulama mantığı için uygundur. Bu özellik, C# veya Visual Basic kodu için kullanabilirsiniz.<br />     Örneğin, Windows Phone 8 ve Windows 8, Windows çalışma zamanı API'leri paylaşın, ancak taşınabilir sınıf kitaplıkları, bu platformlar için Windows çalışma zamanı desteklemez. Kullanabileceğiniz `Add as link` bir Windows Phone 8 uygulaması ve Windows 8'i hedefleyen bir Windows Store uygulaması arasında ortak Windows çalışma zamanı kod paylaşmak için.<br /><br /> Ayrıntılar için bkz:<br /><br /> -   [Bağlantı olarak Ekle ile kod paylaşın](https://docs.microsoft.com/previous-versions/windows/apps/jj714082(v=vs.105))<br />-   [Nasıl Yapılır: Bir projeye var olan öğeleri Ekle](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100))|  
|Windows Store uygulamaları .NET Framework kullanarak yazmak veya .NET Framework kodundan Windows çalışma zamanı API'leri çağırma|**Windows çalışma zamanı API'ları** .NET Framework C# veya Visual Basic kod ve Windows Store apps oluşturmak için .NET Framework'ü kullanın. API farklılıkları iki platform arasında farkında olmalıdır. Ancak, bu farklılıkları ile çalışmanıza yardımcı olmak için sınıflar uygulanır.<br /><br /> Ayrıntılar için bkz:<br /><br /> -   [Windows Store uygulamaları ve Windows çalışma zamanı için .NET framework desteği](support-for-windows-store-apps-and-windows-runtime.md) <br />-   [Windows çalışma zamanı için bir URI'yı geçirme](passing-a-uri-to-the-windows-runtime.md) <br />-   <xref:System.IO.WindowsRuntimeStreamExtensions><br />-    <xref:System.WindowsRuntimeSystemExtensions>|  
|Microsoft olmayan platformlar için .NET Framework uygulamaları oluşturun|**Taşınabilir sınıf kitaplığı başvuru bütünleştirilmiş kodları** .NET Framework ve Xamarin gibi bir Visual Studio uzantısı ya da üçüncü taraf araç.<br /><br /> Ayrıntılar için bkz:<br /><br /> -   [Taşınabilir sınıf kitaplığı tüm platformlarda kullanıma sunuldu.](https://devblogs.microsoft.com/dotnet/portable-class-library-pcl-now-available-on-all-platforms/) (blog gönderisi)<br />-   [Xamarin belgeleri](/xamarin)|  
|JavaScript ve HTML platformlar arası geliştirme için kullanın|**Evrensel uygulama şablonları** Visual Studio 2013 güncelleştirme 2, Windows 8.1 ve Windows Phone 8.1 için Windows çalışma zamanı API'leri karşı geliştirmek için. Şu anda, JavaScript ve HTML .NET Framework API'ları ile platformlar arası uygulamalar geliştirmek için kullanamazsınız.<br /><br /> Ayrıntılar için bkz:<br /><br /> -   [JavaScript proje şablonları](https://docs.microsoft.com/previous-versions/windows/apps/hh758331%28v=win.10%29)<br />-   [Windows Phone için JavaScript kullanarak bir Windows çalışma zamanı uygulama taşıma](https://docs.microsoft.com/previous-versions/windows/apps/dn636144%28v=win.10%29)|
