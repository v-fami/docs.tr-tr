---
title: ISymUnmanagedDocument::GetSourceRange Yöntemi
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetSourceRange
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetSourceRange
helpviewer_keywords:
- ISymUnmanagedDocument::GetSourceRange method [.NET Framework debugging]
- GetSourceRange method [.NET Framework debugging]
ms.assetid: 20fefee7-1040-41ba-93dc-bd42f68b90c2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 59420cfd29c3228aece9fc5ae02b950db6099ea0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61939870"
---
# <a name="isymunmanageddocumentgetsourcerange-method"></a>ISymUnmanagedDocument::GetSourceRange Yöntemi
Katıştırılmış kaynak Belirtilen aralıktaki belirli arabelleğe döndürür. Arabellek kaynağını tutabilecek kadar büyük olmalıdır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT GetSourceRange(  
    [in]  ULONG32  startLine,  
    [in]  ULONG32  startColumn,  
    [in]  ULONG32  endLine,  
    [in]  ULONG32  endColumn,  
    [in]  ULONG32  cSourceBytes,  
    [out] ULONG32  *pcSourceBytes,  
    [out, size_is(cSourceBytes),  
        length_is(*pcSourceBytes)] BYTE source[]);  
```  
  
## <a name="parameters"></a>Parametreler  
 `startLine`  
 [in] Geçerli belgedeki başlangıç satırı.  
  
 `startColumn`  
 [in] Geçerli belgedeki başlangıç sütunu.  
  
 `endLine`  
 [in] Geçerli belgedeki son satır.  
  
 `endColumn`  
 [in] Son sütun geçerli belge.  
  
 `cSourceBytes`  
 [in] Kaynak, bayt cinsinden boyutu.  
  
 `pcSourceBytes`  
 [out] Kaynak boyutu alan bir değişken için bir işaretçi.  
  
 `source`  
 [out] Boyutu ve belirtilen kaynak belgesinde bayt aralığı uzunluğu.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem başarılı olursa S_OK.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [ISymUnmanagedDocument Arabirimi](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
