# README

#### The code in this folder has various ROMS modules copied from LO_roms_source. The original, unedited, copied files are called "_ORIG" and the edited versions have the original name. The intention is that you could  and then compile to get the effect of the edits.

---

2023.07.12

The code comes from this version:
```
svn: $HeadURL: https://www.myroms.org/svn/src/trunk/ROMS/Version $
svn: $LastChangedBy: arango $
svn: $LastChangedRevision: 1122 $
svn: $LastChangedDate: 2022-04-13 12:50:43 -0700 (Wed, 13 Apr 2022) $
```

#### The intention of the edits is to introduce vertical sources that only change the tracer concentration, without adding volume.

To see places that might be involved with the vertical sources search for any occurrence of LwSrc in the source code.

To see sections I have edited, search this code for "PM Edit".

To implement these changes copy the edited files into your source code folder (being careful to save your own ORIG versions) and define LWSRC_MASS_ONLY in your cpp file before compiling.

---
