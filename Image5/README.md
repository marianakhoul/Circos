# Image 5

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
