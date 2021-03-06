---
title: Genelleştirilmiş eklenebilir modelleri ve Şekil işlevleri için model explainability kullanın
description: ML.NET içindeki model explainability için genelleştirilmiş eklenebilir modelleri ve Şekil işlevleri kullanın
ms.date: 03/05/2019
ms.custom: mvc,how-to
ms.openlocfilehash: ef56f737a2ad0cba616e32229ac3a395146fb6d2
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64662126"
---
# <a name="use-generalized-additive-models-and-shape-functions-for-model-explainability-in-mlnet"></a>ML.NET içindeki model explainability için genelleştirilmiş eklenebilir modelleri ve Şekil işlevleri kullanın

> [!NOTE]
> Bu konu şu anda Önizleme aşamasında olan ML.NET ifade eder ve malzeme değişiklik gösterebilir. Daha fazla bilgi için ziyaret [ML.NET giriş](https://www.microsoft.com/net/learn/apps/machine-learning-and-ai/ml-dotnet).

Bu nasıl yapılır ve ilgili örnek şu anda kullandığınızdan **ML.NET sürüm 0.10**. Daha fazla bilgi için bkz: adresindeki sürüm notlarını [dotnet/machinelearning GitHub deposunu](https://github.com/dotnet/machinelearning/tree/master/docs/release-notes).

Makine öğrenimi modelleri oluştururken, bunu yalnızca tahminlerde bulunmak için yeterli değil genellikle. Genellikle, makine öğrenimi geliştiriciler, karar verenler ve bu modelleri tarafından etkilenen nasıl makine öğrenme modellerini kararlar ve performanslarını için hangi özelliklerin katkıda anlamanız gerekir. **Eklenebilir modelleri (GAMs) genelleştirilmiş** dahili olarak model explainability için Microsoft machine learning geliştiriciler başkaları tarafından kolayca yorumlanabilir yüksek kapasiteli modelleri oluşturma yardımcı olmak için kullanılır.

GAMs olan bir sınıfı **yorumlanabilen modelleri** koşulları doğrusal olmayan işlevler, "işlevleri tek bir değişken, Şekil" olarak adlandırılan nerede Doğrusal Model olan. Doğrusal Model kolayca yorumlanır ancak modelleri işlevleri yerine tek bir ağırlık özellikleri öğrenmek için basit bir Doğrusal model değerinden daha karmaşık ilişkileri modelleme yapabilirsiniz. Sonuçta elde edilen GAM tahmini Ortalama tahmin Eğitim kümesi ve Ortalama tahmin sapma temsil eden şekle işlevleri temsil eden bir kesme noktası terim sahiptir. Şekil işlevleri farklı bir özellik değerlerini modelinin yanıtı görmek için göz tarafından inceledi ve kod örneği sonunda oluşturulan grafiğin aşağıdaki gibi görünür. ML.NET içinde GAM Eğitmeni gradyan artırmalı ağaçlarının sığ nonparametric şekli işlevleri öğrenin (örneğin ağacı stumps) kullanılarak uygulanır ve açıklanan yöntemi dayalı [sınıflandırma ve regresyonanlaşılırmodelleri](https://www.cs.cornell.edu/~yinlou/papers/lou-kdd12.pdf) Lou Caruana ve Gehrke tarafından.

```csharp
// Train the Generalized Additive Model
var fitPipeline = pipeline.Fit(data);
var gamModel = fitPipeline.LastTransformer.Model;

// The intercept for Generalize Additive Models represent the average prediction for the training data
var intercept = gamModel.Intercept;
Console.WriteLine($"Average predicted cost: {intercept:0.00}");

// Get the column names from the training set
var columnNames = data.Schema.AsEnumerable()
    .Select(column => column.Name) // Get the column names
    .Where(name => name != "MedianHomeValue") // Drop the Label
    .ToArray();

// Get the index of a variable from the training data
var myFeatureIndex = columnNames.ToList().FindIndex(str => str.Equals("MyFeature"));

// The shape functions represent the deviation from the average prediction as a function of the feature value
// It is represented by a discrete set of bins
// First, get the array of bin upper bounds from the model for this feature
var myFeatureBins = gamModel.GetBinUpperBounds(myFeatureIndex);
// Then get the array of bin weights; these are the effect size for each bin
var myFeatureWeights = gamModel.GetBinEffects(myFeatureIndex);

// Write out the shape function for the feature (see the following figure for what this looks like)
for (int i = 0; i < myFeatureBins.Length; i++)
{
    Console.WriteLine($"x < {myFeatureBins[i]:0.00} => {myFeatureWeights[i]:0.000}");
}
```

![Genelleştirilmiş eklenebilir modelleri şekli işlevi grafiği](./media/use-gams-for-model-explainability/gam-shape-function-graph.png)

GAM modeli eğitmek ve sonuçları yorumlamanıza incelemek nasıl bir örnek için bkz: [dotnet/machinelearning GitHub deposunu](https://github.com/dotnet/machinelearning/blob/master/docs/samples/Microsoft.ML.Samples/Dynamic/GeneralizedAdditiveModels.cs).
