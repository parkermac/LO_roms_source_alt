# README for npzd_banas

#### This is edited npzd code to use with LiveOcean.

---

It is copied from the ROMS/Nonlinear/Biology folder of revision 1099, January 2022, after the introduction of varinfo.yaml.

I have also copied in ROMS/External/bio_Fennel.in and varinfo.dat.


Then these files were edited to retain the Fennel code, including NH4 and Chl variables, but modifying the parameters in the .in and the equations in fennel.h to reproduce the Banas/Siedlecki/Davis model as closely as possible, while allowing a separate NH4 pool.

All changes in the .h code are denoted with:
```
! PM Edit
[new code]
! End PM Edit
```

The fundamental edits occur in:
- fennel.h where I make changes to the npzd functions to reproduce the Banas/Siedlecki/Davis model.
- bio_Fennel.in where I make changes to the parameter values.  We strictly retain the parameter names because they are baked-into all the other code and so it is much easier to keep them.
- bio_Fennel_BLANK.in has a few more edits to the new bio_Fennel.in to allow it to be used in the dot_in code.  This mainly involved allowing for automated specification of boundary conditions, and turning on tracer sources and climatology.
- NOTE: varinfo.yaml may need a few additional entries to work with the Fennel code.  I think this reflects a bug in the ROMS source code.
