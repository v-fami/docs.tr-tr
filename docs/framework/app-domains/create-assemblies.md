---
title: Derlemeler Oluşturma
ms.date: 03/30/2017
helpviewer_keywords:
- assemblies [.NET Framework], multifile
- single-file assemblies
- assemblies [.NET Framework], creating
- multifile assemblies
ms.assetid: 54832ee9-dca8-4c8b-913c-c0b9d265e9a4
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3a8b6c37df398b7273bfcf082def572d4d0e7d87
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65634524"
---
# <a name="creating-assemblies"></a>Derlemeler Oluşturma

Visual Studio gibi bir IDE kullanarak tek dosya veya çok dosyalı derlemeler oluşturabilir veya derleyiciler ve araçlar sağlayan [!INCLUDE[winsdklong](../../../includes/winsdklong-md.md)]. Basit, basit bir ada sahip ve tek bir uygulama etki alanına yüklü olduğu tek bir dosyaya derlemesidir. Bu derleme, uygulama dizininin dışındaki diğer derlemeler tarafından başvurulamaz ve sürüm denetimi yapmak değil. Derlemenin oluşan uygulamayı kaldırmak için basitçe bulunduğu dizini silin. Birçok geliştirici için bu özelliklere sahip bir derleme bir uygulamayı dağıtmak için gereken şey.

Birkaç kod modülleri ve kaynak dosyalarını, bir çoklu dosya derlemesi oluşturabilirsiniz. Birden çok uygulama tarafından paylaşılabilen bir derlemeyi de oluşturabilirsiniz. Paylaşılan bir derleme tanımlayıcı bir ada sahip olmalıdır ve genel derleme önbelleğinde dağıtılabilir.

Derlemeler, aşağıdaki etkenlere bağlı olarak içine kod modülleri ve kaynakları gruplama birkaç seçeneğiniz vardır:

- Sürüm Oluşturma

     Grup modüller aynı sürüm bilgisini içermelidir.

- Dağıtım

     Grup kod modülleri ve modelinizin dağıtımı destekleyen kaynaklar.

- Yeniden kullanma

     Bunlar mantıksal olarak birlikte bazı amaç için kullanılabiliyorsa modülleri gruplandırın. Örneğin, aynı derlemede türlerin ve sınıfların program bakımı için kullanılmayan oluşan bir derleme içine yerleştirilebilir. Ayrıca, birden çok uygulama ile paylaşmak için istediğinize türleri bir derlemeye gruplandırılmasını ve derlemeyi bir güçlü ad ile imzalanması gerekir.

- Güvenlik

     Aynı güvenlik izinleri gerektiren türler içeren Grup modüller.

- Kapsam belirleme

     Görünürlüğü aynı derlemeye sınırlandırılmalıdır türleri içeren Grup modüllerinin.

Özel durumlar, ortak dil çalışma zamanı derlemeleri yönetilmeyen COM uygulamalarına yaparken yapılmalıdır. Yönetilmeyen kod ile çalışma hakkında daha fazla bilgi için bkz. [.NET Framework bileşenlerini COM'da gösterme](../../../docs/framework/interop/exposing-dotnet-components-to-com.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Bütünleştirilmiş Kodlarla Programlama](../../../docs/framework/app-domains/programming-with-assemblies.md)
- [Bütünleştirilmiş Kod Sürümü Oluşturma](../../../docs/framework/app-domains/assembly-versioning.md)
- [Nasıl yapılır: Tek Dosyalı bütünleştirilmiş kod derleme](../../../docs/framework/app-domains/how-to-build-a-single-file-assembly.md)
- [Nasıl yapılır: Bir çoklu dosya derlemesi oluşturun](../../../docs/framework/app-domains/how-to-build-a-multifile-assembly.md)
- [Çalışma Zamanının Bütünleştirilmiş Kodların Konumunu Bulması](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
- [Çok Dosyalı Bütünleştirilmiş Kodlar](../../../docs/framework/app-domains/multifile-assemblies.md)
