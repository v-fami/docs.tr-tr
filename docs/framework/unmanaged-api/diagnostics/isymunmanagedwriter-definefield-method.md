---
title: ISymUnmanagedWriter::DefineField Yöntemi
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineField
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineField
helpviewer_keywords:
- ISymUnmanagedWriter::DefineField method [.NET Framework debugging]
- DefineField method, ISymUnmanagedWriter interface [.NET Framework debugging]
ms.assetid: c6a1f797-dbf4-40f5-ab99-d9b4bfb26148
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5fd9798b3681d66e71d5703f4d16564b153da07b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789636"
---
# <a name="isymunmanagedwriterdefinefield-method"></a>ISymUnmanagedWriter::DefineField Yöntemi
Bir yöntem içinde değil tek bir değişkeni tanımlar. Bu, kullanılan belirli alanları sınıflarda, bit alanları ve benzeri yöntemidir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT DefineField(  
    [in] mdTypeDef    parent,  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] ULONG32      cSig,  
    [in, size_is(cSig)] unsigned char signature[],  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3);  
```  
  
## <a name="parameters"></a>Parametreler  
 `parent`  
 [in] Meta veri türünde veya yönteminde ' belirteci.  
  
 `name`  
 [in] Alan adı.  
  
 `attributes`  
 [in] Alan öznitelikleri.  
  
 `cSig`  
 [in] A `ULONG32` alan imzası içermesi gereken arabelleğin karakter cinsinden boyutu diğer bir deyişle.  
  
 `signature`  
 [in] Alan imzaları dizisi.  
  
 `addrKind`  
 [in] Adres türü.  
  
 `addr1`  
 [in] İlk adres alanı belirtimi için.  
  
 `addr2`  
 [in] İkinci bir adres alanı belirtimi için.  
  
 `addr3`  
 [in] Üçüncü adres alanı belirtimi için.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem başarılı olursa S_OK; Aksi takdirde, E_FAIL veya başka bir hata kodu.  
  
## <a name="requirements"></a>Gereksinimler  
 **Üst bilgi:** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Ayrıca bkz.

- [ISymUnmanagedWriter Arabirimi](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
