# Homework 2

1. 第4列和第5列分别代表该基因或转录本在参考序列上的起始和终止位置。exon长度应该是$5-$4+1。

2. ```sh
   cat 1.gtf | awk '$1 == "XI" && $3 == "CDS" {print $5}' | sort -n | tail
   
   ```
   ![Fig 1](https://github.com/qingningmengguodong/bioinfo_tsinghua/blob/master/homework2/img/fig1.png "Fig 1")

3. ```shell
   grep -v "^#" 1.gtf | awk '{print $3}' | sort | uniq -c | sort -n
   ```
   ![Fig 2](https://github.com/qingningmengguodong/bioinfo_tsinghua/blob/master/homework2/img/fig2.png "Fig 2")

   
