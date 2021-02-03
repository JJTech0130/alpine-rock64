# Decompress originial initramfs
src: initramfs-lts
	mkdir src
	cd src && zcat ../$< | cpio -i

# Compress the initramfs file
initramfs:
	find src | cpio -H newc -o | gzip -9 > $@

# Create img file
initramfs.img: initramfs
	mkimage -n $< -A arm -O linux -T ramdisk -C none -d $< $@

# Remove all generated files
.PHONY: clean
clean:
	rm -rf src initramfs initramfs.img
