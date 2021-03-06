---
title: 'Nasıl yapılır: Windows Forms’a Kullanıcı Arabirimi Olmadan Denetimler Ekleme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- NonVisualSelection
helpviewer_keywords:
- invisible controls [Windows Forms]
- Windows Forms controls, adding to form
- controls [Windows Forms], nonvisual
- Windows Forms controls, nonvisual
- nonvisual controls [Windows Forms]
ms.assetid: 52134d9c-cff6-4eed-8e2b-3d5eb3bd494e
ms.openlocfilehash: 49bf927085d29b60c1d9cf5d61df3894495349db
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65210420"
---
# <a name="how-to-add-controls-without-a-user-interface-to-windows-forms"></a>Nasıl yapılır: Windows Forms’a Kullanıcı Arabirimi Olmadan Denetimler Ekleme

Görsel olmayan denetim (veya bileşen) uygulamanıza işlevsellik sağlar. Diğer denetimleri farklı bileşenleri bir kullanıcı arabirimi kullanıcıya sağlamaz ve bu nedenle Windows Form Tasarımcısı yüzeyine görüntülenmesi gerekmez. Bir forma bir bileşen eklendiğinde Windows Form Tasarımcısı yeniden boyutlandırılabilir Tepsisi tüm bileşenleri görüntülendiği formun alt kısmındaki görüntüler. Bir denetim, bileşen tepsisine eklendikten sonra bileşeni seçebilir ve herhangi bir form denetiminde olduğu gibi özelliklerini ayarlayın.

## <a name="add-a-component-to-a-windows-form"></a>Bir Windows forma bir bileşen ekleyin

1. Form, Visual Studio'da açın. Ayrıntılar için bkz [nasıl yapılır: Tasarımcıda Windows formlarını görüntüleme](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w5yd62ts(v=vs.100)).

2. İçinde **araç kutusu**bir bileşene tıklayın ve formunuza sürükleyin.

     Bileşen, bileşen tepsisinde görünür.

Ayrıca, bileşenler çalışma zamanında bir forma eklenebilir. Özellikle bileşenleri farklı bir kullanıcı arabirimi denetimleri bir görsel ifade olmadığı için yaygın bir senaryo budur. Aşağıdaki örnekte bir <xref:System.Windows.Forms.Timer> bileşen çalışma zamanında eklenir. (Visual Studio birkaç farklı zamanlayıcılar içerdiğine dikkat edin; bu durumda, bir Windows Forms kullanın <xref:System.Windows.Forms.Timer> bileşeni. Visual Studio'da farklı zamanlayıcılar hakkında daha fazla bilgi için bkz. [sunucu tabanlı zamanlayıcılar giriş](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).)

> [!CAUTION]
> Bileşenler genellikle etkili bir şekilde çalışması bileşeni için ayarlanmalıdır denetime özgü özelikleri sahiptir. Durumunda, <xref:System.Windows.Forms.Timer> aşağıdaki bileşen, ayarladığınız `Interval` özelliği. Bileşenlerin özellikleri söz konusu bileşen için gerekli olarak ayarlayın, projenize eklerken emin olun.

## <a name="add-a-component-to-a-windows-form-programmatically"></a>Bir bileşen program aracılığıyla bir Windows forma ekleme

1. Bir örneğini oluşturmak <xref:System.Windows.Forms.Timer> kod sınıfı.

2. Ayarlama `Interval` Zamanlayıcının işaretleri arasındaki süreyi belirlemek için özellik.

3. Bileşeniniz için gerekli diğer özellikleri yapılandırın.

     Aşağıdaki kod oluşturma işlemini gösterir. bir <xref:System.Windows.Forms.Timer> ile kendi `Interval` özellik kümesi.

    ```vb
    Public Sub CreateTimer()
       Dim timerKeepTrack As New System.Windows.Forms.Timer
       timerKeepTrack.Interval = 1000
    End Sub
    ```

    ```csharp
    public void createTimer()
    {
       System.Windows.Forms.Timer timerKeepTrack = new
           System.Windows.Forms.Timer();
       timerKeepTrack.Interval = 1000;
    }
    ```

    ```cpp
    public:
       void createTimer()
       {
          System::Windows::Forms::Timer^ timerKeepTrack = gcnew
             System::Windows::Forms::Timer();
          timerKeepTrack->Interval = 1000;
       }
    ```

    > [!IMPORTANT]
    > Yerel bir güvenlik riski ağ üzerinden bilgisayarınıza kötü amaçlı bir UserControl başvurarak doğurabilir. Bu, yalnızca, yanlışlıkla bunu projenize ekleyerek ardından zararlı olabilecek özel bir denetim oluşturulamaz kötü amaçlı bir kişinin söz konusu olduğunda önemli hale gelir.

## <a name="see-also"></a>Ayrıca bkz.

- [Windows Forms Denetimleri](index.md)
- [Nasıl yapılır: Windows Forms'a denetimler ekleme](how-to-add-controls-to-windows-forms.md)
- [Nasıl yapılır: Windows Forms'a ActiveX denetimleri ekleme](how-to-add-activex-controls-to-windows-forms.md)
- [Nasıl yapılır: Windows Forms arasında denetimleri kopyalama](how-to-copy-controls-between-windows-forms.md)
- [Windows Forms’a Denetimler Yerleştirme](putting-controls-on-windows-forms.md)
- [Ayrı Windows Forms Denetimlerini Etiketleme ve Kısayollarını Sunma](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [Windows Forms'da Kullanılacak Denetimler](controls-to-use-on-windows-forms.md)
- [İşleve Göre Windows Forms Denetimleri](windows-forms-controls-by-function.md)
