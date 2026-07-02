# Kernel Tree for Infinix Hot 60 Pro Plus (X6886)

| Device | Infinix Hot 60 Pro Plus |
| :--- | :--- |
| Chipset | MediaTek Helio G200 (MT6789) |
| Kernel | Linux 5.10.237 |
| Compiler | Clang 12.0.5 |
| Branch | lineage-23.2 |

## Contents

| File | Size | Description |
|------|------|-------------|
| `Image.gz` | 19 MB | Gzip-compressed kernel Image (from stock boot) |
| `defconfig` | 6,727 lines | Kernel configuration (extracted via ikconfig) |
| `ramdisk/*.ko` | 229 files, 31 MB | Vendor ramdisk kernel modules (GKI vendor_boot) |
| `vendor_dlkm/*.ko` | 184 files, 27 MB | Vendor DLKM kernel modules |
| `dtbs/dtb.img` | 8 MB | MT6789 Device Tree Blob |
| `dtbs/dtbo.img` | 8 MB | Device Tree Blob Overlay |
| `kernel-headers/` | | Generated UAPI kernel headers |

## Usage

Place in LineageOS source tree at `kernel/infinix/x6886/` and build:

```bash
source build/envsetup.sh
lunch lineage_x6886-userdebug
mka bacon -j$(nproc)
```

No LFS needed — all files are actual binaries tracked directly in git.

## Notes

- Kernel extracted from stock boot partition (ELF 64-bit ARM Image)
- All 413 kernel modules verified present and matching modules.load
- DTBs from stock vendor_boot and device tree overlays

## Credits

- Stock ROM dump by [Il103](https://github.com/Il103)
- Kernel extracted from boot.img
- DTB from stock vendor_boot
