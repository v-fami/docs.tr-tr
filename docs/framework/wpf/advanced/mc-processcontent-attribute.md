---
title: mc:ProcessContent Özniteliği
ms.date: 03/30/2017
helpviewer_keywords:
- mc:ProcessContent attribute
- XAML [WPF], mc:ProcessContent attribute
ms.assetid: 2689b2c8-b4dc-4b71-b9bd-f95e619122d7
ms.openlocfilehash: 865b1a3ccc30ff5efab4b08956bf7ba2bba4769c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62017909"
---
# <a name="mcprocesscontent-attribute"></a>mc:ProcessContent Özniteliği
Belirten [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] öğeleri hala olmalıdır içeriği ilgili üst öğeler tarafından işlenen en yakın üst öğe tarafından gözardı edilebilir olsa bile bir [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] belirtme nedeniyle İşlemci [mc: Ignorable özniteliği](mc-ignorable-attribute.md) . `mc:ProcessContent` Özniteliği işaretleme uyumluluk destekler ve özel ad alanı eşlemesi için [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] sürüm oluşturma.  
  
## <a name="xaml-attribute-usage"></a>XAML Öznitelik Kullanımı  
  
```  
<object  
  xmlns:ignorablePrefix="ignorableUri"  
  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"  
  mc:Ignorable="ignorablePrefix"...  
  mc:ProcessContent="ignorablePrefix:ThisElementCanBeIgnored"  
>  
    <ignorablePrefix:ThisElementCanBeIgnored>  
        [content]  
    </ignorablePrefix:ThisElementCanBeIgnored>  
</object>  
```  
  
## <a name="xaml-values"></a>XAML Değerleri  
  
|||  
|-|-|  
|*ignorablePrefix*|XML 1.0 belirtimi başına herhangi geçerli bir önek dizesi.|  
|*ignorableUri*|XML 1.0 belirtimi başına bir ad atamak için geçerli bir URI.|  
|*ThisElementCanBeIgnored*|Tarafından göz ardı edilebilir öğenin [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] işlemcisi uygulamaları, temel alınan türü çözümlenemiyor.|  
|*[content]*|*ThisElementCanBeIgnored* yoksayılabilir olarak işaretlenir. Bu öğe işlemci yoksayar, *[content]* tarafından işlenen *nesne*.|  
  
## <a name="remarks"></a>Açıklamalar  
 Varsayılan olarak, bir [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] işlemci yoksayılan öğe içindeki içeriği yoksayar. Belirli bir öğeyi belirtebilirsiniz `mc:ProcessContent`ve [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] işlemci yoksayılan öğe içinde içerik işlemeye devam eder. İçeriği en az biri Ignorable olan ve en az biri Ignorable değil birkaç etiket içinde iç içe ise, bu genellikle kullanılmaz.  
  
 Alan ayırıcı, örneğin kullanarak özniteliğinde birden çok ön ekleri belirtilebilir: `mc:ProcessContent="ignore:Element1 ignore:Element2"`.  
  
 [!INCLUDE[TLA#tla_mcxmlnsv1](../../../../includes/tlasharptla-mcxmlnsv1-md.md)] Diğer öğeleri ve bu alanı içinde belgelenmeyen öznitelikleri ad alanını tanımlayan [!INCLUDE[TLA#tla_sdk](../../../../includes/tlasharptla-sdk-md.md)]. Daha fazla bilgi için [XML işaretleme Uyumluluk Belirtimi](https://go.microsoft.com/fwlink/?LinkId=73824).  
  
## <a name="see-also"></a>Ayrıca bkz.

- [mc:Ignorable Özniteliği](mc-ignorable-attribute.md)
- [XAML'ye Genel Bakış (WPF)](xaml-overview-wpf.md)
