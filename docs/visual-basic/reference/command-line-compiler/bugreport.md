---
title: -bugreport
ms.date: 03/08/2018
helpviewer_keywords:
- -bugreport compiler option [Visual Basic]
- bugreport compiler option [Visual Basic]
- /bugreport compiler option [Visual Basic]
ms.assetid: e4325406-8dbd-4b48-b311-9ee0799e48bb
ms.openlocfilehash: 440e583b55765d680ee72f8574f929e335e10cdb
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65590637"
---
# <a name="-bugreport"></a>-bugreport
Bir hata raporu dosyası oluştururken kullanabileceğiniz bir dosya oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
-bugreport:file  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terim|Tanım|  
|---|---|  
|`file`|Gerekli. Hata raporunuzu içerecek dosyanın adı. Dosya adı tırnak içine alın ("") adı boşluk içeriyorsa.|  
  
## <a name="remarks"></a>Açıklamalar  
 Aşağıdaki bilgileri eklenir `file`:  
  
- Derlemedeki tüm kaynak kodu dosyalarının bir kopyasını.  
  
- Derlemede kullanılan derleyici seçeneklerinin bir listesi.  
  
- Derleyici, ortak dil çalışma zamanı ve işletim sistemi sürüm bilgisi.  
  
- Derleyici çıkışı, varsa.  
  
- Kendileri için sizden istenir, sorun açıklaması.  
  
- Sorunun ne düşündüğünüzü açıklaması düzeltilmelidir, kendileri için sizden istenir.  
  
 Tüm kaynak kodu dosyalarının bir kopyasını dahil olduğundan `file`, kısa olası programına (şüphelenilen) kod hatasını yeniden oluşturmak isteyebilirsiniz.  
  
> [!IMPORTANT]
>  `-bugreport` Seçenek olası duyarlı bilgileri içeren bir dosya oluşturur. Bu geçerli zaman, derleyici sürümü, .NET Framework sürümü, işletim sistemi sürümü, kullanıcı adı, komut satırı bağımsız değişkenleri ile derleyici çalıştırıldığı, tüm kaynak kodu ve herhangi başvurulan bütünleştirilmiş kodun ikili biçimini içerir. Bu seçenek, bir sunucu tarafı derleme bir ASP.NET uygulaması için Web.config dosyasında komut satırı seçeneklerini belirleyerek erişilebilir. Bunu önlemek için sunucuda önleyen kullanıcıların Machine.config dosyasının değiştirin.  
  
 Bu seçeneği ile kullandıysanız `-errorreport:prompt`, `-errorreport:queue`, veya `-errorreport:send`, ve bir iç derleyici hata bilgileri uygulamanızın karşılaştığı `file` Microsoft Corporation gönderilir. Bu bilgiler, Microsoft mühendisleri hatanın nedenini belirlemenize yardımcı olur ve Visual Basic'in sonraki sürümüne artırmanıza yardımcı olabilir. Varsayılan olarak, hiçbir bilgi Microsoft'a gönderilmez. Ancak, derleme yaparken bir uygulama kullanarak `-errorreport:queue`, varsayılan olarak etkindir, bu uygulama, hata raporlarını toplar. Ardından, bilgisayarın yönetici oturum açtığında, hata raporlama sistem yönetici oturum açma işleminden sonra gerçekleşen tüm hata raporlarını Microsoft'a iletecek şekilde sağlayan bir açılır pencere görüntüler.  
  
> [!NOTE]
>  `/bugreport` Seçeneği, Visual Studio geliştirme ortamında kullanılabilir değil; yalnızca komut satırından derleme yaptığınızda kullanılabilir.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek derler `T2.vb` ve hata raporlama tüm bilgileri dosyada koyar `Problem.txt`.  
  
```  
vbc -bugreport:problem.txt t2.vb  
```  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Visual Basic komut satırı derleyicisi](../../../visual-basic/reference/command-line-compiler/index.md)
- [-debug (Visual Basic)](../../../visual-basic/reference/command-line-compiler/debug.md)
- [-errorreport](../../../visual-basic/reference/command-line-compiler/errorreport.md)
- [Örnek Derleme Komut Satırları](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- [trustLevel öğesi securityPolicy (ASP.NET Settings Schema) için](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/as399f0x(v=vs.100))
