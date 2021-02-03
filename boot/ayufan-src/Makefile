.PHONY: all
all: linux-image linux-headers linux-firmware-image

KFILE = $@-$(KTAG)-$(KBUILD)_$(KTAG)_arm64.deb
KURL = https://github.com/ayufan-rock64/linux-kernel/releases/download/$(KTAG)/$(KFILE)

define get-kf
 @echo Downloading $(KFILE)...
 wget $(KURL)
 @echo Extracting $(KFILE)...
 dpkg -x $(KFILE) $@
endef

linux-image:
	$(get-kf)
linux-headers:
	$(get-kf)
linux-firmware-image:
	$(get-kf)

.PHONY: clean
clean:
	rm -rf linux-*
