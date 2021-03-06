#!/usr/bin/env make
#
# 2012 makefile
#
# This work by Landon Curt Noll, Simon Cooper, and Leonid A. Broukhis
# is licensed under:
#
#	Creative Commons Attribution-ShareAlike 3.0 Unported License.
#
# See: http://creativecommons.org/licenses/by-sa/3.0/


################
# tool locations
################
#
SHELL= /bin/bash
CP= cp
CPP= cpp
GUNZIP= gunzip
LD= ld
MAKE= make
RM= rm
SED= sed
TAR= tar
TRUE= true

# Set X11_LIBDIR to the directory where the X11 library resides
#
X11_LIBDIR= /usr/X11R6/lib

# Set X11_INCLUDEDIR to the directory where the X11 include files reside
#
X11_INCDIR= /usr/X11R6/include

# Compiler warnings
#
#CWARN=
#CWARN= -Wall -W
CWARN= -Wall -W -pedantic

# compiler standard
#
#CSTD=
#CSTD= -ansi
CSTD= -std=c99

# compiler bit architecture
#
# Some entries require 32-bitness:
# ARCH= -m32
#
# Some entries require 64-bitess:
# ARCH= -m64
#
# By default we assume nothing:
#
ARCH=

# optimization
#
# Most compiles will safely use -O2.  Some can use only -O1 or -O.
# A few compilers have broken optimizers or this entry make break
# under those buggy optimizers and thus you may not want anything.
#
#OPT=
#OPT= -O
#OPT= -O1
OPT= -O2
#OPT= -O3

# Libraries needed to build
#
LIBS=

# default flags for ANSI C compilation
#
CFLAGS= ${CWARN} ${CSTD} ${ARCH} ${OPT} ${LIBS}

# ANSI compiler
#
# Set CC to the name of your ANSI compiler.
#
# Some entries seem to need gcc.  If you have gcc, set
# both CC and MAY_NEED_GCC to gcc.
#
# If you do not have gcc, set CC to the name of your ANSI compiler, and
# set MAY_NEED_GCC to either ${CC} (and hope for the best) or to just :
# to disable such programs.
#
CC= cc
#CC=clang
MAY_NEED_GCC= gcc


##############################
# Special flags for this entry
##############################
#
ENTRY= endoh2
DATA=

ALT_C= pi.c 314.c 3141.c 31415.c 314159.c 3141592.c \
	31415926.c 314159265.c 3141592653.c 31415926535.c \
	e.c 271.c 2718.c 27182.c 271828.c 2718281.c \
	27182818.c 271828182.c 2718281828.c 27182818284.c

ALT_ENTRY= pi 314 3141 31415 314159 \
	3141592 31415926 314159265 3141592653 31415926535 \
	e 271 2718 27182 271828 \
	2718281 27182818 271828182 2718281828 27182818284

ALT_OBJ= pi.o 314.o 3141.o 31415.o 314159.o 3141592.o \
	31415926.o 314159265.o 3141592653.o 31415926535.o \
	e.o 271.o 2718.o 27182.o 271828.o 2718281.o \
	27182818.o 271828182.o 2718281828.o 27182818284.o

ALT_ENTRY= pi 314 3141 31415 314159 3141592 \
	31415926 314159265 3141592653 31415926535 \
	e 271 2718 27182 271828 2718281 \
	27182818 271828182 2718281828 27182818284


#################
# build the entry
#################
#
all: ${ENTRY} ${DATA}
	@${TRUE}

${ENTRY}: ${ENTRY}.c
	${CC} ${CFLAGS} $< -o $@

pi.c: ${ENTRY}
	./$< > $@

pi: pi.c
	${CC} ${CFLAGS} $< -o $@

314.c: pi
	./$< > $@

314: 314.c
	${CC} ${CFLAGS} $< -o $@

3141.c: 314
	./$< > $@

3141: 3141.c
	${CC} ${CFLAGS} $< -o $@

31415.c: 3141
	./$< > $@

31415: 31415.c
	${CC} ${CFLAGS} $< -o $@

314159.c: 31415
	./$< > $@

314159: 314159.c
	${CC} ${CFLAGS} $< -o $@

3141592.c: 314159
	./$< > $@

3141592: 3141592.c
	${CC} ${CFLAGS} $< -o $@

31415926.c: 3141592
	./$< > $@

31415926: 31415926.c
	${CC} ${CFLAGS} $< -o $@

314159265.c: 31415926
	./$< > $@

314159265: 314159265.c
	${CC} ${CFLAGS} $< -o $@

3141592653.c: 314159265
	./$< > $@

3141592653: 3141592653.c
	${CC} ${CFLAGS} $< -o $@

31415926535.c: 3141592653
	./$< > $@

31415926535: 31415926535.c
	${CC} ${CFLAGS} $< -o $@

# you get the transcendental idea ... :-)

e.c: ${ENTRY}
	./$< e > $@

e: e.c
	${CC} ${CFLAGS} $< -o $@

271.c: e
	./$< > $@

271: 271.c
	${CC} ${CFLAGS} $< -o $@

2718.c: 271
	./$< > $@

2718: 2718.c
	${CC} ${CFLAGS} $< -o $@

27182.c: 2718
	./$< > $@

27182: 27182.c
	${CC} ${CFLAGS} $< -o $@

271828.c: 27182
	./$< > $@

271828: 271828.c
	${CC} ${CFLAGS} $< -o $@

2718281.c: 271828
	./$< > $@

2718281: 2718281.c
	${CC} ${CFLAGS} $< -o $@

27182818.c: 2718281
	./$< > $@

27182818: 27182818.c
	${CC} ${CFLAGS} $< -o $@

271828182.c: 27182818
	./$< > $@

271828182: 271828182.c
	${CC} ${CFLAGS} $< -o $@

2718281828.c: 271828182
	./$< > $@

2718281828: 2718281828.c
	${CC} ${CFLAGS} $< -o $@

27182818284.c: 2718281828
	./$< > $@

27182818284: 27182818284.c
	${CC} ${CFLAGS} $< -o $@

271828182845.c: 27182818284
	./$< > $@

271828182845: 271828182845.c
	${CC} ${CFLAGS} $< -o $@

# etc. ... :-)

# alternative executable
#
alt: ${ALT_ENTRY}
	@${TRUE}

# data files
#
data: ${DATA}
	@${TRUE}


###############
# utility rules
###############
#
everything: all alt

clean:
	${RM} -f ${ENTRY}.o ${ALT_OBJ}

clobber: clean
	${RM} -f ${ENTRY} ${ALT_ENTRY} ${ALT_C}

nuke: clobber
	@${TRUE}

dist_clean: nuke
	@${TRUE}

install:
	@echo "Surely you're joking Mr. Feynman!"
	@${TRUE}

# backwards compatibility
#
build: all
	@${TRUE}


##################
# 133t hacker rulz
##################
#
love:
	@echo 'not war?'
	@${TRUE}

haste:
	$(MAKE) waste
	@${TRUE}

waste:
	@echo 'waste'
	@${TRUE}

easter_egg:
	@echo you expected to mis-understand this $${RANDOM} magic
	@echo chongo '<was here>' "/\\oo/\\"
	@echo Readers shall be disallowed from not being unable to partly misunderstand this partocular final echo.

# Understand the history of "I Am the Walrus" and
# and in particular John Lennon's remarks on that
# song and you might be confused about these next
# rules in a different way. :-)
#
supernova: nuke
	@-if [ -r .code_anal ]; then \
	    ${RM} -f .code_anal_v3; \
	else \
	    echo "You are not expected to understand this"; \
	fi
	@${TRUE}

deep_magic:
	@-if [ -r .code_anal ]; then \
	    ccode_analysis --deep_magic 1c2c85c7a02c55d1add91967eca491d53c101dc1 --FNV1a_hash 256-bit "${ENTRY}"; \
	else \
	    echo "Understand different"; \
	fi
	@${TRUE}

magic: deep_magic
	@-if [ -r .code_anal ]; then \
	    ccode_analysis --mode 21701 --level 23209 --FNV1a_hash 256-bit "${ENTRY}"; \
	else \
	    echo "These aren't the droids you're looking for Mr. Spock!"; \
	fi
	@${TRUE}
