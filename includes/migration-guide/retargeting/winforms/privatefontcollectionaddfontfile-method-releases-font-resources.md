---
ms.openlocfilehash: f5d93d76ab3409d4d4c1870cfef94cac59f9475c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61762645"
---
### <a name="privatefontcollectionaddfontfile-method-releases-font-resources"></a>PrivateFontCollection.AddFontFile yöntemi yazı tipi kaynakları serbest bırakır.

|   |   |
|---|---|
|Ayrıntılar|.NET Framework 4.7.1 ve önceki sürümlerde <xref:System.Drawing.Text.PrivateFontCollection?displayProperty=nameWithType> sınıfı, sonra GDI +'da yazı tipi kaynakları serbest değil <xref:System.Drawing.Text.PrivateFontCollection> için atıldı <xref:System.Drawing.Font> kullanarak bu koleksiyona eklendiğinden nesneleri <xref:System.Drawing.Text.PrivateFontCollection.AddFontFile(System.String)> yöntemi. .NET Framework'teki 4.7.2 ve daha sonra <xref:System.Drawing.Text.FontCollection.Dispose%2A> dosyaları olarak eklenen GDI +'da yazı tiplerinin serbest bırakır.|
|Öneri|<strong>İçine veya dışına bu değişiklikleri nasıl</strong>sırada bu değişiklikleri yararlanmak bir uygulama için .NET Framework 4.7.2 çalıştırmanız gerekir veya üzeri. Uygulamaya bu değişiklikler aşağıdaki yollardan birini yararlanabilir:<ul><li>.NET Framework 4.7.2 hedefleyecek şekilde derlenmiştir. Bu, varsayılan olarak .NET Framework'ü 4.7.2 hedefleyen Windows Forms uygulamaları etkin ya da üzeri değişikliktir.</li><li>.NET Framework 4.7.1 veya önceki bir sürümünü hedefleyen ve eski erişilebilirlik davranışları dışında aşağıdakileri ekleyerek bölgedeyse [AppContext anahtar](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) için <code>&lt;runtime&gt;</code> app.config dosyası ve içinayarlamabölümünü<code>false</code>aşağıdaki örnekte gösterildiği gibi.</li></ul><pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Drawing.Text.DoNotRemoveGdiFontsResourcesFromFontCollection=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>.NET Framework 4.7.2 hedefleyen uygulamalar veya sonraki bir sürümü ve eski korumak istediğiniz davranışı kabul etme yazı tipi kaynakları açıkça ayarlayarak bu AppContext anahtar sunmamayı <code>true</code>.|
|Kapsam|Kenar|
|Sürüm|4.7.2|
|Tür|Yeniden Hedefleme|
|Etkilenen API’ler|<ul><li><xref:System.Drawing.Text.PrivateFontCollection.AddFontFile(System.String)?displayProperty=nameWithType></li><li><xref:System.Drawing.Text.FontCollection.Dispose?displayProperty=nameWithType></li></ul>|
