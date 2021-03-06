---
title: 'Nasıl yapılır: -Office Programlamada adlandırılmış ve isteğe bağlı bağımsız değişkenler kullanan C# Programlama Kılavuzu'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- named and optional arguments [C#], Office programming
- optional arguments [C#], Office programming
- named arguments [C#], Office programming
ms.assetid: 65b8a222-bcd8-454c-845f-84adff5a356f
ms.openlocfilehash: 3ecea9d55ef61d2158da0dabeca22a58460b3bea
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61975211"
---
# <a name="how-to-use-named-and-optional-arguments-in-office-programming-c-programming-guide"></a>Nasıl yapılır: Office Programlamada adlandırılmış ve isteğe bağlı bağımsız değişkenleri kullanma (C# Programlama Kılavuzu)
Adlandırılmış bağımsız değişkenler ve sunulan isteğe bağlı bağımsız değişkenlere [!INCLUDE[csharp_dev10_long](~/includes/csharp-dev10-long-md.md)], kolaylık, esneklik ve C# programlama okunabilirliği geliştirmek. Ayrıca, bu özellikler, Microsoft Office Otomasyon API'leri gibi COM arabirimlerine erişim büyük ölçüde kolaylaştırır.  
  
 Aşağıdaki örnekte, yöntem [ConvertToTable](<xref:Microsoft.Office.Interop.Word.Range.ConvertToTable%2A>) on altı gibi sütun ve biçimlendirme, satır sayısını sınırlayan bir tablonun özellikleri temsil eden parametreleri, yazı tiplerini ve renkleri vardır. Çoğu zaman hepsi için belirli değerler belirtmek istemiyorsanız çünkü tüm on altı, isteğe bağlı parametrelerdir. Ancak, adlandırılmış ve isteğe bağlı bağımsız değişkenler bir değer veya bir yer tutucu değerini her parametre için sağlanan gerekir. Adlandırılmış ve isteğe bağlı bağımsız değişkenleri ile projeniz için gerekli olan parametreleri için değerler belirtin.  
  
 Bu yordamları tamamlamak için Microsoft Office Word bilgisayarınızda yüklü olması gerekir.  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-create-a-new-console-application"></a>Yeni bir konsol uygulaması oluşturmak için  
  
1. Visual Studio’yu çalıştırın.  
  
2. Üzerinde **dosya** menüsünde **yeni**ve ardından **proje**.  
  
3. İçinde **şablon kategorileri** bölmesini genişletin **Visual C#** ve ardından **Windows**.  
  
4. Üst konum **şablonları** emin olmak için bölmesinde **.NET Framework 4** görünür **hedef Framework'ü** kutusu.  
  
5. İçinde **şablonları** bölmesinde tıklayın **konsol uygulaması**.  
  
6. Projeniz için bir ad yazın **adı** alan.  
  
7. **Tamam**'ı tıklatın.  
  
     Yeni Proje görünür **Çözüm Gezgini**.  
  
### <a name="to-add-a-reference"></a>Başvuru eklemek için  
  
1. İçinde **Çözüm Gezgini**, projenizin adına sağ tıklayın ve ardından **Başvuru Ekle**. **Başvuru Ekle** iletişim kutusu görüntülenir.  
  
2. Üzerinde **.NET** sayfasında **Microsoft.Office.Interop.Word** içinde **bileşen adı** listesi.  
  
3. **Tamam**'ı tıklatın.  
  
### <a name="to-add-necessary-using-directives"></a>Eklemek için gerekli yönergeleri kullanma  
  
1. İçinde **Çözüm Gezgini**, sağ **Program.cs** dosya ve ardından **kodu görüntüle**.  
  
2. Aşağıdaki `using` kod dosyasının en üstüne yönergeleri.  
  
     [!code-csharp[csProgGuideNamedAndOptional#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csprogguidenamedandoptional/cs/wordprogram.cs#4)]  
  
### <a name="to-display-text-in-a-word-document"></a>Word belgesinde metni görüntülemek için  
  
1. İçinde `Program` sınıfı Program.cs içinde bir Word uygulaması ve bir Word belgesi oluşturmak için aşağıdaki yöntemi ekleyin. [Ekle](<xref:Microsoft.Office.Interop.Word.Documents.Add%2A>) yöntemi dört isteğe bağlı parametreye sahiptir. Bu örnek, varsayılan değerleri kullanır. Bu nedenle, arama deyiminde hiçbir bağımsız değişken gereklidir.  
  
     [!code-csharp[csProgGuideNamedAndOptional#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csprogguidenamedandoptional/cs/wordprogram.cs#6)]  
  
2. Aşağıdaki kod, belgede metin görüntüleneceği yeri ve görüntülenecek metni tanımlamak için yöntem sonuna ekleyin.  
  
     [!code-csharp[csProgGuideNamedAndOptional#7](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csprogguidenamedandoptional/cs/wordprogram.cs#7)]  
  
### <a name="to-run-the-application"></a>Uygulamayı çalıştırmak için  
  
1. Aşağıdaki deyim, ana ekleyin.  
  
     [!code-csharp[csProgGuideNamedAndOptional#8](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csprogguidenamedandoptional/cs/wordprogram.cs#8)]  
  
2. Projeyi çalıştırmak için CTRL + F5 tuşlarına basın. Belirtilen metni içeren bir Word belgesi görünür.  
  
### <a name="to-change-the-text-to-a-table"></a>Metin bir tabloya dönüştürmek için  
  
1. Kullanım `ConvertToTable` bir tabloda metin kapsamak için yöntemi. Yöntemi, on altı isteğe bağlı parametre yok. IntelliSense aşağıdaki çizimde gösterildiği gibi isteğe bağlı parametreler köşeli parantez içine alır.  
  
     ![ConvertToTable yönteminin listesi](./media/how-to-use-named-and-optional-arguments-in-office-programming/convert-table-parameters.png)  
  
     Adlandırılmış ve isteğe bağlı bağımsız değişkenler yalnızca değiştirmek istediğiniz parametreleri için değerleri belirtmenize olanak verir. Yönteminin sonuna aşağıdaki kodu ekleyin `DisplayInWord` basit bir tablo oluşturun. Metinde virgüller de dize bağımsız değişkeni belirtir `range` tablo hücrelerini ayırın.  
  
     [!code-csharp[csProgGuideNamedAndOptional#9](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csprogguidenamedandoptional/cs/wordprogram.cs#9)]  
  
     C#, çağrısı'nın önceki sürümlerinde `ConvertToTable` aşağıdaki kodda gösterildiği gibi her parametre için bir başvuru bağımsız değişkeni gerektirir.  
  
     [!code-csharp[csProgGuideNamedAndOptional#14](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csprogguidenamedandoptional/cs/wordprogram.cs#14)]  
  
2. Projeyi çalıştırmak için CTRL + F5 tuşlarına basın.  
  
### <a name="to-experiment-with-other-parameters"></a>Diğer parametreler ile denemek için  
  
1. Bir sütun ve üç satır sahip olacak şekilde değiştirmek için son satırında değiştirin `DisplayInWord` CTRL + F5'e yazın ve aşağıdaki deyimi.  
  
     [!code-csharp[csProgGuideNamedAndOptional#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csprogguidenamedandoptional/cs/wordprogram.cs#10)]  
  
2. Tablo için önceden tanımlanmış bir biçimi belirtmek için son satırında değiştirin `DisplayInWord` CTRL + F5'e yazın ve aşağıdaki deyimi. Biçim herhangi biri olabilir [WdTableFormat](<xref:Microsoft.Office.Interop.Word.WdTableFormat>) sabitler.  
  
     [!code-csharp[csProgGuideNamedAndOptional#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csprogguidenamedandoptional/cs/wordprogram.cs#11)]  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod tam örneği içerir.  
  
 [!code-csharp[csProgGuideNamedAndOptional#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csprogguidenamedandoptional/cs/wordprogram.cs#12)]  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Adlandırılmış ve İsteğe Bağlı Bağımsız Değişkenler](../../../csharp/programming-guide/classes-and-structs/named-and-optional-arguments.md)
