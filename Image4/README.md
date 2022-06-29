# Image 4
The image shows the links between chromosomes for Structural Variant data. The links also have the gene names associated with them on the band edges.

## Chromosome Subset
To display the subset of chromosomes, first set **chromosomes_display_default = no** and then list the chromosomes separated by ;.
```
chromosomes_display_default = no
chromosomes                 = hs1;hs17;hs22;hsX
```

## Link data 
**segdup.bundle2.txt** file has the following format
```
hsX 49037901 49037901 hsX 71299453 71299453 color=blue
hsX 49036303 49036303 hs17 82002033 82002033 color=vvdyellow
hsX 49034295 49034295 hs1 35181558 35181558 color=red
hsX 49034299 49034299 hs1 35181562 35181562 color=black
```

## Text data for the links
**gene_name.txt** looks as follows. Make sure the gene_name.txt has the same chromosomes and positions as the **segdup.bundle2.txt** file and same colors.
```
hsX 71299453 71299453 NONO color=blue
hs17 82002033 82002033 ASPCR1 color=vvdyellow
hs1 35181558 35181558 SFPQ color=red
hsX 47183133 47183133 RBM10 color=green
```

## Gene Name Marks
Plot type = text is how we add the gene names
```
<plots>
<plot>
type             = text
file             = data/gene_name.txt
r0 = 1.02r
r1 = 1.2r
label_font = light
label_size = 50p
rpadding   = 5p

</plot>
</plots>

```
