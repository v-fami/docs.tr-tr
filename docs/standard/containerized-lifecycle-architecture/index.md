---
title: Kapsayıcılar ve Docker’a Giriş
description: Docker'ı kullanmanın başlıca avantajları üst düzey bir bakış edinin.
ms.date: 02/15/2019
ms.openlocfilehash: a03c67ed4fbc55c84e69fba5b7978863c8305e00
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65644955"
---
# <a name="introduction-to-containers-and-docker"></a>Kapsayıcılar ve Docker'a giriş

*Kapsayıcı içinde bir uygulama veya hizmeti ve bağımlılıklarını yapılandırmasıyla (dağıtım bildirim dosyaları soyutlanır) bir arada bir kapsayıcı görüntüsü paketlenmiş yazılım geliştirme için bir yaklaşımdır. Ardından bir birim olarak kapsayıcılı uygulamayı test etme ve konak işletim sistemi (OS) bir kapsayıcı görüntüsü örneği olarak dağıtabilirsiniz.*

Yalnızca ürün sevk, train veya kargo içinde bağımsız olarak kamyon taşınmasını nakliye izin vermek gibi yazılım kapsayıcıları farklı kodu ve bağımlılıkları içerebilir, yazılım dağıtımının standart bir birim olarak davranır. Bu şekilde yazılım kapsayıcılı hale getirmek, geliştiriciler ve BT uzmanları onları ortamlarında çok az kayıpla veya hiç değişiklik ile dağıtmak etkinleştirir.

Kapsayıcılar ayrıca paylaşılan bir işletim sisteminde uygulamaları birbirinden yalıtın. Kapsayıcılı uygulamaların, işletim sisteminde (Linux veya Windows) sırayla çalıştırılan bir kapsayıcı konağı üzerinde çalıştırın. Kapsayıcılar, bu nedenle bir çok daha küçük kaplama alanı sanal makine (VM) görüntülerini daha da içerir.

Her kapsayıcı, tüm web uygulaması veya hizmeti, Şekil 1-1'de gösterildiği gibi çalıştırabilirsiniz. Bu örnekte, Docker ana bir kapsayıcı konağı ve App1 ve App2, Svc1 ve Svc2 kapsayıcılı uygulamalar veya hizmetler şunlardır.

![İki uygulama ve işletim sisteminde bir VM veya fiziksel sunucu üzerinde çalışan iki Hizmetleri](./media/image1.png)

**Şekil 1-1**. Bir kapsayıcı konağı üzerinde çalışan birden çok kapsayıcı

Kapsayıcı türetilip bir diğer avantajı ölçeklenebilirlik özelliğidir. Hızlı bir şekilde yeni kapsayıcılar için kısa vadeli görevleri oluşturarak ölçeği genişletebilirsiniz. Bir uygulama açısından bakıldığında, örnekleme (bir kapsayıcı oluşturma) görüntü hizmeti veya web uygulaması gibi bir işlem örnekleme için benzerdir. Birden çok ana bilgisayar sunucuları arasında aynı görüntüsünün birden çok örneği çalıştırdığınızda güvenilirliği, ancak genellikle her bir kapsayıcı (farklı bir ana sunucu çalıştırmak için görüntü örnek) veya VM farklı hata etki alanlarında istersiniz.

Kısacası, kapsayıcılar arasında tüm uygulama yaşam döngüsü iş akışı yalıtımı, taşınabilirliği, çevikliği, ölçeklenebilirlik ve denetim avantajlarını sunar. En önemli avantajı, geliştirme ve Ops sağlanan ortam yalıtım olur.

>[!div class="step-by-step"]
>[Next](what-is-docker.md)
