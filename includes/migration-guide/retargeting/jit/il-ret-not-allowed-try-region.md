---
ms.openlocfilehash: 1687b1b9a1a6861f9569a0e29426de7f32ffc32b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62093618"
---
### <a name="il-ret-not-allowed-in-a-try-region"></a>IL ret deneyin bölgede izin verilmiyor

|   |   |
|---|---|
|Ayrıntılar|JIT64 tam zamanında derleyici, bir IL yönergesi bir try bölgede ret (.NET Framework 4. 6'içinde kullanılan) Ryujıt izin vermez. Bir try bölgeden döndüren ECMA-335 belirtimine göre izin verilmez ve bu tür IL bilinen hiçbir yönetilen derleyici oluşturur. Bununla birlikte, yansıma kullanarak oluşturulursa JIT64 derleyici böyle IL yürütecek gösterin.|
|Öneri|Bir uygulama bir try bölgede ret opcode içeren IL oluşturuyorsa, uygulama .NET Framework 4. 5'i eski JIT kullanın ve bu kesmesinden kaçınılmasını sağlar hedefleyebilir. Alternatif olarak, oluşturulan IL sonra deneyin bölge döndürmek için güncelleştirilebilir.|
|Kapsam|Kenar|
|Sürüm|4.6|
|Tür|Yeniden Hedefleme|
