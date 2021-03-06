---
title: Özyinelemeli Yordamlar (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], that call themselves
- procedures [Visual Basic], recursive
- procedures [Visual Basic], calling
- recursive procedures
- functions [Visual Basic], calling recursively
- recursion
ms.assetid: ba1d3962-b4c3-48d3-875e-96fdb4198327
ms.openlocfilehash: de9a2af9fc3cd78879b6525245727a6f52d51c63
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61791852"
---
# <a name="recursive-procedures-visual-basic"></a>Özyinelemeli Yordamlar (Visual Basic)
A *özyinelemeli* yordam, kendi kendini çağıran bir kullanılır. Genel olarak, Visual Basic kod yazmak için en etkili yolu değil.  
  
 Aşağıdaki yordam, özgün bağımsız değişkeninin faktöriyelini hesaplamak için özyineleme kullanır.  
  
 [!code-vb[VbVbcnProcedures#51](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#51)]  
  
## <a name="considerations-with-recursive-procedures"></a>Özyinelemeli yordamlar hakkında konuları  
 **Koşullar sınırlama**. Özyineleme sonlandırabilirsiniz en az bir koşul için test etmek için bir özyinelemeli yordamı tasarlamanız gerekir ve ayrıca burada herhangi bir koşul makul bir özyinelemeli çağrıların sayısı içinde sağlanırsa durum işlemesi gerekir. Başarısız karşılanabiliyorsa en az bir koşul olmadan yordamınız sonsuz bir döngüde yürütmenin bir yüksek riskli çalıştırır.  
  
 **Bellek kullanımı**. Uygulamanızı yerel değişkenler için alan sınırlı bir süre vardır. Bir yordam kendisini çağıran her zaman daha bu alan yerel değişkenlerini ek kopyalarını kullanır. Bu işlem süresiz olarak devam ederse, sonunda neden olan bir <xref:System.StackOverflowException> hata.  
  
 **Verimliliği**. Neredeyse her zaman bir döngü için özyineleme birbirinin yerine kullanabilir. Bir döngü, ek depolama alanı'nı başlatma ve değerler döndüren argümanları başlatır, yükü yok. Performansınızı özyinelemeli çağrılar çok daha iyi olabilir.  
  
 **Karşılıklı özyineleme**. Her iki yordam çağırırsanız çok kötü performans veya hatta bir sonsuz döngüye mümkün görebilirsiniz. Bu tür bir tasarım tek özyinelemeli yordamla aynı oluşturur, ancak algılama ve hata ayıklamayı daha zor olabilir.  
  
 **Parantezler ile çağırma**. Olduğunda bir `Function` yordam çağrıları kendisini yinelemeli olarak, hiçbir bağımsız değişken listesi olsa bile, parantezli yordam adı izlemelidir. Aksi halde, işlev adı alınmış işlevinin dönüş değerini temsil eden olarak.  
  
 **Test**. Bir özyinelemeli yordam yazarsanız, bu çok dikkatli bir şekilde her zaman bir sınırlama bazı koşullar karşıladığından emin olmak için test etmelisiniz. Ayrıca, özyinelemeli çağrı sayısı çok fazla olması nedeniyle bellek yetersiz çalıştıramazsınız emin olmalısınız.  
  
## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.StackOverflowException>
- [Yordamlar](./index.md)
- [Alt Yordamlar](./sub-procedures.md)
- [İşlev Yordamları](./function-procedures.md)
- [Özellik Yordamları](./property-procedures.md)
- [İşleç Yordamları](./operator-procedures.md)
- [Yordam Parametreleri ve Bağımsız Değişkenleri](./procedure-parameters-and-arguments.md)
- [Yordam Aşırı Yüklemesi](./procedure-overloading.md)
- [Yordam Sorunlarını Giderme](./troubleshooting-procedures.md)
- [Döngü Yapıları](../../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)
