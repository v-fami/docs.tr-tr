---
title: ODBC Veri Türü Eşlemeleri
ms.date: 03/30/2017
ms.assetid: 43c35d32-831d-480f-a150-78f7e869d17f
ms.openlocfilehash: 51090ede73710afedf74e1d2b8b5363337426279
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65584540"
---
# <a name="odbc-data-type-mappings"></a>ODBC Veri Türü Eşlemeleri
Aşağıdaki tabloda gösterilen .NET Framework türü veri türleri için .NET Framework veri sağlayıcısı için ODBC gösterilmektedir (<xref:System.Data.Odbc>). Türü belirlenmiş erişimci yöntemlerini <xref:System.Data.Odbc.OdbcDataReader> da listelenir.  
  
|ODBC türü|.NET Framework türü|.NET framework erişimci yazılan|  
|---------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|  
|SQL_BIGINT|Int64|GetInt64()|  
|SQL_BINARY|Byte[]|GetBytes()|  
|SQL_BIT|Boole değeri|GetBoolean()|  
|SQL_CHAR|Dize<br /><br /> Char]|GetString()<br /><br /> GetChars()|  
|SQL_DECIMAL|Ondalık|GetDecimal()|  
|SQL_DOUBLE|Çift|GetDouble()|  
|SQL_GUID|Guid|GetGuid()|  
|SQL_INTEGER|Int32|GetInt32()|  
|SQL_LONG_VARCHAR|Dize<br /><br /> Char]|GetString()<br /><br /> GetChars()|  
|SQL_LONGVARBINARY|Byte[]|GetBytes()|  
|SQL_NUMERIC|Ondalık|GetDecimal()|  
|SQL_REAL|Tek|GetFloat()|  
|SQL_SMALLINT|Int16|GetInt16()|  
|SQL_TINYINT|Bayt|GetByte()|  
|SQL_TYPE_TIMES|DateTime|GetDateTime()|  
|SQL_TYPE_TIMESTAMP|DateTime|GetDateTime()|  
|SQL_VARBINARY|Byte[]|GetBytes()|  
|SQL_WCHAR|Dize<br /><br /> Char]|GetString()<br /><br /> GetChars()|  
|SQL_WLONGVARCHAR|Dize<br /><br /> Char]|GetString()<br /><br /> GetChars()|  
|SQL_WVARCHAR|Dize<br /><br /> Char]|GetString()<br /><br /> GetChars()|  
  
## <a name="see-also"></a>Ayrıca bkz.

- [ADO.NET’te Veri Alma ve Değiştirme](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)
- [ADO.NET yönetilen sağlayıcıları ve DataSet Geliştirici Merkezi](https://go.microsoft.com/fwlink/?LinkId=217917)
