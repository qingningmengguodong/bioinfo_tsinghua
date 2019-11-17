# Homework5 KEGG

同: 都反应了这些基因产物的生物学功能。

异: 二者分析的角度和侧重点不同。

GO是一个树状的结构，根节点为cellular component(CC)，Molecular function(MF), Biological process(BP)。树上的每个结点是一个term(annotation)，一个结点可以包括许多基因，同样的一个基因也拥有多个terms(annotations)。GO的富集分析结果主要体现了用户提供的数据集中，拥有哪些terms的基因最多。

KEGG是一个网状的数据库，由很多张代谢通路图组成。KEGG的分析结果可以以基因为单位，显示的是该基因出现在哪些代谢通路中；也可以以代谢通路图为单位，显示该通路中包含哪些用户提供的基因。