---
title: SqlStreamChars.Seek (Int64, SeekOrigin) yöntemi (System.Data.SqlTypes)
author: stevestein
ms.author: sstein
ms.date: 12/20/2018
ms.technology: dotnet-data
topic_type:
- apiref
api_name:
- System.Data.SqlTypes.SqlStreamChars.Seek
api_location:
- System.Data.dll
api_type:
- Assembly
ms.openlocfilehash: 6b69f87da9fb3829d765dc135de1f6c10765b63a
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65634355"
---
# <a name="sqlstreamcharsseekint64-seekorigin-method"></a>(Int64, SeekOrigin) SqlStreamChars.Seek yöntemi

Türetilen bir sınıfta geçersiz kılındığında, geçerli akış içinde konumunu ayarlar. Bu yöntemi içeren derlemenin SQLAccess.dll bir arkadaş ilişkisi vardır. Bu, SQL Server tarafından kullanıma yöneliktir. Diğer veritabanları için veritabanı tarafından sağlanan barındırma mekanizmasına kullanın.

```csharp
public abstract long Seek (long offset, System.IO.SeekOrigin origin);
```

## <a name="parameters"></a>Parametreler

`offset`\
Göreli bir bayt uzaklığı `origin`.

`origin`\
Yeni konumunu alınacağı başvuru noktası belirten numaralandırma değerlerinden biri.

## <a name="returns"></a>Döndürür

<xref:System.Int32>\
Geçerli akışındaki yeni konumu.

## <a name="remarks"></a>Açıklamalar

> [!WARNING]
> `SqlStreamChars.Seek` Yöntemi private olduğuna ve kodunuzda doğrudan kullanılmak üzere tasarlanmamıştır.
>
> Microsoft hiçbir koşulda, bir üretim uygulamasında bu alanı kullanımını desteklemez.

## <a name="requirements"></a>Gereksinimler

**Namespace:** <xref:System.Data.SqlTypes>

**Derleme:** System.Data (içinde System.Data.dll)

**.NET framework sürümleri:** 2.0 sürümünden itibaren kullanılabilir.
