# Makefile for Yuma util directory
#  
#   util directory

ifndef PREFIX
    PREFIX=/usr
endif

UTIL_INSTALL = $(DESTDIR)$(PREFIX)/share/yuma/util

BIN_INSTALL = $(DESTDIR)$(PREFIX)/bin

all:

depend:

clean:

uninstall:
	rm -f $(UTIL_INSTALL)

superclean: clean

ifdef DEBIAN
ifdef DEVELOPER
install: installfiles
else
install: 
endif  # DEVELOPER
else
install: installfiles
endif  # DEBIAN

installfiles:
	mkdir -p $(UTIL_INSTALL)
	cp makefile.sil $(UTIL_INSTALL)/
	cp makefile-top.sil $(UTIL_INSTALL)/
	mkdir -p $(BIN_INSTALL)
	install $(OWNER) $(GRP) make_sil_dir $(BIN_INSTALL)

distclean: superclean

.PHONY: all clean depend superclean install uninstall distclean \
	installfiles

# prevent the make program from choking on all the symbols
# that get generated from autogenerated make rules
.NOEXPORT:



