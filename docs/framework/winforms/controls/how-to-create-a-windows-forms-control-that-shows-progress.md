---
title: 'Nasıl yapılır: İlerleme Durumunu Gösteren Windows Forms Denetimi Oluşturma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [Windows Forms], progress tracking
- controls [Windows Forms], creating
- progress [Windows Forms], reporting [Windows Forms]
- FlashTrackBar custom control
ms.assetid: 24c5a2e3-058c-4b8d-a217-c06e6a130c2f
ms.openlocfilehash: 877df5139fd0e626cd2242e3790bc7100f6233aa
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64599337"
---
# <a name="how-to-create-a-windows-forms-control-that-shows-progress"></a>Nasıl yapılır: İlerleme Durumunu Gösteren Windows Forms Denetimi Oluşturma
Aşağıdaki kod örneğinde adlı özel bir denetimi gösterir `FlashTrackBar` kullanıcı düzeyi veya bir uygulamanın ilerleme durumunu göstermek için kullanılabilir. Gradyan ilerlemesini görsel olarak göstermek için kullanır.  
  
 `FlashTrackBar` Denetimi aşağıdaki kavramları göstermektedir:  
  
- Özel özellikler tanımlama.  
  
- Özel olaylar tanımlama. (`FlashTrackBar` tanımlar `ValueChanged` olay.)  
  
- Geçersiz kılma <xref:System.Windows.Forms.Control.OnPaint%2A> denetimi çizmek için mantığını sağlamak için yöntemi.  
  
- Alan kullanan denetimi çizmek için kullanılabilir bilgi işlem, <xref:System.Windows.Forms.Control.ClientRectangle%2A> özelliği. `FlashTrackBar` bunu yapar, `OptimizedInvalidate` yöntemi.  
  
- Windows Form Tasarımcısı'nda değiştirildiğinde serileştirme veya Kalıcılık bir özellik için uygulama. `FlashTrackBar` tanımlar `ShouldSerializeStartColor` ve `ShouldSerializeEndColor` serileştirmeye yönelik yöntemleri kendi `StartColor` ve `EndColor` özellikleri.  
  
 Tarafından tanımlanan özel özellikler aşağıdaki tabloda gösterilmektedir `FlashTrackBar`.  
  
|Özellik|Açıklama|  
|--------------|-----------------|  
|`AllowUserEdit`|Kullanıcının tıklatarak ve sürükleyerek flash izleme çubuğu değerini değiştirip değiştiremeyeceğini belirtir.|  
|`EndColor`|İzleme çubuğu Bitiş rengini belirtir.|  
|`DarkenBy`|Ne kadar arka planda ön plan gradyan göre koyu belirtir.|  
|`Max`|İzleme çubuğu en büyük değerini belirtir.|  
|`Min`|İzleme çubuğu en küçük değerini belirtir.|  
|`StartColor`|Gradyan başlangıç rengi belirtir.|  
|`ShowPercentage`|Gradyan yüzde görüntülenip görüntülenmeyeceğini gösterir.|  
|`ShowValue`|Geçerli değer geçişin görüntülenip görüntülenmeyeceğini gösterir.|  
|`ShowGradient`|İzleme çubuğu geçerli değerini gösteren bir renk gradyanı görüntülemesi gerekip gerekmediğini gösterir.|  
|-   `Value`|İzleme çubuğu geçerli değerini belirtir.|  
  
 Aşağıdaki tablo diğer üyeleri tarafından tanımlanan gösterir `FlashTrackBar:` özellik değişti olayı ve olayı başlatan yöntem.  
  
|Üye|Açıklama|  
|------------|-----------------|  
|`ValueChanged`|Olay arandığında `Value` çubuğu değişiklikleri izleme özelliği.|  
|`OnValueChanged`|Başlatan yöntem `ValueChanged` olay.|  
  
> [!NOTE]
>  `FlashTrackBar` kullanan <xref:System.EventArgs> olay veri sınıfı ve <xref:System.EventHandler> olay temsilci için.  
  
 Buna karşılık gelen işlemek için *EventName* olayları `FlashTrackBar` devraldığı aşağıdaki yöntemleri geçersiz kılan <xref:System.Windows.Forms.Control?displayProperty=nameWithType>:  
  
- <xref:System.Windows.Forms.Control.OnPaint%2A>  
  
- <xref:System.Windows.Forms.Control.OnMouseDown%2A>  
  
- <xref:System.Windows.Forms.Control.OnMouseMove%2A>  
  
- <xref:System.Windows.Forms.Control.OnMouseUp%2A>  
  
- <xref:System.Windows.Forms.Control.OnResize%2A>  
  
 Karşılık gelen özellik değişti olayları işlemek için `FlashTrackBar` devraldığı aşağıdaki yöntemleri geçersiz kılan <xref:System.Windows.Forms.Control?displayProperty=nameWithType>:  
  
- <xref:System.Windows.Forms.Control.OnBackColorChanged%2A>  
  
- <xref:System.Windows.Forms.Control.OnBackgroundImageChanged%2A>  
  
- <xref:System.Windows.Forms.Control.OnTextChanged%2A>  
  
## <a name="example"></a>Örnek  
 `FlashTrackBar` Denetimi tanımlayan iki kullanıcı Arabirimi tür düzenleyicileri `FlashTrackBarValueEditor` ve `FlashTrackBarDarkenByEditor`, aşağıdaki kod listelerinde gösterilir. `HostApp` Sınıfının kullandığı `FlashTrackBar` bir Windows formunda denetimi.  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#1)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#1)]  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBarDarkenByEditor.cs#10)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBarDarkenByEditor.vb#10)]  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#20](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBarValueEditor.cs#20)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBarValueEditor.vb#20)]  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#30](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/HostApp.cs#30)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#30](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/HostApp.vb#30)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Tasarım zamanı desteği sunma](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120))
- [Windows Forms Denetimi Geliştirmenin Esasları](windows-forms-control-development-basics.md)
