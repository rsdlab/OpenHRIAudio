INSTALLERFILE=$(PACKAGE)-$(VERSION).exe

CLEANFILES=$(INSTALLERFILE)

if INSTALLER
all: $(INSTALLERFILE)
endif

$(INSTALLERFILE): openhriaudio.nsi ../../src/openhriaudio.exe
	$(MAKENSIS) -DOUTFILE="$(abs_builddir)/$@" -DPACKAGE="$(PACKAGE)" -DPACKAGE_NAME="$(PACKAGE_NAME)" -DPACKAGE_VERSION="$(PACKAGE_VERSION)" -DPACKAGE_BUGREPORT="$(PACKAGE_BUGREPORT)" -DVERSIONNUM="$(INSTALLER_VERSION)" -DEXTDIR="$(INSTALLER_EXTDIR)" -DTOP_SRCDIR="$(abs_top_srcdir)" -DTOP_BUILDDIR="$(abs_top_builddir)" $<

.PHONY: all data