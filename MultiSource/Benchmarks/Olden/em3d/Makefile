LEVEL = ../../../..

PROG       = em3d
CPPFLAGS   = -DTORONTO
LDFLAGS    = 

ifdef SMALL_PROBLEM_SIZE
RUN_OPTIONS = 256 250 35
else ifdef LARGE_PROBLEM_SIZE
RUN_OPTIONS = 3072 3000 750
else
RUN_OPTIONS = 1024 1000 125
endif

include $(LEVEL)/MultiSource/Makefile.multisrc

