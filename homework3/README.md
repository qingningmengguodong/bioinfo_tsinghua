# Homework 3

使用Non-RefSeq protein数据库进行检索，过程和结果如下:

![alt text](https://github.com/qingningmengguodong/bioinfo_tsinghua/blob/master/img/homework3_fig2.png)

![alt text](https://github.com/qingningmengguodong/bioinfo_tsinghua/blob/master/img/homework3_fig5.png)

![alt text](https://github.com/qingningmengguodong/bioinfo_tsinghua/blob/master/img/homework3_fig6.png "Results in descriptions")

![alt text](https://github.com/qingningmengguodong/bioinfo_tsinghua/blob/master/img/homework3_fig7.png "Results in graphic summary")

再更换RefSeq protein数据库进行检索，结果如下:

![alt text](https://github.com/qingningmengguodong/bioinfo_tsinghua/blob/master/img/homework3_fig8.png)

![alt text](https://github.com/qingningmengguodong/bioinfo_tsinghua/blob/master/img/homework3_fig9.png)

通过比较发现，利用RefSeq protein数据库得到的检索结果数目明显少于利用Non-RefSeq protein数据库得到的数目。分析Non-RefSeq得到的结果，可以发现其实所有的结果代表的都是同一段序列。这是因为RefSeq protein中，对于每个DNA、RNA或蛋白质只有一条记录，而在Non-RefSeq protein中对于同一个分子可能有多条不同的记录。



PAM有对称和不对称两种形式的原因:

这张不对称的“PAM250”出现在Dayhoff教授1978年的论文中。严格来说，这个矩阵并不能称为PAM矩阵，原文的表述是“Mutation probability matrix for the evolutionary distance of 250 PAMs"。

设mutation matrix第$i$行第$j$列的元素为$M(i,j)$，氨基酸$i$出现的频率为$f(i)$，则有
$$
f(j)M(i,j)=f(i)M(j,i)
$$
利用数学归纳法可以得到
$$
f(j)M^n(i,j)=f(i)M^n(j,i)
$$
$PAM_{n}$第$i$行第$j$列的元素的计算公式为
$$
PAM_n(i,j)=\log\frac{f(j)M^n(i,j)}{f(j)f(i)}=\log\frac{f(i)M^n(j,i)}{f(i)f(j)}=PAM_n(j,i)
$$
故按此公式计算出的$PAM_n$矩阵是对称的。



---

Maximum -likelihood:

![alt text](https://github.com/qingningmengguodong/bioinfo_tsinghua/blob/master/img/max_likelihood.png)

Neighbor-joining:

![alt text](https://github.com/qingningmengguodong/bioinfo_tsinghua/blob/master/img/neighbourhood.png)

Minimum-evolution:

![alt text](https://github.com/qingningmengguodong/bioinfo_tsinghua/blob/master/img/minimum.png)

用Neighbor-joining和Minimum-evolution得到的树结构基本一致，而用Maximum-likelihood得到的树结构与其他两种方法差异较大。