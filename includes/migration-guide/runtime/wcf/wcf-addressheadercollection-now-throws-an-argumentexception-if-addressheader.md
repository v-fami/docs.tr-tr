---
ms.openlocfilehash: d8c9cec723ec4e57fb4868cc95881be8eb4001b7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61764039"
---
### <a name="wcf-addressheadercollection-now-throws-an-argumentexception-if-an-addressheader-element-is-null"></a>WCF AddressHeaderCollection addressHeader öğe null ise artık ArgumentException oluşturur.

|   |   |
|---|---|
|Ayrıntılar|.NET Framework 4.7.1, ile başlayarak <xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})> Oluşturucusu oluşturur bir <xref:System.ArgumentException> öğeler ise <code>null</code>. .NET Framework 4.7 ve önceki sürümlerinde, hiçbir özel durum oluşturulur.|
|Öneri|Bu değişiklik .NET Framework 4.7.1 veya sonraki bir sürümü üzerinde uyumluluk sorunlarıyla karşılaşırsanız, bunu aşağıdaki satırı ekleyerek çevirme <code>&lt;runtime&gt;</code> app.config dosyasının::<pre><code class="lang-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableAddressHeaderCollectionValidation=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Kapsam|İkincil|
|Sürüm|4.7.1|
|Tür|Çalışma zamanı|
|Etkilenen API’ler|<ul><li><xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})?displayProperty=nameWithType></li></ul>|
