---
title: 'Nasıl yapılır: Çalışma Zamanında bir Denetimler Koleksiyonuna Ekleme veya Kaldırma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- run time [Windows Forms], removing controls
- controls [Windows Forms], adding using collections
- controls collections
- collections [Windows Forms], adding items
- run time [Windows Forms], adding controls
- controls [Windows Forms], removing using collections
ms.assetid: 771bf895-3d5f-469b-a324-3528f343657e
ms.openlocfilehash: 85c1d398c1aabbb73d5ae34186775e2c63666cfb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59309452"
---
# <a name="how-to-add-to-or-remove-from-a-collection-of-controls-at-run-time"></a>Nasıl yapılır: Çalışma Zamanında bir Denetimler Koleksiyonuna Ekleme veya Kaldırma
Uygulama geliştirme için ortak görevler için denetimler ekleme ve herhangi bir kapsayıcı denetimi, form üzerinde denetimleri kaldırma (gibi <xref:System.Windows.Forms.Panel> veya <xref:System.Windows.Forms.GroupBox> denetim veya formun kendisi bile). Tasarım zamanında denetimler doğrudan Masası veya grup kutusu sürüklenebilen. Çalışma zamanında bu denetimi yöneten bir `Controls` koleksiyonunun hangi denetimlerin üzerine yerleştirilen izler.  
  
> [!NOTE]
>  Aşağıdaki kod örneği, bir denetim koleksiyonunu tutar herhangi bir denetimi için geçerlidir.  
  
### <a name="to-add-a-control-to-a-collection-programmatically"></a>Bir denetimin program aracılığıyla bir koleksiyona eklemek için  
  
1. Eklenecek denetimin örneği oluşturun.  
  
2. Yeni denetimin özelliklerini ayarlayın.  
  
3. Denetime eklemek `Controls` üst denetim koleksiyonu.  
  
     Aşağıdaki kod örneği, bir örneğini oluşturma işlemi gösterilmektedir <xref:System.Windows.Forms.Button> denetimi. Bir formla gerektiren bir <xref:System.Windows.Forms.Panel> denetimi düğmesi için olay işleme yöntemi oluşturulmakta, `NewPanelButton_Click`, zaten mevcut.  
  
    ```vb  
    Public NewPanelButton As New Button()  
  
    Public Sub AddNewControl()  
       ' The Add method will accept as a parameter any object that derives  
       ' from the Control class. In this case, it is a Button control.  
       Panel1.Controls.Add(NewPanelButton)  
       ' The event handler indicated for the Click event in the code   
       ' below is used as an example. Substite the appropriate event  
       ' handler for your application.  
       AddHandler NewPanelButton.Click, AddressOf NewPanelButton_Click  
    End Sub  
    ```  
  
    ```csharp  
    public Button newPanelButton = new Button();  
  
    public void addNewControl()  
    {   
       // The Add method will accept as a parameter any object that derives  
       // from the Control class. In this case, it is a Button control.  
       panel1.Controls.Add(newPanelButton);  
       // The event handler indicated for the Click event in the code   
       // below is used as an example. Substitute the appropriate event  
       // handler for your application.  
       this.newPanelButton.Click += new System.EventHandler(this. NewPanelButton_Click);  
    }  
    ```  
  
### <a name="to-remove-controls-from-a-collection-programmatically"></a>Denetimleri bir koleksiyondan programlı bir şekilde kaldırmak için  
  
1. Olay işleyici olaydan kaldırılacak. Visual Basic'teki [RemoveHandler deyimi](~/docs/visual-basic/language-reference/statements/removehandler-statement.md) anahtar sözcüğü; görselde C#, kullanın [-= işleci (C# başvuru)](~/docs/csharp/language-reference/operators/subtraction-assignment-operator.md).  
  
2. Kullanım `Remove` istediğiniz denetimi panelinden 's silinemedi yöntemi `Controls` koleksiyonu.  
  
3. Çağrı <xref:System.Windows.Forms.Control.Dispose%2A> denetim tarafından kullanılan tüm kaynakları serbest bırakmak için yöntemi.  
  
    ```vb  
    Public Sub RemoveControl()  
    ' NOTE: The code below uses the instance of   
    ' the button (NewPanelButton) from the previous example.  
       If Panel1.Controls.Contains(NewPanelButton) Then  
          RemoveHandler NewPanelButton.Click, AddressOf _   
             NewPanelButton_Click  
          Panel1.Controls.Remove(NewPanelButton)  
          NewPanelButton.Dispose()  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void removeControl(object sender, System.EventArgs e)  
    {  
    // NOTE: The code below uses the instance of   
    // the button (newPanelButton) from the previous example.  
       if(panel1.Controls.Contains(newPanelButton))  
       {  
          this.newPanelButton.Click -= new System.EventHandler(this.   
             NewPanelButton_Click);  
          panel1.Controls.Remove(newPanelButton);  
          newPanelButton.Dispose();  
       }  
    }  
    ```  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Windows.Forms.Panel>
- [Panel Denetimi](panel-control-windows-forms.md)
