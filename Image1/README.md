# Image 1

The image shows the links between chromosomes for Structural Variant data. 

### Inputs
The input file **segdup.bundle1.txt** file has the following format
```
chr1 10 20 chr2 400 450 color=blue
chr3 1029 2000 chr14 88292982 9292881 color=pink
```
Each type of structural variant was given a color and the ones which weren't of importance got the color black.

The Karyotype file used for the bands around the image were from the circos package found in **data/karyotype/karyotype.human.hg38.txt** since the data was mapped to hg38.

### Links
thickness    = 10 to give more bold links between the chromosomes

### Ideogram

The default space was changed to 0.006r to have less space between the bands of the chromosomes.
```
<spacing>
default = 0.006r
#break   = 0.01r
</spacing>
```

### Labels
To have the chromosomes in the direction they are headed around the plot.
If set to yes, the chromosomes would be perpendicular to their associated bands
```
label_parallel   = no
```
Bold font was chosen as follows
```
label_font       = bold
```

### Chromosomes
By specifying the following, we excluded chromosome Y since this is a female.
```
chromosomes                 = -hsY
```
