---
title: IWpfHostSupport
ms.date: 03/30/2017
helpviewer_keywords:
- IWpfHostSupport interface [WPF]
ms.assetid: cc5a0281-de81-4cc1-87e4-0e46b1a811e9
ms.openlocfilehash: 97a120c57624ada32e6661bd8a613c4ea1d01b2f
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64591379"
---
# <a name="iwpfhostsupport"></a>IWpfHostSupport
Barındıran uygulamalar [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] PresentationHost.exe üzerinden içerik PresentationHost.exe ve konak arasında tümleştirme noktası sağlamak için bu arabirimi uygulayın.  
  
## <a name="remarks"></a>Açıklamalar  
 [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] Web tarayıcıları gibi uygulamaları barındırabilir [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] dahil olmak üzere içerik [!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)] ve XAML kaybedilir. Ana bilgisayara [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] içerik [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] uygulamaları oluşturma örneği [WebBrowser denetimi](https://go.microsoft.com/fwlink/?LinkId=97911). Barındırılması için [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] barındırılan sağlayan PresentationHost.exe örneği oluşturur [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] görüntülemek için ana içerik [WebBrowser denetimi](https://go.microsoft.com/fwlink/?LinkId=97911).  
  
 Tarafından etkinleştirilen tümleştirme `IWpfHostSupport` için PresentationHost.exe sağlar:  
  
- Bul ve ana bilgisayar uygulaması, ilgileniyor ham giriş cihazları (İnsan Arabirimi cihazlar) ile kaydedin.  
  
- Giriş iletileri ham giriş cihazlar kayıtlı ve uygun iletileri yönlendirmek için ana bilgisayar uygulaması alabilir.  
  
- Konak uygulama özel ilerleme durumu ve hata kullanıcı arabirimleri için sorgu.  
  
> [!NOTE]
>  Bu API yalnızca hedeflenen ve yerel istemci makinesinde kullanımı desteklenen  
  
## <a name="members"></a>Üyeler  
  
|Üye|Açıklama|  
|------------|-----------------|  
|[GetRawInputDevices](getrawinputdevices.md)|Ana bilgisayar uygulaması, ilgileniyor ham giriş cihazlarını (İnsan Arabirimi aygıtları) bulma PresentationHost.exe sağlar.|  
|[FilterInputMessage](filterinputmessage.md)|E_NOTIMPL sürece bir ileti alındığında PresentationHost.exe tarafından çağrılır.|  
|[GetCustomUI](getcustomui.md)|Varsayılan olarak, kendi dağıtımının ilerleme durumunu ve dağıtım hata PresentationHost.exe WPF içeriği dağıtıldığında görüntülenen kullanıcı arabirimleri sağlar.|
