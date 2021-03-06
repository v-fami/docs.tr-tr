---
title: 'Nasıl yapılır: Windows Forms RichTextBox Denetimi Dosyaları Kaydetme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- saving files
- RTF files [Windows Forms], saving in RichTextBox control
- examples [Windows Forms], text boxes
- saving files [Windows Forms], RichTextBox control
- files [Windows Forms], saving with RichTextBox control
- RichTextBox control [Windows Forms], saving files
- .rtf files [Windows Forms], saving in RichTextBox control
- text files [Windows Forms], saving from RichTextBox control
ms.assetid: 4a58ec19-84d1-4383-9110-298c06adcfca
ms.openlocfilehash: 9a4f5a98c9fea9658d9d9a400faa773b78a12f3a
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64638312"
---
# <a name="how-to-save-files-with-the-windows-forms-richtextbox-control"></a>Nasıl yapılır: Windows Forms RichTextBox Denetimi Dosyaları Kaydetme
Windows Forms <xref:System.Windows.Forms.RichTextBox> denetimi olarak bulunan biçimlerden birini görüntüler bilgileri yazabilirsiniz:  
  
- Düz metin  
  
- Unicode düz metin  
  
- Zengin metin biçimi (RTF)  
  
- OLE nesneleri yerine boşluk RTF  
  
- Düz metin değerinin metinsel bir gösterimini OLE nesneleri ile  
  
 Bir dosyayı kaydetmek için çağrı <xref:System.Windows.Forms.RichTextBox.SaveFile%2A> yöntemi. Ayrıca **SaveFile** bir akışa veri kaydetmek için yöntemi. Daha fazla bilgi için bkz. <xref:System.Windows.Forms.RichTextBox.SaveFile%28System.IO.Stream%2CSystem.Windows.Forms.RichTextBoxStreamType%29>.  
  
### <a name="to-save-the-contents-of-the-control-to-a-file"></a>Denetimin içeriğini bir dosyaya kaydetmek için  
  
1. Kaydedilecek dosyanın yolunu belirleyin.  
  
     Bir gerçek yaşam uygulaması içinde bunun için genellikle kullanacağınız <xref:System.Windows.Forms.SaveFileDialog> bileşeni. Genel bakış için bkz. [SaveFileDialog bileşenine genel bakış](savefiledialog-component-overview-windows-forms.md).  
  
2. Çağrı <xref:System.Windows.Forms.RichTextBox.SaveFile%2A> yöntemi <xref:System.Windows.Forms.RichTextBox> kaydedin ve isteğe bağlı olarak bir dosya türünü belirten bir denetim. Bir dosya adı yalnızca bağımsız değişken olarak yöntemi çağırın, dosyanın RTF olarak kaydedilir. Başka bir dosya türü belirtmek için bir değerini yöntemi çağırın <xref:System.Windows.Forms.RichTextBoxStreamType> ikinci bağımsız değişken olarak numaralandırması.  
  
     Aşağıdaki örnekte, yolunu ayarlamak için zengin metin dosyasının konumunu **Belgelerim** klasör. Bu konum, Windows işletim sistemi çalıştırılan bilgisayarların çoğu bu klasör içerdiğini varsayar çünkü kullanılır. Bu konumu seçme, güvenli bir şekilde uygulamayı çalıştırmak minimum sistem erişim düzeylerine sahip kullanıcılar sağlar. Aşağıdaki örnekte bir form varsayar bir <xref:System.Windows.Forms.RichTextBox> denetim zaten eklendi.  
  
    ```vb  
    Public Sub SaveFile()  
       ' You should replace the bold file name in the   
       ' sample below with a file name of your own choosing.  
       RichTextBox1.SaveFile(System.Environment.GetFolderPath _  
       (System.Environment.SpecialFolder.Personal) _  
       & "\Testdoc.rtf", _  
          RichTextBoxStreamType.RichNoOleObjs)  
    End Sub  
    ```  
  
    ```csharp  
    public void SaveFile()  
    {  
       // You should replace the bold file name in the   
       // sample below with a file name of your own choosing.  
       // Note the escape character used (@) when specifying the path.  
       richTextBox1.SaveFile(System.Environment.GetFolderPath  
       (System.Environment.SpecialFolder.Personal)  
       + @"\Testdoc.rtf",  
          RichTextBoxStreamType.RichNoOleObjs);  
    }  
    ```  
  
    ```cpp  
    public:  
       void SaveFile()  
       {  
          // You should replace the bold file name in the   
          // sample below with a file name of your own choosing.  
          richTextBox1->SaveFile(String::Concat  
             (System::Environment::GetFolderPath  
             (System::Environment::SpecialFolder::Personal),  
             "\\Testdoc.rtf"), RichTextBoxStreamType::RichNoOleObjs);  
       }  
    ```  
  
    > [!IMPORTANT]
    >  Bu örnek, bir dosya zaten mevcut değilse yeni bir dosya oluşturur. Bir uygulama bir dosya oluşturması gerekiyorsa, bu uygulama için klasör oluşturma erişmesi gerekir. İzinler, erişim denetim listeleri kullanılarak ayarlanır. Dosya zaten varsa, uygulamanın daha az ayrıcalıkla yalnızca yazma erişimi gerekir. Mümkün olan yerlerde, dosyayı dağıtım sırasında oluşturmak ve yalnızca tek bir dosyayı okuma yetkisi vermek yerine erişim için bir klasör oluşturmak için daha güvenlidir. Ayrıca, kök klasöre veya Program dosyaları klasörüne kullanıcı klasörleri verileri yazmak amacıyla daha güvenlidir.  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.RichTextBox.SaveFile%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.RichTextBox>
- [RichTextBox Denetimi](richtextbox-control-windows-forms.md)
- [Windows Forms'da Kullanılacak Denetimler](controls-to-use-on-windows-forms.md)
