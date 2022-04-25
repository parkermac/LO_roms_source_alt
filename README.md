# README for LO_roms_source_alt

#### This repo contains edited copies of a few pieces of the code in LO_roms_source. These are things NPZD code that could be needed by all users in the LiveOcean group to run ROMS on the hyak supercomputers (e.g. mox and klone).  We put them here to keep them out of LO_roms_source = (\*).  This is so that (\*) can stay unedited, and updated directly from the ROMS git site.
---

This directory, LO_roms_source_alt, is a git repo that you clone to klone or mox at the same level as LO, LO_roms_source, etc. It is a place for copies of ROMS code that needed edits in order to run on on those machines. There are a few categories:
- The custom bio code, npzd_banas. This has its own README.
- A version of varinfo.yaml that is copied from (*)/ROMS/External and then very lightly edited to allow python to parse it.

For all the edited code you can use diff to compare it to the original version in (*).
