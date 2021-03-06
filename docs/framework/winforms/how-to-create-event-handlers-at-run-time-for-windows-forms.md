---
title: 'Nasıl yapılır: Windows Forms için Çalışma Zamanındaki Olay İşleyicileri'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms, event handling
- event handlers [Windows Forms], creating
- run time [Windows Forms], creating event handlers at
- examples [Windows Forms], event handling
- Button control [Windows Forms], event handlers
ms.assetid: 2e7c9e1a-61fe-444d-8113-3c5bacf1c8cb
ms.openlocfilehash: 4d2290622e648030f150d9bb06ce1f3000145759
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211462"
---
# <a name="how-to-create-event-handlers-at-run-time-for-windows-forms"></a>Nasıl yapılır: Windows Forms için Çalışma Zamanındaki Olay İşleyicileri

Visual Studio'da Windows Forms Tasarımcısı'nı kullanarak olayları oluşturmaya ek olarak, çalışma zamanında bir olay işleyicisi de oluşturabilirsiniz. Bu eylem, bunları programı ilk kez başlatıldığında, bağlı olan'ın aksine çalışma zamanında kod koşullara göre olay işleyicileri bağlanmanızı sağlar.

## <a name="create-an-event-handler-at-run-time"></a>Çalışma zamanında bir olay işleyicisi oluşturun

1. Bir olay işleyicisi eklemek istediğiniz formunu açın.

2. Yöntem imzası için kullanmak istediğiniz olay ile formunuza bir yöntem ekleyin.

     Örneğin, işleme, <xref:System.Windows.Forms.Control.Click> olayı bir <xref:System.Windows.Forms.Button> denetimi, aşağıdaki gibi bir yöntem oluşturma:

    ```vb
    Private Sub Button1_Click(ByVal sender As Object, ByVal e As EventArgs)
       ' Add event handler code here.
    End Sub
    ```

    ```csharp
    private void button1_Click(object sender, System.EventArgs e)
    {
    // Add event handler code here.
    }
    ```

    ```cpp
    private:
       void button1_Click(System::Object ^ sender,
          System::EventArgs ^ e)
       {
          // Add event handler code here.
       }
    ```

3. Uygulamanıza uygun şekilde olay işleyicisine kod ekleyin.

4. Hangi form veya denetim için bir olay işleyicisi oluşturmak istiyorsanız bu seçeneği belirleyin.

5. Formunuzun sınıf içindeki bir yöntemde, olayı işlemek için olay işleyicisini belirten kod ekleyin. Örneğin, olay işleyicisine aşağıdaki kodu belirtir `button1_Click` tanıtıcıları <xref:System.Windows.Forms.Control.Click> olayı bir <xref:System.Windows.Forms.Button> denetimi:

    ```vb
    AddHandler Button1.Click, AddressOf Button1_Click
    ```

    ```csharp
    button1.Click += new EventHandler(button1_Click);
    ```

    ```cpp
    button1->Click += gcnew System::EventHandler(this, &Form1::button1_Click);
    ```

     <xref:System.ComponentModel.EventHandlerList.AddHandler%2A> Yukarıdaki Visual Basic kodu içinde gösterilen yöntemi, bir düğme için tıklama olayı işleyicisi oluşturur.

## <a name="see-also"></a>Ayrıca bkz.

- [Windows Forms'ta Olay İşleyicileri Oluşturma](creating-event-handlers-in-windows-forms.md)
- [Olay İşleyicilerine Genel Bakış](event-handlers-overview-windows-forms.md)
- [Basic'de devralınmış olay işleyicileri Visual Basic sorunlarını giderme](~/docs/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers.md)
