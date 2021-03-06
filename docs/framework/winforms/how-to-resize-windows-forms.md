---
title: 'Nasıl yapılır: Windows Forms’u Yeniden Boyutlandırma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- resizing Windows Forms
- Windows Forms, resizing
ms.assetid: 5d9dd47e-e68c-48c9-a0a3-a9ff34ba009d
ms.openlocfilehash: aa7ee2bbbf6983a371ea71edc0dfd0cc12cd0c9d
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211661"
---
# <a name="how-to-resize-windows-forms"></a>Nasıl yapılır: Windows Forms’u Yeniden Boyutlandırma

Windows formunuzda boyutu birkaç şekilde belirtebilirsiniz. İçin yeni bir değer ayarlayarak hem yüksekliğini hem de formun genişliğine programlama yoluyla değiştirebilirsiniz <xref:System.Windows.Forms.Form.Size%2A> özelliği veya ayarla <xref:System.Windows.Forms.Control.Height%2A> veya <xref:System.Windows.Forms.Control.Width%2A> özellikleri ayrı ayrı. Visual Studio kullanıyorsanız, Windows Forms Tasarımcısı'nı kullanarak boyutunu değiştirebilirsiniz. Ayrıca bkz: [nasıl yapılır: Tasarımcı kullanarak Windows formlarını yeniden boyutlandır](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/37k2zkwx(v=vs.100)).

## <a name="resize-a-form-programmatically"></a>Bir form programlı olarak yeniden boyutlandırma

Form boyutunu çalışma zamanında ayarlayarak tanımlarsanız <xref:System.Windows.Forms.Form.Size%2A> formun özelliği.

Aşağıdaki kod örneği, 100 x 100 piksel olarak ayarlayın form boyutunu gösterir.

```vb
Form1.Size = New System.Drawing.Size(100, 100)
```

```csharp
Form1.Size = new System.Drawing.Size(100, 100);
```

```cpp
Form1->Size = System::Drawing::Size(100, 100);
```

## <a name="change-form-width-and-height-programmatically"></a>Form genişlik ve yükseklik program aracılığıyla değiştirme

Sonra <xref:System.Windows.Forms.Form.Size%2A> olan tanımlanmış formu yükseklik veya genişlik kullanarak değiştirmek <xref:System.Windows.Forms.Control.Width%2A> veya <xref:System.Windows.Forms.Control.Height%2A> özellikleri.

Aşağıdaki kod örneği, yüksekliği sabit kalır ancak formun sol kenardan 300 piksel olarak ayarlayın formun genişliğine gösterir.

```vb
Form1.Width = 300
```

```csharp
Form1.Width = 300;
```

```cpp
Form1->Width = 300;
```

-veya-

Değişiklik <xref:System.Drawing.Size.Width%2A> veya <xref:System.Drawing.Size.Height%2A> ayarlayarak <xref:System.Windows.Forms.Form.Size%2A> özelliği.

Aşağıdaki kod örneğinde gösterildiği gibi ancak bu ayarı yalnızca daha fazla hantal yaklaşımdır <xref:System.Windows.Forms.Control.Width%2A> veya <xref:System.Windows.Forms.Control.Height%2A> özellikleri.

```vb
Form1.Size = New Size(300, Form1.Size.Height)
```

```csharp
Form1.Size = new Size(300, Form1.Size.Height);
```

```cpp
Form1->Size = System::Drawing::Size(300, Form1->Size.Height);
```

## <a name="change-form-size-by-increments-programmatically"></a>Form boyutunu artışlarla program aracılığıyla değiştirme

Formun boyutunu artırmak için ayarlanmış <xref:System.Drawing.Size.Width%2A> ve <xref:System.Drawing.Size.Height%2A> özellikleri.

Aşağıdaki kod örneği, geçerli boyuttan daha geniş 200 piksel olarak formun genişliğini gösterir.

```vb
Form1.Width += 200
```

```csharp
Form1.Width += 200;
```

```cpp
Form1->Width += 200;
```

> [!CAUTION]
> Her zaman <xref:System.Drawing.Size.Height%2A> veya <xref:System.Drawing.Size.Width%2A> yükseklik ve genişlik boyutları ayarlayarak aynı anda ayarlamakta olduğunuz sürece, bir form boyutunu değiştirmek için özellik <xref:System.Windows.Forms.Form.Size%2A> yeni bir özellik <xref:System.Drawing.Size> yapısı. <xref:System.Windows.Forms.Form.Size%2A> Özelliği döndürür bir <xref:System.Drawing.Size> yapısı, bir değer türüdür. Bir değer türünün özelliğine yeni bir değer atanamaz. Bu nedenle, aşağıdaki kod örneği derlemeyecektir.

```vb
' NOTE: CODE WILL NOT COMPILE
Dim f As New Form()
f.Size.Width += 100
```

```csharp
// NOTE: CODE WILL NOT COMPILE
Form f = new Form();
f.Size.Width += 100;
```

```cpp
// NOTE: CODE WILL NOT COMPILE
Form^ f = gcnew Form();
f->Size->X += 100;
```

## <a name="see-also"></a>Ayrıca bkz.

- [Windows Forms'a Başlarken](getting-started-with-windows-forms.md)
- [Windows Forms Uygulamalarını Geliştirme](./advanced/index.md)
