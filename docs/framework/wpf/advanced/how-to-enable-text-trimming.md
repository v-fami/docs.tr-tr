---
title: 'Nasıl yapılır: Metin Kırpmayı Etkinleştirme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [WPF], trimming
- documents [WPF], trimming text
- trimming text [WPF]
ms.assetid: dd8c9191-d2be-45fd-9fb4-3c75b65578c5
ms.openlocfilehash: 25fff566868e792004a915fee195485c4a1f385f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61776135"
---
# <a name="how-to-enable-text-trimming"></a>Nasıl yapılır: Metin Kırpmayı Etkinleştirme

Bu örnek kullanımını ve kullanılabilir değerleri etkilerini gösterir <xref:System.Windows.TextTrimming> sabit listesi.

## <a name="example"></a>Örnek

Aşağıdaki örnekte tanımlayan bir <xref:System.Windows.Controls.TextBlock> öğeyle <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> öznitelik kümesi.

[!code-xaml[TextTrimmingSnippets#_TextTrimmingXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTrimmingSnippets/CSharp/Window1.xaml#_texttrimmingxaml)]

Buna karşılık gelen ayarı <xref:System.Windows.TextTrimming> kod özelliğinde aşağıda gösterilmiştir.

[!code-csharp[TextTrimmingSnippets#_TextTrimmingSetTextTrimming](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTrimmingSnippets/CSharp/Window1.xaml.cs#_texttrimmingsettexttrimming)]
[!code-vb[TextTrimmingSnippets#_TextTrimmingSetTextTrimming](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextTrimmingSnippets/VisualBasic/Window1.xaml.vb#_texttrimmingsettexttrimming)]

Metin kırpma için şu anda üç seçenek vardır: **CharacterEllipsis**, **WordEllipsis**, ve **hiçbiri**.

Zaman <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> ayarlanır **CharacterEllipsis**, metin kırpılır ve kırpma kenarına en yakın karakterde üç nokta ile devam eder.  Bu ayar daha yakından kırpmayı sınıra uyacak şekilde metin olarak kırpmaya ancak sözcükler kesilecek kısmen neden olabilir.  Aşağıdaki şekil, bu ayarda etkisini gösterir. bir <xref:System.Windows.Controls.TextBlock> yukarıda tanımlanan benzer.

![Örnek: TextTrimming.CharacterEllipsis](./media/texttrimming-character.png "TextTrimming_Character")

Zaman <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> ayarlanır **WordEllipsis**, metin kırpılır ve kırpma kenarına en yakın ilk tam sözcük sonuna üç nokta ile devam eder.  Bu ayar, kısmen bölünen sözcükleri göstermez ancak yakın kesme kenara metin değil olarak kırpmaya **CharacterEllipsis** ayarı.  Aşağıdaki şekil, bu ayarda etkisini gösterir <xref:System.Windows.Controls.TextBlock> yukarıda tanımlanan.

![Örnek: TextTrimming.WordEllipsis](./media/texttrimming-word.png "TextTrimming_Word")

Zaman <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> ayarlanır **hiçbiri**, hiçbir metin kırpmayı gerçekleştirilir.  Bu durumda, metin yalnızca metin kapsayıcının üst sınıra kırpılır.  Aşağıdaki şekil, bu ayarda etkisini gösterir. bir <xref:System.Windows.Controls.TextBlock> yukarıda tanımlanan benzer.

![Örnek: TextTrimming.None](./media/texttrimming-none.png "TextTrimming_None")
