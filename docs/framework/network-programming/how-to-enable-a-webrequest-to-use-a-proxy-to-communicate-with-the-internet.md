---
title: 'Nasıl yapılır: İnternet ile İletişim Kurmak Üzere Ara Sunucu Kullanan bir WebRequest’i Etkinleştirme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 63c0ef2c-44b5-4c54-9804-ba0b9b001ac7
ms.openlocfilehash: 99bbff5a3350f55f04fdbd6ce7147b6597773322
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64624595"
---
# <a name="how-to-enable-a-webrequest-to-use-a-proxy-to-communicate-with-the-internet"></a>Nasıl yapılır: İnternet ile İletişim Kurmak Üzere Ara Sunucu Kullanan bir WebRequest’i Etkinleştirme
Bu örnek, tüm olanak sağlayacak bir genel proxy örneği oluşturur <xref:System.Net.WebRequest> Internet ile iletişim kurmak için bir ara sunucu kullanmak için. Bu örnek, proxy sunucusu adlandırıldığını varsayar `webproxy` ve üzerinde iletişim bağlantı noktası 80, standart HTTP bağlantı noktası.  
  
## <a name="example"></a>Örnek  
  
```csharp  
WebProxy proxyObject = new WebProxy("http://webproxy:80/");  
GlobalProxySelection.Select = proxyObject;  
```  
  
```vb  
Dim proxyObject As WebProxy = New WebProxy("http://webproxy:80/")  
GlobalProxySelection.Select = proxyObject  
```  
  
## <a name="compiling-the-code"></a>Kod Derleniyor  
 Bu örnek gerektirir:  
  
- A [ `using` yönergesi](../../csharp/language-reference/keywords/using-directive.md) için **System.Net** ad alanı.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Uygulama Protokolleri Kullanma](../../../docs/framework/network-programming/using-application-protocols.md)
- [Ara Sunucu Üzerinden İnternet Erişimi](../../../docs/framework/network-programming/accessing-the-internet-through-a-proxy.md)
