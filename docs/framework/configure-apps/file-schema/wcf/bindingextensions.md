---
title: <bindingExtensions>
ms.date: 03/30/2017
ms.assetid: 8373f94d-d095-486f-8f1e-4ac2f72b58c7
ms.openlocfilehash: ed55701e45d8580e37cf4776de6b9c5241e0548c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61673484"
---
# <a name="bindingextensions"></a>\<bindingExtensions >
Bu bölümde, kullanıcı tanımlı bir makineden bağlama kullanımını etkinleştirir veya uygulama yapılandırma dosyası. Kullanıcı tanımlı kullanılarak bu koleksiyona bağlama ekleyebileceğiniz `add` anahtar sözcüğü ve ayarı `type` özniteliği kullanıcı tanımlı bağlama, öğenin yanı sıra `name` tanımlanan bağlama kullanıcı adı özniteliği.  
  
 Bağlama uzantıları bir uç nokta yapılandırması bir parçası olarak kullanmak için kullanıcı tanımlı bağlamalar oluşturma olanağı sunar. Programlı olarak soyut sınıf uygulayan bir tür bir bağlama uzantısı olan <xref:System.ServiceModel.Channels.Binding>.  
  
 Aşağıdaki örnekte `add` öğesi hem de `name` özniteliği bir bağlama uzantının ekleneceği `bindingElementExtensions` yapılandırma dosyasının.  
  
```xml  
<system.serviceModel>
  <extensions>
    <bindingExtensions>
      <add name="MyBinding"
           type="Microsoft.ServiceModel.Samples.MyBinding, MyBinding,
                 Version=1.0.0.0, Culture=neutral, PublicKeyToken=null" />
    </bindingExtensions>
  </extensions>
</system.serviceModel>
```  
  
 Yapılandırma yeteneklerini öğesine eklemek için yazmak ve kaydetmek kullanıcı gerekli bir `bindingSection` öğesi. Bunun hakkında daha fazla bilgi için bkz. <xref:System.Configuration> belgeleri.  
  
 Öğesi ve kendi yapılandırma türü tanımlandıktan sonra uzantıyı aşağıdaki örnekte gösterildiği gibi bir uç noktasının bir parçası kullanılabilir.  
  
```xml  
<services>
  <service name="MyService">
    <endpoint address="myAddress"
              binding="MyBinding" />
  </service>
</services>
```  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Bağlamaları Genişletme](../../../../../docs/framework/wcf/extending/extending-bindings.md)
