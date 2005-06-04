##
## Makefile.am,v 1.5 2002/03/28 00:41:50 joel Exp
##


C_FILES = vectors_init.c

H_FILES = vectors.h

S_FILES = vectors.S

$(PROJECT_INCLUDE)/bsp:
	$(mkinstalldirs) $@

$(PROJECT_INCLUDE)/bsp/%.h: %.h
	$(INSTALL_DATA) $< $@

PREINSTALL_FILES = $(PROJECT_INCLUDE)/bsp \
    $(H_FILES:%.h=$(PROJECT_INCLUDE)/bsp/%.h)

all-local: $(PREINSTALL_FILES)

EXTRA_DIST = vectors.S vectors.h vectors_init.c exceptionhandler.c bspException.h machinecheckclear.c

include $(top_srcdir)/../../../../../automake/local.am
