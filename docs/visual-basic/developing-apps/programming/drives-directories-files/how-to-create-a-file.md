---
title: "Nasıl yapılır: Visual Basic'te dosya oluşturma"
ms.date: 07/20/2015
helpviewer_keywords:
- text files [Visual Basic], creating
- files [Visual Basic], creating
ms.assetid: 0253bb6d-5519-4a50-b882-b93ef5cca0d9
ms.openlocfilehash: f24fdd6ce1fea7540c33e4a2fdfc06885825f76a
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64628979"
---
# <a name="how-to-create-a-file-in-visual-basic"></a>Nasıl yapılır: Visual Basic'te dosya oluşturma
Bu örnek, belirtilen yolu kullanarak boş bir metin dosyası oluşturur <xref:System.IO.File.Create%2A> yönteminde <xref:System.IO.File> sınıfı.  
  
## <a name="example"></a>Örnek  
 [!code-vb[VbFileIOMisc#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIOMisc/VB/class2.vb#1)]  
  
## <a name="compiling-the-code"></a>Kod Derleniyor  
 Kullanım `file` dosyaya yazmak için değişken.  
  
## <a name="robust-programming"></a>Güçlü Programlama  
 Dosya zaten varsa, değiştirilir.  
  
 Aşağıdaki koşullar özel bir duruma neden olabilir:  
  
- Yol adı yanlış biçimlendirilmiş. Örneğin, geçersiz karakterler içeriyor veya yalnızca boşluk (<xref:System.ArgumentException>).  
  
- Salt okunur yoludur (<xref:System.IO.IOException>).  
  
- Yol adı `Nothing` (<xref:System.ArgumentNullException>).  
  
- Yol adı çok uzun (<xref:System.IO.PathTooLongException>).  
  
- Yol geçersiz (<xref:System.IO.DirectoryNotFoundException>).  
  
- Yalnızca bir iki nokta üst üste yoludur ":" (<xref:System.NotSupportedException>).  
  
## <a name="net-framework-security"></a>.NET Framework Güvenliği  
 A <xref:System.Security.SecurityException> kısmi güven düzeyine sahip ortamlarda oluşturulabilir.  
  
 Çağrı <xref:System.IO.File.Create%2A> gerektirdiğine <xref:System.Security.Permissions.FileIOPermission>.  
  
 Bir <xref:System.UnauthorizedAccessException> kullanıcının dosyayı oluşturma izni yoksa oluşturulur.  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.IO>
- <xref:System.IO.File.Create%2A>
- [Kısmen güvenilen koddan kitaplıkları kullanma](../../../../framework/misc/using-libraries-from-partially-trusted-code.md)
- [Kod erişimi güvenliği temelleri](../../../../framework/misc/code-access-security-basics.md)
