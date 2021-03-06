---
title: "Nasıl yapılır: Belirli bir düzendeki dosyaları Visual Basic'te bir dizine kopyalayın"
ms.date: 07/20/2015
helpviewer_keywords:
- My.Computer.FileSystem.CopyFile method, copying files [Visual Basic]
- files [Visual Basic], copying
- CopyFile method [Visual Basic], copying files in Visual Basic
- I/O [Visual Basic], copying files
ms.assetid: f205d2ad-bbe5-4d55-8a40-acda21aa82dd
ms.openlocfilehash: 15bec7c9604b243c586b393d71007b02917d3a6e
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64628932"
---
# <a name="how-to-copy-files-with-a-specific-pattern-to-a-directory-in-visual-basic"></a>Nasıl yapılır: Belirli bir düzendeki dosyaları Visual Basic'te bir dizine kopyalayın
<xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.GetFiles%2A> Yöntemi dosyaları için yol adlarını temsil eden dizeleri salt okunur bir koleksiyonunu döndürür. Kullanabileceğiniz `wildCards` parametresini kullanarak belirli bir desen belirtin.  
  
 Eşleşen hiçbir dosya bulunamazsa, boş bir koleksiyon döndürülür.  
  
 Kullanabileceğiniz <xref:Microsoft.VisualBasic.FileIO.FileSystem.CopyFile%2A> bir dizinine dosyalar kopyalamak için yöntemi.  
  
### <a name="to-copy-files-with-a-specific-pattern-to-a-directory"></a>Belirli bir düzendeki dosyaları dizine kopyalama  
  
1. Kullanım `GetFiles` dosyaların listesini döndürmek için yöntemi. Bu örnek belirtilen dizindeki tüm .rtf dosyaları döndürür.  
  
     [!code-vb[VbFileIOMisc#36](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIOMisc/VB/Class1.vb#36)]  
  
2. Kullanım `CopyFile` dosyaları kopyalamak için yöntemi. Bu örnek adlı bir dizin dosyaları kopyalar `testdirectory`.  
  
     [!code-vb[VbVbcnMyFileSystem#88](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#88)]  
  
3. Kapat `For` deyimiyle bir `Next` deyimi.  
  
     [!code-vb[VbVbcnMyFileSystem#89](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#89)]  
  
## <a name="example"></a>Örnek  
 Yukarıdaki kod, formun tamamını sunar, aşağıdaki örnekte, tüm .rtf dosyaları belirtilen dizine adlı dizine kopyalar `testdirectory`.  
  
 [!code-vb[VbFileIOMisc#37](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIOMisc/VB/Class1.vb#37)]  
  
## <a name="net-framework-security"></a>.NET Framework Güvenliği  
 Aşağıdaki koşullar özel bir duruma neden olabilir:  
  
- Yol aşağıdaki nedenlerden biri için geçerli değildir: sıfır uzunluklu bir dize olan, yalnızca boşluk içeriyor, geçersiz karakterler içeriyor veya cihaz yoludur (ile başlayan \\ \\.\\) (<xref:System.ArgumentException>).  
  
- Çünkü bu yolu geçerli değil `Nothing` (<xref:System.ArgumentNullException>).  
  
- Dizin mevcut değil (<xref:System.IO.DirectoryNotFoundException>).  
  
- Mevcut bir dosyayı dizine işaret (<xref:System.IO.IOException>).  
  
- Yolun sistem tarafından tanımlanan uzunluk üst sınırını aşıyor (<xref:System.IO.PathTooLongException>).  
  
- Yolda bir dosya veya dizin adı iki nokta üst üste (:) içeriyor veya biçimi geçersiz (<xref:System.NotSupportedException>).  
  
- Kullanıcı yolu görüntülemek için gerekli izinlere sahip değil (<xref:System.Security.SecurityException>). Kullanıcı gerekli izinlere sahip değil (<xref:System.UnauthorizedAccessException>).  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:Microsoft.VisualBasic.FileIO.FileSystem.CopyFile%2A>
- <xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.GetFiles%2A>
- [Nasıl yapılır: Belirli bir desendeki alt dizinleri bulma](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-find-subdirectories-with-a-specific-pattern.md)
- [Sorun giderme: Okuma ve dosyalara metin yazma](../../../../visual-basic/developing-apps/programming/drives-directories-files/troubleshooting-reading-from-and-writing-to-text-files.md)
- [Nasıl yapılır: Bir dizindeki dosya koleksiyonunu alma](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-get-the-collection-of-files-in-a-directory.md)
