---
title: .NET Core'a taşıma araçları
description: .NET Core için bağlantı noktası için kullanabileceğiniz araçlardan bazıları hakkında bilgi edinin
author: cartermp
ms.author: mairaw
ms.date: 12/07/2018
ms.openlocfilehash: d0b74b5708f31922b72fa0e236c8bbe69ae06217
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65632245"
---
# <a name="tools-to-help-with-porting-to-net-core"></a>.NET Core'a taşıma ile yardımcı olacak araçlar

Bu makale faydalı taşırken listelenen araçlar bulabilirsiniz:

* [.NET portability Analyzer](../../standard/analyzers/portability-analyzer.md), nasıl taşınabilir kod .NET Framework ve .NET Core arasında olan bir rapor oluşturabilen bir araç zinciri:  Olarak bir [komut satırı aracını](https://github.com/Microsoft/dotnet-apiport/releases) olarak bir [Visual Studio uzantısı](https://visualstudiogallery.msdn.microsoft.com/1177943e-cfb7-4822-a8a6-e56c7905292b)
* [.NET API Çözümleyicisi](../../standard/analyzers/api-analyzer.md) -olası uyumluluk bulur bir Roslyn çözümleyicinizi risklerini için C# farklı platformlarda API'leri ve kullanım dışı API'lere giden çağrıların algılar.

Ayrıca, bağlantı noktası daha küçük çözümleri veya .NET Core proje dosyası biçimi ile tek tek projelere deneyebilirsiniz [CsprojToVs2017](https://github.com/hvanbakel/CsprojToVs2017) aracı.

> [!WARNING] 
> CsprojToVs2017 üçüncü taraf bir araçtır. Tüm projeleriniz için çalışacak bir garanti yoktur ve ince değişiklikler, bağımlı davranış neden. CsprojToVs2017 olarak kullanılmalıdır bir _başlangıç noktası_ otomatikleştirilebilir temel işlemleri otomatikleştirir. Bu geçişi proje dosya biçimleri için garantili bir çözüm değildir.
