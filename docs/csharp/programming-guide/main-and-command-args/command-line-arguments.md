---
title: Komut satırı bağımsız değişkenleri - C# Programlama Kılavuzu
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- command-line arguments [C#]
ms.assetid: 0e597e0d-ea7a-41ba-a38a-0198122f3c26
ms.openlocfilehash: 8216e144dfcaeaf9b480d681ae91ce59832ae9e3
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65877531"
---
# <a name="command-line-arguments-c-programming-guide"></a>Komut Satırı Bağımsız Değişkenleri (C# Programlama Kılavuzu)
Bağımsız değişken gönderebilirsiniz `Main` yöntemi aşağıdaki yöntemlerden biriyle tanımlayarak yöntemi:  
  
 [!code-csharp[csProgGuideMain#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideMain/CS/Class3.cs#2)]  
  
 [!code-csharp[csProgGuideMain#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideMain/CS/Class3.cs#3)]  
  
> [!NOTE]
>  Komut satırı bağımsız değişkenlerini etkinleştirmek için `Main` yöntemi bir Windows Forms uygulamasındaki el ile değiştirmeniz gerekir imzası `Main` program.CS'de webhostbuilder'a. Windows Forms Tasarımcısı tarafından oluşturulan kod oluşturur bir `Main` girdi parametresi olmadan. Ayrıca <xref:System.Environment.CommandLine%2A?displayProperty=nameWithType> veya <xref:System.Environment.GetCommandLineArgs%2A?displayProperty=nameWithType> konsolda veya Windows uygulama herhangi bir noktasından komut satırı bağımsız değişkenleri erişmek için.  
  
 Parametresi `Main` yöntemi bir <xref:System.String> komut satırı bağımsız değişkenlerini temsil eden bir dizi. Genellikle, test ederek bağımsız değişkenleri var olup olmadığını belirlemeniz `Length` özelliği, örneğin:  
  
 [!code-csharp[csProgGuideMain#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideMain/CS/Class3.cs#4)]  
  
 Kullanarak dize bağımsız değişkenlerini sayısal türlere de dönüştürebilirsiniz <xref:System.Convert> sınıfı veya `Parse` yöntemi. Örneğin, aşağıdaki deyim dönüştürür `string` için bir `long` numarası kullanarak <xref:System.Int64.Parse%2A> yöntemi:  
  
```  
long num = Int64.Parse(args[0]);  
```  
  
 C# türü kullanmak da mümkündür `long`, hangi diğer adların `Int64`:  
  
```  
long num = long.Parse(args[0]);  
```  
  
 Ayrıca `Convert` sınıfı yöntemi `ToInt64` aynı şeyi yapmak için:  
  
```  
long num = Convert.ToInt64(s);  
```  
  
 Daha fazla bilgi için bkz. <xref:System.Int64.Parse%2A> ve <xref:System.Convert>.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, bir konsol uygulamasında komut satırı bağımsız değişkenleri kullanmayı gösterir. Uygulama çalışma zamanında bir bağımsız değişken alır, bağımsız değişkeni bir tamsayıya dönüştürür ve sayının faktöriyelini hesaplar. Bağımsız değişken sağlanmadıysa uygulama programın doğru kullanımını açıklayan bir ileti verir.  
  
 Derleme ve uygulamayı bir komut istemi'nden çalıştırmak için bu adımları izleyin:  
  
1. Aşağıdaki kodu herhangi bir metin düzenleyiciye yapıştırın ve dosyayı ada sahip bir metin dosyası olarak kaydedin `Factorial.cs`.  
  
     [!code-csharp[csProgGuideMain#16](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideMain/CS/Class1.cs#16)]  
  
2. Gelen **Başlat** ekran veya **Başlat** menüsünde, Visual Studio'yu açın **Geliştirici komut istemi** penceresini ve ardından yeni dosyasını içeren klasöre gidin oluşturuldu.  
  
3. Uygulamayı derlemek üzere aşağıdaki komutu girin.  
  
     `csc Factorial.cs`  
  
     Uygulamanızın adında bir yürütülebilir dosya hiç derleme hatası varsa `Factorial.exe` oluşturulur.  
  
4. 3'ün faktoriyelini hesaplamak için aşağıdaki komutu girin:  
  
     `Factorial 3`  
  
5. Komut şu çıktıyı üretir: `The factorial of 3 is 6.`  
  
> [!NOTE]
>  Visual Studio'da bir uygulama çalıştırırken, komut satırı bağımsız değişkenlerinde belirtebilirsiniz [hata ayıklama sayfası, Proje Tasarımcısı](/visualstudio/ide/reference/debug-page-project-designer).  
  
 Komut satırı bağımsız değişkenlerinin nasıl kullanılacağı hakkında daha fazla örnek için bkz. [nasıl yapılır: Komut satırını kullanarak derlemeler oluşturma ve kullanma](../../../csharp/programming-guide/concepts/assemblies-gac/how-to-create-and-use-assemblies-using-the-command-line.md).  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Environment?displayProperty=nameWithType>
- [C# Programlama Kılavuzu](../../../csharp/programming-guide/index.md)
- [Ana() ve Komut Satırı Bağımsız Değişkenleri](../../../csharp/programming-guide/main-and-command-args/index.md)
- [Nasıl yapılır: Komut satırı bağımsız değişkenlerini görüntüleme](../../../csharp/programming-guide/main-and-command-args/how-to-display-command-line-arguments.md)
- [Ana() Dönüş Değerleri](../../../csharp/programming-guide/main-and-command-args/main-return-values.md)
- [Sınıflar](../../../csharp/programming-guide/classes-and-structs/classes.md)
