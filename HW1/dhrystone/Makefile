# Dhrystone V2.1 and V1.1 Makefile.
DEFINES = -DUNIX
FLAGS = $(DEFINES) -O2
FILEA = Makefile dhry.doc dhryrun.doc dhry.h dhry21a.c
FILES = $(FILEA) dhry21b.c dhry11.c timers_b.c dhry.bat input

GCC = gcc $(FLAGS)

dhry21   : dhry21a.c dhry21b.c dhry.h timers_b.c
	   $(GCC) dhry21a.c dhry21b.c timers_b.c -o dhry21

dhry11   : dhry11.c timers_b.c
	   $(GCC) dhry11.c timers_b.c -o dhry11

MANIFEST : $(FILES)
	   ls -l $(FILES) > MANIFEST

shar     : $(FILES) MANIFEST
	   shar -o dhry.shar MANIFEST $(FILES)

tar      : $(FILES) MANIFEST
	   tar -cf dhry.tar MANIFEST $(FILES)
	   compress dhry.tar
	   uuencode dhry.tar.Z dhry.tar.Z > dhry.tar.Z.uue
