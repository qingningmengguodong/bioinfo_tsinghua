# Homework5 GO

1.选取了前40个基因进行GO enrichment分析。分析结果如图所示

![alt text]( https://github.com/qingningmengguodong/bioinfo_tsinghua/blob/master/img/enrichment.png )

* 通过和数据库比对，我们可以知道在数据库参考基因组的20996个基因中，被注释为regulation of mRNA stability的有180个，在用户上传的40个可以识别的基因中有5个基因有同样的注释。
* $$ expected=180*5/20996=0.34$$
* $$Fold Erichment=8/0.63=12.72$$
* $rawPvalue=\frac{{n\choose k}{N-n\choose K-k}}{N\choose K}=\frac{{40\choose 5}{20956\choose 175}}{20996\choose 180}=2.55E-05$

2.