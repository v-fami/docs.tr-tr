---
title: ISymUnmanagedBinder3::GetReaderFromCallback Metodu
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder3.GetReaderFromCallback
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder3::GetReaderFromCallback
helpviewer_keywords:
- GetReaderFromCallback method [.NET Framework debugging]
- ISymUnmanagedBinder3::GetReaderFromCallback method [.NET Framework debugging]
ms.assetid: 4ef83bd2-3d8e-499e-8a12-d9d6fd6ced30
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9487cf89d87b5f373302dc49a08c4fabb719e746
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61940016"
---
# <a name="isymunmanagedbinder3getreaderfromcallback-method"></a>ISymUnmanagedBinder3::GetReaderFromCallback Metodu
Uygulama veya geri çağırma ya da kaynağı izin verir bir `IID_IDiaReadExeAtRVACallback` veya `IID_IDiaReadExeAtOffsetCallback` bellekten hata ayıklama dizin bilgileri elde edilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT GetReaderFromCallback(  
    [in]  IUnknown     *importer,  
    [in]  const WCHAR  *fileName,  
    [in]  const WCHAR  *searchPath,  
    [in]  ULONG32      searchPolicy,  
    [in]  IUnknown     *callback,  
    [out,retval] ISymUnmanagedReader  **pRetVal);  
```  
  
## <a name="parameters"></a>Parametreler  
 `importer`  
 [in] Meta veri alma arayüzü işaretçisi.  
  
 `fileName`  
 [in] Dosya adı için bir işaretçi.  
  
 `searchPath`  
 [in] Arama yolu için bir işaretçi.  
  
 `searchPolicy`  
 [in] Değerini [CorSymSearchPolicyAttributes](../../../../docs/framework/unmanaged-api/diagnostics/corsymsearchpolicyattributes-enumeration.md) sembol Okuyucu için arama yaparken kullanılacak ilkeyi belirten sabit listesi.  
  
 `callback`  
 [in] Geri çağırma işlevi için bir işaretçi.  
  
 `pRetVal`  
 [out] Ayarlanmış bir işaretçi ve döndürülen [Isymunmanagedreader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) arabirimi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem başarılı olursa S_OK; Aksi takdirde, E_FAIL veya başka bir hata kodu.  
  
## <a name="requirements"></a>Gereksinimler  
 **Üst bilgi:** CorSym.idl  
  
## <a name="see-also"></a>Ayrıca bkz.

- [ISymUnmanagedBinder3 Arabirimi](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder3-interface.md)
