# Image 3
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

## Links
The links are longer and more visible in this picture.
```
bezier_radius        = 0.05r
```
The larger the number the smaller the link.
