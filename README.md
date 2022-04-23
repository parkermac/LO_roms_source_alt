# README for LO_roms_source_alt

---

(*) = LO_roms_source

This directory, LO_roms_source_alt, is a git repo that you clone to klone at the same level as LO, LO_roms_source, etc. It is a place for copies of ROMS code that I need to edit. There are a few categories:
- The compiler instructions, copied from (*)/Compilers.
- The custom bio code, which goes in npzd_banas. This has its own README.
- A lightly modified varinfo.yaml.

For all the edited code you can use diff to compare it to the original version in (*).

---

#### npzd_banas

This folder started as copies of the Fennel code in (*)/ROMS/Nonlinear/Biology. It also includes External/bio_Fennel.in. Then these files were edited to retain the Fennel code, including NH4 and Chl variables, but modifying the parameters in the .in and the equations in fennel.h to reproduce the Banas/Siedlecki/Davis model as closely as possible, while allowing a separate NH4 pool. All changes in the .h code are denoted with:
```
! PM Edit
[new code]
! End PM Edit
```
The first test of using this will be the uu0kb executable.
