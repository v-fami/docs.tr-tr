---
ms.openlocfilehash: 566a3e0455b30e901b09be88b4256ffe67bdc2b5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61664975"
---
### <a name="workflow-sql-persistence-adds-primary-key-clusters-and-disallows-null-values-in-some-columns"></a>İş akışı SQL kalıcılığını birincil anahtar kümeleri ve bazı sütunları null değerleri izin vermiyor ekler.

|   |   |
|---|---|
|Ayrıntılar|.NET Framework 4.7 ile başlayarak, SQL iş akışı örneği Store (SWIS) için SqlWorkflowInstanceStoreSchema.sql betiği tarafından oluşturulan tablolarda kümelenmiş birincil anahtarları kullanın. Bu nedenle, kimlikleri desteklemez <code>null</code> değerleri. SWIS işlemi, bu değişiklikten etkilenmez. SQL Server işlem çoğaltmayı desteklemek için güncelleştirmeleri yapıldı.|
|Öneri|Bu değişiklik deneyimi için SQL dosyası SqlWorkflowInstanceStoreSchemaUpgrade.sql var olan yüklemeler için uygulanması gerekir. Yeni veritabanı yüklemelerini değişikliği otomatik olarak sahip olur.|
|Kapsam|Kenar|
|Sürüm|4.7|
|Tür|Çalışma zamanı|
