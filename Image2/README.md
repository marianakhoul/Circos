# Image 2

The image shows the links between chromosomes for Structural Variant data and the heatmap represents the Copy Number Variant data.

## Inputs
The input files:

**segdup.bundle1.txt** file has the following format
```
chr1 10 20 chr2 400 450 color=blue
chr3 1029 2000 chr14 88292982 9292881 color=pink
```

The **heatmap** file has the following format
```
hs1 903175 16549912 3.452042253
hs1 16549913 16948171 3.91318101
hs1 16948172 121699999 3.502179318
hs1 125100001 234777446 3.502179318
```
Chromosome, start, end, CNV value

The Karyotype file used for the bands around the image were from the circos package found in **data/karyotype/karyotype.human.hg38.txt** since the data was mapped to hg38.

## Heatmap
The heatmap was added using the following code block. r1 and r2 represent where the heatmap portion would lie with respect to the bands. rules gave the red, blue, grey coloring of the CNV with red being amplification and blue being deletions.
```
<plots>
<plot>
type 		   = heatmap
file 		   = data/heatmap.txt
r1      = 0.975r
r0      = 0.9r

<rules>
<rule>
condition	  = var(value)>=0 && var(value) <1
color 		  = vdblue
</rule>
<rule>
condition	  = var(value)>=1 && var(value) <1.5
color 		  = lblue
</rule>
<rule>
condition	  = var(value)>=1.5 && var(value) <2.5
color 		  = vlgrey
</rule>
<rule>
condition	  = var(value)>=2.5 && var(value) <3.5
color 		  = lred
</rule>
<rule>
condition	  = var(value)>=3.5
color 		  = vdred
</rule>
</rules>
</plot>
</plots>
```


