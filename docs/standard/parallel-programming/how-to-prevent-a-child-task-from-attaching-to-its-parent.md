---
title: 'Nasıl yapılır: Alt Görevin Üst Göreve Eklenmesini Önleme'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- tasks, preventing attachments
ms.assetid: c0fb85d4-9e80-4905-9f65-29acc54201c4
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 55b9c6c7175d8c7c33d8bfa03330c8e4b8816531
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65592018"
---
# <a name="how-to-prevent-a-child-task-from-attaching-to-its-parent"></a>Nasıl yapılır: Alt Görevin Üst Göreve Eklenmesini Önleme
Bu belge, bir alt görevin üst göreve eklenmesini önleme gösterilmiştir. Bir üçüncü taraf tarafından yazılan ve görevleri de kullanan bir bileşen çağırdığınızda, bir alt görevin üst göreve eklenmesini önleme yararlıdır. Örneğin, kullanan bir üçüncü parti bileşeniniz <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent?displayProperty=nameWithType> oluşturma seçeneği bir <xref:System.Threading.Tasks.Task> veya <xref:System.Threading.Tasks.Task%601> nesne sorunlara neden olabilir, kodunuzda uzun süreli veya işlenmeyen bir özel durum oluşturur.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, bir alt görevin üst göreve eklenmesini önleme etkileri için varsayılan seçenekleri kullanarak etkilerini karşılaştırır. Örnek bir <xref:System.Threading.Tasks.Task> de kullanan bir üçüncü taraf kitaplığına çağıran bir nesne bir <xref:System.Threading.Tasks.Task> nesne. Üçüncü taraf kitaplığı kullandığını <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent> oluşturma seçeneği <xref:System.Threading.Tasks.Task> nesne. Uygulamanın kullandığı <xref:System.Threading.Tasks.TaskCreationOptions.DenyChildAttach?displayProperty=nameWithType> üst görev oluşturma seçeneği. Bu seçeneği kaldırmak için çalışma zamanı bildirir <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent> alt görevlerdeki belirtimi.  
  
 [!code-csharp[TPL_DenyChildAttach#1](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl_denychildattach/cs/denychildattach.cs#1)]
 [!code-vb[TPL_DenyChildAttach#1](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl_denychildattach/vb/denychildattach.vb#1)]  
  
 Tüm alt görevler tamamlanıncaya kadar bir üst görev sonlanmaz, uzun süre çalışan alt görev genel uygulamanın sonlanmayacağından neden olabilir. Uygulama, üst görev oluşturmak için varsayılan seçenekleri kullandığında bu örnekte, alt görev üst görev tamamlanmadan önce tamamlanmalıdır. Uygulama kullandığında <xref:System.Threading.Tasks.TaskCreationOptions.DenyChildAttach?displayProperty=nameWithType> seçeneği, alt üst öğeye bağlı değil. Bu nedenle, uygulamanın ek iş üst görev tamamlandıktan sonra ve son alt görevin tamamlanmasını beklemelisiniz önce gerçekleştirebilirsiniz.  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Görev Tabanlı Zaman Uyumsuz Desen](../../../docs/standard/parallel-programming/task-based-asynchronous-programming.md)
