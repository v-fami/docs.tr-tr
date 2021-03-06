---
title: Güvenlik ve Serileştirme
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- code security, serialization
- serialization, security
- secure coding, serialization
- security [.NET Framework], serialization
ms.assetid: b921bc94-bd3a-4c91-9ede-2c8d4f78ea9a
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c275e7179daf0dfdf2dda8bf364a4682565f28a6
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64596726"
---
# <a name="security-and-serialization"></a>Güvenlik ve Serileştirme
Serileştirme bakın veya erişilemez Aksi durumda olacak nesne örneği verileri değiştirmek başka bir kod izin vermek için özel bir izin serileştirme gerçekleştiren kod gereklidir: <xref:System.Security.Permissions.SecurityPermission> ile <xref:System.Security.Permissions.SecurityPermissionFlag.SerializationFormatter> bayrağı belirtilmiş. Varsayılan ilkesi altında çok Internet karşıdan bu izin verilmez veya intranet kodu; yalnızca yerel bilgisayarda kod bu izin verilir.  
  
 Normalde, bir nesne örneğinin tüm alanlar veri örneği için seri duruma getirilmiş verilerde temsil edilen anlamı serileştirilir. Veri değerleri, üyenin erişilebilirliğini bağımsız nelerdir belirlemek için biçim yorumlayabilir kodunu mümkündür. Benzer şekilde, seri durumundan çıkarma serileştirilmiş temsilinden verileri ayıklayan ve nesne durumu doğrudan yeniden erişilebilirlik kuralları bağımsız olarak ayarlar.  
  
 Güvenlik açısından duyarlı verileri içerebilen herhangi bir nesne nonserializable, mümkünse yapılmalıdır. Hassas verileri nonserializable tutun belirli alanlar seri hale getirilebilir olması gerekir, deneyin. Bu yapılamaz, bu verileri seri hale getirmek ve kötü amaçlı bir kodun bu izin alabilirsiniz emin olmak için izni olan herhangi bir kod sunulan dikkat edin.  
  
 <xref:System.Runtime.Serialization.ISerializable> Arabirimi, yalnızca seri hale getirme altyapısı tarafından kullanılmak üzere tasarlanmıştır. Ancak, korumasız, potansiyel olarak hassas bilgileri serbest bırakabilirsiniz. Özel serileştirme uygulayarak sağlarsanız **ISerializable**, aşağıdaki önlemleri dikkate aldığınızdan emin olun:  
  
- <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A> Yöntemi açıkça güvenli yoğun ya da **SecurityPermission** ile **SerializationFormatter** göre yaparak emin olan ya da belirtilen izni yok duyarlı bilgi yöntemi çıkış ile serbest bırakılır. Örneğin:  
  
    ```vb  
    Public Overrides<SecurityPermissionAttribute(SecurityAction.Demand, SerializationFormatter := True)>  _  
    Sub GetObjectData(info As SerializationInfo, context As StreamingContext)  
    End Sub  
    ```  
  
    ```csharp  
    [SecurityPermissionAttribute(SecurityAction.Demand,SerializationFormatter   
    =true)]  
    public override void GetObjectData(SerializationInfo info,   
    StreamingContext context)  
    {  
    }  
    ```  
  
- Serileştirme için kullanılan özel bir oluşturucu ayrıca kapsamlı giriş doğrulaması gerçekleştirmeniz ve kötü amaçlı kod tarafından kötüye karşı korumaya yardımcı olmak için özel veya korumalı olmalıdır. Aynı güvenlik denetimleri ve açıkça sınıfı oluşturma veya Fabrika tür üzerinden dolaylı olarak oluşturma gibi diğer araçları, böyle bir sınıfın bir örneği elde etmek için gerekli izinler uygulaması gerekir.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Güvenli Kodlama Yönergeleri](../../../docs/standard/security/secure-coding-guidelines.md)
