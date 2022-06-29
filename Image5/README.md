# Image 5
The image shows the links between chromosomes for Structural Variant data and the heatmap represents the Copy Number Variant data.

## Inputs
The input file **segdup.bundle3.txt** looks the following way
```
hs1 123266415 123266415 hs1 123804771 123804771 value=Deletion
hs1 216779533 216779533 hs4 175434662 175434662 value=Trans-Bal
hs1 226886137 226886137 hs5 98845601 98845601 value=Trans-Unbal
hs1 90802171 90802171 hs6 32501058 32501058 value=Trans-Bal
hs1 231359214 231359214 hs18 34947190 34947190 value=Trans-Bal
```
Value represents the SV type.

## Rules
The following rules were added inside the **Link** block to add conditional coloring based on the value inside the input file. It will color the different SV types. The first condition for the between hs1,hsX is red and thicker because we want this link to stand out. Needs to be added first because if satisfies a different condition, will follow rules of that condition first.
```
<rules>
<rule>
condition    = between(hs1,hsX)
color 		   = vdred
thickness    = 20
</rule>
<rule>
condition	   = var(value) eq "Deletion"
color 		   = vvdyellow
</rule>
<rule>
condition	   = var(value) eq "Balanced"
color 		   = blue
</rule>
<rule>
condition	   = var(value) eq "Unbalanced"
color 		   = orange
</rule>
<rule>
condition	   = var(value) eq "Trans-Bal"
color 		   = green
</rule>
<rule>
condition	   = var(value) eq "TandemDup"
color 		   = purple
</rule>
<rule>
condition	   = var(value) eq "Trans-Unbal"
color 		   = vdblue
</rule>
<rule>
condition	   = var(value) eq "Inversion-Foldback"
color 		   = vdpurple
</rule>
<rule>
condition	   = var(value) eq "Inversion-Bal"
color 		   = chr19
</rule>
<rule>
condition	   = var(value) eq "Inversion-Unbal"
color 		   = grey
</rule>
</rules>
```
