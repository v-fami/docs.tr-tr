---
title: ColorConvertedBitmap Biçimlendirme Uzantısı
ms.date: 03/30/2017
helpviewer_keywords:
- XAML [WPF], ColorConvertedBitmap markup extension
- ColorConvertedBitmap markup extension [WPF]
ms.assetid: 18321c18-c898-4470-93fa-a702b47770c1
ms.openlocfilehash: e8a36a1b8592146eb2474805638cdc3697adb0c4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62010663"
---
# <a name="colorconvertedbitmap-markup-extension"></a>ColorConvertedBitmap Biçimlendirme Uzantısı
Katıştırılmış bir profili olmayan bir bit eşlem kaynağını belirtmek için bir yol sağlar. Renk bağlamları / tarafından belirtilen profilleri [!INCLUDE[TLA2#tla_uri](../../../../includes/tla2sharptla-uri-md.md)], görüntü kaynağı olarak [!INCLUDE[TLA2#tla_uri](../../../../includes/tla2sharptla-uri-md.md)].  
  
## <a name="xaml-attribute-usage"></a>XAML Öznitelik Kullanımı  
  
```xml  
<object property="{ColorConvertedBitmap imageSource sourceIIC destinationIIC}" .../>  
```  
  
## <a name="xaml-values"></a>XAML Değerleri  
  
|||  
|-|-|  
|`imageSource`|[!INCLUDE[TLA2#tla_uri](../../../../includes/tla2sharptla-uri-md.md)] Kullanıp bit eşlemin.|  
|`sourceIIC`|[!INCLUDE[TLA2#tla_uri](../../../../includes/tla2sharptla-uri-md.md)] Kaynak profili yapılandırması.|  
|`destinationIIC`|[!INCLUDE[TLA2#tla_uri](../../../../includes/tla2sharptla-uri-md.md)] Hedef profili yapılandırma|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu işaretleme uzantısı gibi bir dizi görüntü kaynağı özellik değerleri doldurmak için hedeflenen <xref:System.Windows.Media.Imaging.BitmapImage.UriSource%2A>.  
  
 Öznitelik sözdizimi, bu işaretleme uzantısı ile kullanılan en yaygın sözdizimidir. `ColorConvertedBitmap` (veya `ColorConvertedBitmapExtension`) özellik öğesi sözdizimine kullanılamaz çünkü değerleri yalnızca değerleri dize ilk oluşturucu üzerinde ayarlanabilir uzantı tanımlayıcısı şu.  
  
 `ColorConvertedBitmap` bir işaretleme uzantısıdır. Biçimlendirme uzantıları, genellikle öznitelik değerlerinin değişmez değerler veya işleyici isimleri dışına çıkma gereksinimi olduğunda ve bu gereksinim, belirli türler veya özellikler üzerine tür dönüştürücülerini koymaktan daha genel olduğunda uygulanır. İçindeki tüm biçimlendirme uzantıları [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] kullanmak {ve} kuralına göre kendi öznitelik sözdizimi içinde karakterler bir [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] işlemcisinin bir işaretleme uzantısı özniteliği işlemesi gerekir. Daha fazla bilgi için [biçimlendirme uzantıları ve WPF XAML](markup-extensions-and-wpf-xaml.md).  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Media.Imaging.BitmapImage.UriSource%2A>
- [İşaretleme Uzantıları ve WPF XAML](markup-extensions-and-wpf-xaml.md)
- [Görüntülemeye Genel Bakış](../graphics-multimedia/imaging-overview.md)
