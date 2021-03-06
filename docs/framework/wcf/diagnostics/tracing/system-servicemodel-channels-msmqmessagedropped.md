---
title: System.ServiceModel.Channels.MsmqMessageDropped
ms.date: 03/30/2017
ms.assetid: 8b6e644d-fa68-4be7-abe9-3659671a37c1
ms.openlocfilehash: 3fa5ec62c5e8ac83f3f81fb406499b7e596b3dac
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61969513"
---
# <a name="systemservicemodelchannelsmsmqmessagedropped"></a>System.ServiceModel.Channels.MsmqMessageDropped
İletinin MSMQ bırakıldı.  
  
## <a name="description"></a>Açıklama  
 İzleme, bir MSMQ iletisinin bırakıldı gösterir. Windows Communication Foundation (WCF) (NetMsmqBinding veya MsmqIntegrationBinding ile kullanılır) bunları işleyemiyor olduğunda MSMQ iletileri bırakılabilir. Bu türden iletilere zehirli ileti olarak adlandırılır.  
  
 Zehirli ileti ne zaman bırakılan `ReceiveErrorHandling` özelliği NetMsmqBinding veya MsmqIntegrationBinding `Drop`. Bırakılan ileti kuyruktan kaldırılır ve artık kurtarılabilir.  
  
 Bkz: [Poison ileti işleme](https://go.microsoft.com/fwlink/?LinkID=99546) iletileri zehirli duruma ne zaman ve uygun şekilde işlemek için hizmetinizi yapılandırmak nasıl daha fazla ayrıntı için.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [İzleme](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [Uygulamanızda Sorun Giderme için İzleme Kullanma](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [Yönetim ve Tanılama](../../../../../docs/framework/wcf/diagnostics/index.md)
- [Poison ileti işleme](https://go.microsoft.com/fwlink/?LinkID=99546)
