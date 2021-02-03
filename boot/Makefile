# Kernel Version
export KTAG := 4.4.202-1237-rockchip-ayufan
export KBUILD := gfd4492386213

.PHONY: all
all: vmlinuz

.PHONY: ayufan-src
ayufan-src:
	$(MAKE) -C $@

vmlinuz: ayufan-src
	
