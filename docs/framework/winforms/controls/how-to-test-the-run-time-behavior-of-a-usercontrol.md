---
title: 'Nasıl yapılır: Bir UserControl Denetiminin Çalışma Zamanı Davranışını Sınama'
ms.date: 03/30/2017
helpviewer_keywords:
- UserControl class [Windows Forms], testing
- user controls [Windows Forms], testing
- composite controls [Windows Forms], testing
- UserControl Test Container
- UserControl class [Windows Forms], run-time behavior
ms.assetid: 4e4d5c49-1346-40ac-9d96-40211b573583
ms.openlocfilehash: 48531ab1ef3b30b6516e3f2e7b5858a8884cbfe8
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211706"
---
# <a name="how-to-test-the-run-time-behavior-of-a-usercontrol"></a>Nasıl yapılır: Bir UserControl denetiminin çalışma zamanı davranışını sınama

Geliştirirken bir <xref:System.Windows.Forms.UserControl>, çalışma zamanı davranışını sınama gerekir. Ayrı Windows tabanlı uygulama projesi oluşturun ve test form üzerindeki denetiminizi yerleştirin, ancak bu zor bir işlemdir. Daha hızlı ve kolay bir yolu **UserControl Test kapsayıcısı** Visual Studio tarafından sağlanan. Bu test kapsayıcısında, doğrudan Windows Denetim Kitaplığı projenizden başlatır.

> [!IMPORTANT]
> Yüklemek test kapsayıcısı için <xref:System.Windows.Forms.UserControl>, denetimin en az bir ortak oluşturucuya sahip olmalıdır.

> [!NOTE]
> Visual C++ denetimi kullanarak sınanamıyor **UserControl Test kapsayıcısı**.

## <a name="test-the-run-time-behavior-of-a-usercontrol"></a>Bir UserControl denetiminin çalışma zamanı davranışını sınama

1. Adlı bir Windows Denetim Kitaplığı projesini Visual Studio'da oluşturma **TestContainerExample**. Ayrıntılar için bkz [Windows Denetim Kitaplığı şablonu](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).

2. İçinde **Windows Form Tasarımcısı**, sürükleyin bir <xref:System.Windows.Forms.Label> denetimi **araç kutusu** denetimin tasarım yüzeyine.

3. Tuşuna **F5** Projeyi derlemek ve çalıştırmak için **UserControl Test kapsayıcısı**. Test kapsayıcısı ile görünür, <xref:System.Windows.Forms.UserControl> içinde **Önizleme** bölmesi.

4. Seçin <xref:System.Windows.Forms.Control.BackColor%2A> görüntülenen özelliği <xref:System.Windows.Forms.PropertyGrid> denetim sağındaki **Önizleme** bölmesi. Değerine değiştirmek `ControlDark`. Denetim daha koyu bir renge dönüşür gözlemleyin. Diğer özellik değerleri değiştirmeyi deneyin ve denetim üzerindeki etkisini inceleyin.

5. Tıklayın **Dock dolgu kullanıcı denetimi** aşağıdaki onay kutularından **Önizleme** bölmesi. Denetim bölmesinde doldurmak için boyutlandırılır gözlemleyin. Test kapsayıcı yeniden boyutlandırma ve Denetim ile bölmesinde yeniden boyutlandırılır gözlemleyin.

6. Test kapsayıcısını kapatın.

7. Başka bir kullanıcı denetimine ekleme **TestContainerExample** proje. Ayrıntılar için bkz [nasıl yapılır: Projeye var olan öğeleri ekleme](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100)).

8. İçinde **Windows Form Tasarımcısı**, sürükleyin bir <xref:System.Windows.Forms.Button> denetimi **araç kutusu** denetimin tasarım yüzeyine.

9. Projeyi oluşturmak ve test kapsayıcıyı çalıştırmak için F5 tuşuna basın.

10. Tıklayın **kullanıcı denetimi seçin** <xref:System.Windows.Forms.ComboBox> iki kullanıcı denetimler arasında geçiş yapmak için.

## <a name="test-user-controls-from-another-project"></a>Kullanıcı denetimleri başka bir projeden test

Kullanıcı denetimleri diğer projelerden geçerli projenin test kapsayıcısında test edebilirsiniz.

1. Adlı bir Windows Denetim Kitaplığı projesi oluşturun **TestContainerExample2**. Ayrıntılar için bkz [Windows Denetim Kitaplığı şablonu](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).

2. İçinde **Windows Form Tasarımcısı**, sürükleyin bir <xref:System.Windows.Forms.RadioButton> denetimi **araç kutusu** denetimin tasarım yüzeyine.

3. Projeyi oluşturmak ve test kapsayıcıyı çalıştırmak için F5 tuşuna basın. Test kapsayıcısı ile görünür, <xref:System.Windows.Forms.UserControl> içinde **Önizleme** bölmesi.

4. Tıklayın **yük** düğmesi.

5. İçinde **açık** iletişim kutusunda, gitmek **TestContainerExample**önceki yordamda oluşturulan .dll,. Seçin **TestContainerExample**tıklayın ve .dll **açık** yük kullanıcı denetimleri için düğme

6. Kullanım **kullanıcı denetimi seçin** <xref:System.Windows.Forms.ComboBox> iki kullanıcı denetimlerini arasında geçiş yapmak için **TestContainerExample** proje.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.UserControl>
- [Nasıl yapılır: Bileşik denetimler yazma](how-to-author-composite-controls.md)
- [İzlenecek yol: Visual Basic ile bileşik denetim yazma](walkthrough-authoring-a-composite-control-with-visual-basic.md)
- [İzlenecek yol: Visual C# ile bileşik denetim yazma](walkthrough-authoring-a-composite-control-with-visual-csharp.md)
- [Kullanıcı denetimi Tasarımcısı](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/183c3hth(v=vs.100))
