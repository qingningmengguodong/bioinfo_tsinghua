# ChIP-seq

1. findPeaks的主要参数:

   1. -style:选择特定的分析策略，例如factor(转录因子染色质免疫共沉淀测序)和histone(组蛋白修饰染色质免疫共沉淀测序)
   2. -o:输出的.peak文件的文件名，默认输出到标准输出
   3. -i:输入的tag目录

   findMotifsGenome.pl的主要参数:

   1. Region Size:用于寻找motif的区域大小，默认为200bp
   2. Motif length:想要寻找的motif的长度，可以设置多个参数，默认为8,10,12
   3. Number of motifs to find:对于每种长度的motif，想要找到的数目

2. 分析结果
   满足Fold Change(vs Control)>=8且p-value(vs Control)<1e-8的peaks存放在part_ans.peak文件中。
   满足p-value<1e-10的motif只有一个，在homerResults.html的第一行。
