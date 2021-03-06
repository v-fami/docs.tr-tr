---
title: 'Nasıl yapılır: Görsel Taslak Kullanmadan Özelliğe Animasyon Ekleme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- non-Storyboard animation
- local animation [WPF]
- animation [WPF], non-Storyboard (local)
ms.assetid: d411db70-4df7-487d-82bc-95a7c1b2e7f8
ms.openlocfilehash: 93609cdeb4d879cbec0f90096e4fa2c131a2ec5e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61761292"
---
# <a name="how-to-animate-a-property-without-using-a-storyboard"></a>Nasıl yapılır: Görsel Taslak Kullanmadan Özelliğe Animasyon Ekleme
Bu örnek, kullanmadan özelliğe animasyon uygulamak için bir yol gösterir. bir <xref:System.Windows.Media.Animation.Storyboard>.  
  
> [!NOTE]
>  Bu işlevselliği kullanıma sunulmadı [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)]. Bir özelliğe animasyon ekleme hakkında bilgi için [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], bkz: [görsel taslak kullanarak özelliğe animasyon ekleme](how-to-animate-a-property-by-using-a-storyboard.md).  
  
 Bir özellik için bir yerel animasyon uygulamak için kullanma <xref:System.Windows.UIElement.BeginAnimation%2A> yöntemi. Bu yöntem iki parametre alır: bir <xref:System.Windows.DependencyProperty> animasyon uygulamak için özellik ve bu özelliğe animasyon belirtir.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte, genişlik ve arka plan rengini animasyon ekleme işlemi gösterilmektedir bir <xref:System.Windows.Controls.Button>.  
  
 [!code-cpp[animateproperty#11](~/samples/snippets/cpp/VS_Snippets_Wpf/animateproperty/CPP/LocalAnimationExample.cpp#11)]
 [!code-csharp[animateproperty#11](~/samples/snippets/csharp/VS_Snippets_Wpf/animateproperty/CSharp/LocalAnimationExample.cs#11)]
 [!code-vb[animateproperty#11](~/samples/snippets/visualbasic/VS_Snippets_Wpf/animateproperty/VisualBasic/LocalAnimationExample.vb#11)]  
  
 Animasyon sınıfları çeşitli <xref:System.Windows.Media.Animation> ad mevcut özellikler farklı türde animasyon için. Özellikleri hakkında daha fazla bilgi için bkz. [animasyona genel bakış](animation-overview.md). Bağımlılık özellikleri (Bu örneklerde gösterilen özellikler türü) ve bunların özellikleri hakkında daha fazla bilgi için bkz. [bağımlılık özelliklerine genel bakış](../advanced/dependency-properties-overview.md).  
  
 Kullanmadan animasyon uygulamak için başka bir yöntemle <xref:System.Windows.Media.Animation.Storyboard> nesnelerini; daha fazla bilgi için [özellik Animasyon Tekniklerine Genel Bakış](property-animation-techniques-overview.md).  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Media.Animation.AnimationTimeline>
- <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A>
- <xref:System.Windows.Media.Animation>
- <xref:System.Windows.Media.Animation.Storyboard>
- [Özellik Animasyon Tekniklerine Genel Bakış](property-animation-techniques-overview.md)
- [Animasyona Genel bakış](animation-overview.md)
