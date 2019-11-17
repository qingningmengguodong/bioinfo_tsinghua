# Homework6 Differential Expression

1. Normalization。不同的芯片/通道拥有不同的强度值，为了比较它们的分布，我们需要对数据进行归一化。这与协方差和相关系数之间的关系是一样的。
2. Multiple testing correction(P value校正)。最常用的是Bonferroni法，它的思想是调整检验水准，根据比较的指标个数重新设定检验水准。 这样做的理由是基于这样一个事实：在同一数据集上进行多个假设的检验，每20个假设中就有一个可能纯粹由于概率而达到0.05的显著水平。 