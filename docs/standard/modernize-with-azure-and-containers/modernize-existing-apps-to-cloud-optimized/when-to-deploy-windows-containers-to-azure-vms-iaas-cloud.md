---
title: Azure VM’lere (IaaS bulutu) Windows Kapsayıcıları ne zaman dağıtılmalıdır?
description: Azure Bulut ve Windows kapsayıcıları ile mevcut .NET uygulamalarını modernleştirme | Azure Vm'lere (Iaas Bulutu) Windows kapsayıcıları dağıtma zamanı
ms.date: 04/28/2018
ms.openlocfilehash: e9a2903662306b607977a7751018e24161ab80ab
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65638981"
---
# <a name="when-to-deploy-windows-containers-to-azure-vms-iaas-cloud"></a>Azure VM’lere (IaaS bulutu) Windows Kapsayıcıları ne zaman dağıtılmalıdır?

Ayrıca Windows kapsayıcılarını kullanıyor olsanız bile kuruluşunuz Azure Vm'leri kullanıyor, Iaas uğraşmanızı hala demektir. Bir yük dengeli altyapısında birden çok VM dağıtmak ihtiyacınız olduğunda bu uğraşmanızı altyapı işlemleri, VM işletim sistemi düzeltme ekleri ve altyapı karmaşıklığını yüksek düzeyde ölçeklenebilir uygulamalar için anlamına gelir. Bir Azure sanal Makinesinde Windows kapsayıcılarını kullanmaya yönelik temel senaryolar şunlardır:

- **Geliştirme/test ortamı**: Bir VM bulut geliştirme ve test amacıyla buluta mükemmeldir. Hızlı bir şekilde oluşturabilir veya gereksinimlerinize bağlı olarak ortamı durdurun.

- **Küçük ve orta ölçekli ölçeklenebilirlik ihtiyacı**: Düzenleyiciler gibi daha gelişmiş PaaS ortamlara taşınana kadar burada yalnızca birkaç sanal makinelerinin üretim ortamınız için ihtiyacınız olabilecek senaryolarda, uygun maliyetli az sayıda VM yönetme olabilir.

- **Üretim ortamında var olan dağıtım araçlarıyla**: Bir şirket içi ortamdan sanal makineleri veya çıplak sunucuları (örneğin, Puppet veya benzer Araçlar) karmaşık dağıtımları yapmak için Araçlar, yatırım yapmış taşıma. Üretim ortamına dağıtım yordamları için minimum değişiklikle buluta taşımak için Azure Vm'leri dağıtmak için bu araçları kullanmaya devam edebilir. Ancak, Windows kapsayıcıları dağıtım deneyimini iyileştirmek üzere dağıtım birimi olarak kullanmak isteyebilirsiniz.

>[!div class="step-by-step"]
>[Önceki](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)
>[İleri](when-to-deploy-windows-containers-to-azure-container-instances-ACI.md)
