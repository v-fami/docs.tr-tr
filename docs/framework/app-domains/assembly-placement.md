---
title: Derleme Yerleştirme
ms.date: 03/30/2017
helpviewer_keywords:
- <codeBase> element
- locating assemblies
- assemblies [.NET Framework], placement
- assemblies [.NET Framework], location
ms.assetid: ff8d48bc-f606-484f-9fe1-d0af264269fb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a9b8357be5b9f49569114cbc1c2942eea03696eb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61675331"
---
# <a name="assembly-placement"></a>Derleme Yerleştirme
Çoğu .NET Framework uygulaması için, uygulamayı oluşturan derlemeleri uygulama dizininde, uygulama dizininin bir alt dizininde veya genel derleme önbelleğinde (derleme paylaşılıyorsa) bulursunuz. Ortak dil çalışma zamanı kullanarak bir derleme için nerede arar kılabilirsiniz [ \<codeBase > öğesi](../../../docs/framework/configure-apps/file-schema/runtime/codebase-element.md) bir yapılandırma dosyası. Derlemeyi kullanarak belirtilen konum tanımlayıcı bir ada sahip değilse [ \<codeBase > öğesi](../../../docs/framework/configure-apps/file-schema/runtime/codebase-element.md) uygulama dizini veya bir alt dizine sınırlıdır. Derlemeyi tanımlayıcı bir ada sahipse [ \<codeBase > öğesi](../../../docs/framework/configure-apps/file-schema/runtime/codebase-element.md) bilgisayarda veya bir ağ üzerinde herhangi bir konum belirtebilirsiniz.  
  
 Yönetilmeyen kod veya COM ile birlikte çalışma uygulamaları için derleme bulurken de benzer kurallar geçerlidir: Derleme birden çok uygulama tarafından paylaşılacaksa, genel derleme önbelleğine yüklenmelidir. Yönetilmeyen kodla kullanılan derlemeler, bir tür kitaplığı olarak dışarı aktarılmalı ve kaydedilmelidir. COM ile birlikte çalışma tarafından kullanılan derlemeler kataloğa kaydedilmelidir, ancak bazı durumlarda bu kayıt otomatik olarak gerçekleşir.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Çalışma Zamanının Bütünleştirilmiş Kodların Konumunu Bulması](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
- [Uygulamaları Yapılandırma](../../../docs/framework/configure-apps/index.md)
- [Yönetilmeyen kod ile birlikte çalışma](../../../docs/framework/interop/index.md)
- [Ortak Dil Çalışma Zamanı Modülündeki Bütünleştirilmiş Kodlar](../../../docs/framework/app-domains/assemblies-in-the-common-language-runtime.md)
