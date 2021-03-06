---
title: 'Nasıl yapılır: Veri CollectionView İçindeki Nesneler Aracılığıyla Gezinme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- CollectionView [WPF], navigating through objects
- data binding [WPF], navigating through objects in data CollectionView
- navigating through objects in data CollectionView [WPF]
ms.assetid: fcd37590-bce1-4ac9-8b74-3b96c7458b8a
ms.openlocfilehash: 1507ab4db0c91b670d8bca754f6fd67d887c7041
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61931522"
---
# <a name="how-to-navigate-through-the-objects-in-a-data-collectionview"></a>Nasıl yapılır: Veri CollectionView İçindeki Nesneler Aracılığıyla Gezinme
Görünümler, aynı veri koleksiyonunu sıralama, filtreleme ve gruplandırma bağlı olarak farklı şekillerde görüntülenmesine izin verir. Görünümleri, ayrıca geçerli bir kayıt işaretçi kavramı sağlar ve imleci taşıma etkinleştirin. Bu örnek geçerli nesne olarak sunulan işlevleri kullanarak bir veri koleksiyonu içindeki nesneler aracılığıyla gezinme nasıl gösterir <xref:System.Windows.Data.CollectionView> sınıfı.  
  
## <a name="example"></a>Örnek  
 Bu örnekte, `myCollectionView` olduğu bir <xref:System.Windows.Data.CollectionView> bağlı bir koleksiyon üzerinde bir görünümü olan nesne.  
  
 Aşağıdaki örnekte, `OnButton` için bir olay işleyicisi `Previous` ve `Next` bir uygulamada, veri toplama gitmek kullanıcının olanak tanıyan düğmeler düğmeleri. Unutmayın <xref:System.Windows.Data.CollectionView.IsCurrentBeforeFirst%2A> ve <xref:System.Windows.Data.CollectionView.IsCurrentAfterLast%2A> rapor özelliklerini geçerli kayıt işaretçisine başında ve sonunda listesinin için sırasıyla şekilde gelip gelmediğini <xref:System.Windows.Data.CollectionView.MoveCurrentToFirst%2A> ve <xref:System.Windows.Data.CollectionView.MoveCurrentToLast%2A> uygun olarak çağrılabilir.  
  
 <xref:System.Windows.Data.CollectionView.CurrentItem%2A> Görünümün özelliği olarak atandığında bir `Order` koleksiyonda geçerli sipariş öğesi döndürülecek.  
  
 [!code-csharp[CollectionView#OnButton](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionView/CSharp/Page1.xaml.cs#onbutton)]
 [!code-vb[CollectionView#OnButton](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CollectionView/VisualBasic/Page1.xaml.vb#onbutton)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Veri Bağlamaya Genel Bakış](data-binding-overview.md)
- [Görünümde Verileri Sıralama](how-to-sort-data-in-a-view.md)
- [Görünümde Veri Filtreleme](how-to-filter-data-in-a-view.md)
- [XAML İçerisinde bir Görüntü Kullanarak Verileri Sıralama ve Gruplama](how-to-sort-and-group-data-using-a-view-in-xaml.md)
- [Nasıl Yapılır Konuları](data-binding-how-to-topics.md)
