---
title: 'Nasıl yapılır: Tür Kitaplıklarına Başvurular Ekleme'
ms.date: 03/30/2017
helpviewer_keywords:
- importing type library
- interop assemblies, generating
- type libraries
- COM interop, importing type library
ms.assetid: f5cfa6ba-cc25-4017-82cd-ba7391859113
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2b3fda2af84ff74e129c36dc966bad247bdf9e20
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61643289"
---
# <a name="how-to-add-references-to-type-libraries"></a>Nasıl yapılır: Tür Kitaplıklarına Başvurular Ekleme
Visual Studio, bir tür kitaplığına bir başvuru eklediğinizde, meta verileri içeren bir birlikte çalışma derlemesi oluşturur. Visual Studio, bir birincil birlikte çalışma derlemesi varsa, yeni bir birlikte çalışma bütünleştirilmiş kodu oluşturuluyor önce mevcut bütünleştirilmiş kodu kullanır.  
  
### <a name="to-add-a-reference-to-a-type-library-in-visual-studio"></a>Visual Studio'da bir tür kitaplığına bir başvuru eklemek için  
  
1. Bir Windows Setup.exe dosyasını yükleme sizin için gerçekleştirir, bilgisayarınızda COM DLL veya EXE dosyasının yükleyin.  
  
2. Seçin **proje**, **Başvurusu Ekle**.  
  
3. Başvuru Yöneticisi'nde seçin **COM**.  
  
4. Tür kitaplığını listeden seçin veya .tlb dosyasına göz at.  
  
5. **Tamam**’ı seçin.  
  
6. Çözüm Gezgini içinde eklenen yeni başvuru için kısayol menüsünü açın ve ardından **özellikleri**.  
  
7. İçinde **özellikleri** penceresinde emin **birlikte çalışma türlerini katıştır** özelliği **True**. Bu, uygulamanız ile birincil birlikte çalışma derlemelerini dağıtma gereksinimini ortadan kaldıran, yürütülebilir dosyaları, COM türleri için tür bilgisi katıştırma Visual Studio neden olur.  
  
> [!NOTE]
>  Menü ve iletişim kutusu seçenekleri, kullanmakta olduğunuz Visual Studio sürümüne bağlı olarak değişiklik gösterebilir.  
  
### <a name="to-add-a-reference-to-a-type-library-for-command-line-compilation"></a>Komut satırı derlemesi için bir tür kitaplığına bir başvuru eklemek için  
  
1. Birlikte çalışma derlemesi açıklandığı gibi oluşturmak [nasıl yapılır: Tür kitaplıklarından birlikte çalışma derlemeleri oluşturma](how-to-generate-interop-assemblies-from-type-libraries.md).  
  
2. Kullanım [/link (C# derleyici seçenekleri)](../../csharp/language-reference/compiler-options/link-compiler-option.md) veya [/Link (Visual Basic)](../../visual-basic/reference/command-line-compiler/link.md) COM için tür bilgilerini katıştırma derleyici seçeneğiyle birlikte çalışma bütünleştirilmiş kod adı, yürütülebilir dosyaların türleri.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Tür Kitaplığını Bütünleştirilmiş Kod Olarak İçeri Aktarma](importing-a-type-library-as-an-assembly.md)
- [COM Bileşenlerini .NET Framework'te Gösterme](exposing-com-components.md)
- [İzlenecek yol: Yönetilen derlemeler Visual Studio'da türler katıştırma (C#)](../../csharp/programming-guide/concepts/assemblies-gac/walkthrough-embedding-types-from-managed-assemblies-in-visual-studio.md) 
- [İzlenecek yol: Visual Studio'da (Visual Basic) yönetilen derlemelerden türler katıştırma](../../visual-basic/programming-guide/concepts/assemblies-gac/walkthrough-embedding-types-from-managed-assemblies-in-vs.md)
- [/ Link (C# Derleyici Seçenekleri)](../../csharp/language-reference/compiler-options/link-compiler-option.md)
- [/ Link (Visual Basic)](../../visual-basic/reference/command-line-compiler/link.md)
