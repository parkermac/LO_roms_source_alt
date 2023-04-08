# README for LO_roms_source_alt

#### This repo contains edited copies of a few pieces of the code in LO_roms_source. These are things NPZD code that could be needed by all users in the LiveOcean group to run ROMS on the hyak supercomputers (e.g. mox and klone).  We put them here to keep them out of LO_roms_source = (\*).  This is so that (\*) can stay unedited, and updated directly from the ROMS git site.
---

This directory, LO_roms_source_alt, is a git repo that you clone to klone or mox at the same level as LO, LO_roms_source, etc. It is a place for copies of ROMS code that needed edits in order to run on on those machines. There are a few categories:
- The custom bio code, npzd_banas. This has its own README.
- A version of varinfo.yaml that is copied from (*)/ROMS/External and then very lightly edited to allow python to parse it.

For all the edited code you can use diff to compare it to the original version in (*).

---

**NOTE**: if `varinfo.yaml` here is edited then you have to update its parsed version in `LO_data/varinfo/varinfo_list.p`.  There are two ways to do this.  If you just delete the directory LO_data/varinfo it will be automatically created whenever you run the forcing code.  Alternatively (easier) you could go to LO, launch ipython, and do:
```
from lo_tools import zrfun
zrfun.make_verinfo_list()
```
You would only need to do this in a place where you are making forcing files, like apogee or perigee.  When you run ROMS on hyak it uses the yaml file.

---

NOTE: As of 2023.04.08 I am putting the modified fennel.h code in the [ex_name] folder.
