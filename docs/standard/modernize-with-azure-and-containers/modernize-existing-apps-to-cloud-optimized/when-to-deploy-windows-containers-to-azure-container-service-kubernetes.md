---
title: Azure Container Service (Kubernetes) için Windows kapsayıcıları dağıtma zamanı
description: Azure Bulut ve Windows kapsayıcıları ile mevcut .NET uygulamalarını modernleştirme | Azure Container Service (Kubernetes) için Windows kapsayıcıları dağıtma zamanı
ms.date: 04/30/2018
ms.openlocfilehash: 921767b52f2b0d80f2d31d972b65ac7551d2f7c5
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65643566"
---
# <a name="when-to-deploy-windows-containers-to-azure-container-service-that-is-kubernetes"></a>Azure Container Service (Kubernetes) için Windows kapsayıcıları dağıtma zamanı

Azure kapsayıcı hizmeti popüler açık kaynaklı araçların ve teknolojilerin yapılandırmasını özellikle Azure'a yönelik en iyi duruma getirir. Hem kapsayıcılarınız için hem de uygulama yapılandırmanız için taşınabilirlik sunan bir açık çözümü sahip olursunuz. Boyutu, konak sayısını ve düzenleyici araçlarını seçmeniz. Azure Container Service, altyapı sizin yerinize çözer.

Zaten açık kaynak düzenleyicileri Kubernetes, Docker Swarm veya DC/OS gibi çalışıyorsanız kapsayıcı iş yüklerini buluta taşımak için mevcut yönetim uygulamalarınızı değiştirmeniz gerekmez. Zaten alışkın olduğunuz uygulama yönetimi araçlarını kullanın ve tercih ettiğiniz orchestrator için standart API uç noktaları aracılığıyla bağlanın.

Linux Docker kapsayıcılarını kullanarak ancak yalnızca Windows kapsayıcıları için Önizleme durumunda olabilir, bu düzenleyicileri olgun ortamları vardır.

Kapsayıcılar için Kubernetes, örneğin, destek yerel (birinci sınıf Vatandaşlık), Windows kapsayıcıları azure'da Kubernetes kullanarak etkin (önizlemede ACS erken 2018'den itibaren) de.

Önemli Not: Sistem gereksinimleri ve "daha fazla PaaS" sürümüdür (Azure Container Service) bir ACS kubernetes AKS (Azure Kubernetes hizmeti), ancak Windows kapsayıcıları hala desteklenmez S2 2018'den itibaren ancak yakında desteklenecek.

>[!div class="step-by-step"]
>[Önceki](when-to-deploy-windows-containers-to-service-fabric.md)
>[İleri](choosing-azure-compute-options-for-container-based-applications.md)
