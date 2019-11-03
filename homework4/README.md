# Homework4

首先将`/home/test/share`文件夹下的`THA2.fa`与`e_coli_500.fq`拷贝到工作目录`/home/test/mapping`中（以下代码在`/home/test/share`中运行）

 ```bash
cp THA2.fa /home/test/share
cp e_coli_500.fq /home/test/share
 ```

按照教程中给出的方法进行mapping

```
bowtie -v 2 -m 10 --best --strata BowtieIndex/YeastGenome -f THA2.fa -S THA2.sam

bowtie -v 1 -m 10 --best --strata bowtie-src/indexes/e_coli \
    -q e_coli_500.fq -S e_coli_500.sam
```

将`.sam`处理成`.bed`格式

```
perl sam2bed.pl THA2.sam > THA2.bed
perl sam2bed.pl e_coli_500.sam > e_coli_500.bed
```

按照题目要求进行筛选

```
grep -v $'chrV\t' THA2.bed > THA2_no_chrV.bed

grep $'chrXII\t' THA2.bed > THA2_chrXII.bed
```

最后统计两个文件的行数

```
wc -l THA2_no_chrV.bed
wc -l THA2_chrXII.bed
```

结果`THA2_no_chrV.bed`有1158行，`THA2_chrXII.bed`有169行。