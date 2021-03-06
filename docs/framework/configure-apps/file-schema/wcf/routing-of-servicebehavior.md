---
title: <routing> / <serviceBehavior>
ms.date: 03/30/2017
ms.assetid: d8f9c844-4629-4a45-9599-856dc8f01794
ms.openlocfilehash: b7a9be18395ef8878900d754b5aa5afdeee0cff8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61783064"
---
# <a name="routing-of-servicebehavior"></a>\<Yönlendirme >, \<serviceBehavior >
Dinamik yönlendirme yapılandırması değişikliğini izin vermek için yönlendirme hizmeti çalışma zamanı erişim sağlar.  
  
 \<system.ServiceModel>  
\<davranışlar >  
\<serviceBehaviors>  
\<davranışı >  
\<Yönlendirme >  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <routing filterTable="String"
               routeOnHeadersOnly="Boolean"
               SoapProcessingEnabled="Boolean" />
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|filterTable|Yönlendirme hizmeti tarafından değerlendirilecek filtreleri içeren yönlendirme tablosunun adını belirten dize. Bu değer eşleşmelidir `name` özniteliği bir [ \<filterTable >](../../../../../docs/framework/configure-apps/file-schema/wcf/filtertable.md) öğesinde [ \<filterTables >](../../../../../docs/framework/configure-apps/file-schema/wcf/filtertables.md) bölümü.|  
|routeOnHeaderOnly|Filtre hem ileti gövdesi ve üst bilgi veya üst bilgi inceleyin olup olmadığını belirten bir Boole değeri. Varsayılan, `true` değeridir.|  
|soapProcessingEnabled|SOAP işleme olmamalıdır olup olmadığını belirten bir Boole değeri.|  
  
### <a name="child-elements"></a>Alt Öğeler  
 Yok.  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[\<davranışı >](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|Bir davranış öğesi belirtir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Hizmetin davranışı yapılandırmasına eklendiğinde, bu yapılandırma öğesi, hizmet için yönlendirme sağlar. Bu öğe hizmeti tarafından kullanılacak gerçek yönlendirme tablosunu belirtebilirsiniz.  
  
 Bu yapılandırma bölümü kullanarak dağıtım desen değiştiğinde hareket halindeyken yönlendirme ayarlarınızı değiştirebilirsiniz. Çalışma zamanında, yönlendirme yeni ayarlarla yönlendirme uzantınızı kaydedebilir ve yönlendirme hizmeti yeni iletileri için güncelleştirilmiş yapılandırma bilgilerini kullanarak başlar ve oturumlar, hangi kuralları kullanarak uçuşan iletileri/oturumları bırakarak çalışırken bulunduğunuz Bunlar başlatıldığında yerleştirin.  Bu oturum için güvenli, geri dönüşüm daha az yeniden yapılandırılmasını yönlendirme hizmeti çalışma zamanı sırasında yapabilmenizi sağlar.  
