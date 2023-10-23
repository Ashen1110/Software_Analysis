DEFINES = -DUNIX
FLAGS = $(DEFINES) -O3
SPI = -prof-gen=srcpos
NO_COMM = -diag-disable=10441

SRC =  $(wildcard *.c)
EXE = $(subst .,,$(SRC))
all: ${EXE}

ICC = icc $(FLAGS)

%c:	%.c
	@${ICC} ${SPI} ${NO_COMM} $*.c -o $* 

