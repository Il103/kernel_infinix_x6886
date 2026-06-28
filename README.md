# Kernel Tree for Infinix Hot 60 Pro Plus (X6886)

| Device | Infinix Hot 60 Pro Plus |
| :--- | :--- |
| Chipset | MediaTek Helio G200 (MT6789) |
| Kernel | Linux 5.10.237 |
| Compiler | Clang 12.0.5 |
| Branch | lineage-23.2 |

## Contents

- `Image.gz` - Prebuilt kernel extracted from stock boot.img
- `defconfig` - Kernel configuration (6,727 lines, from ikconfig)
- `dtbs/dtbo.img` - Device Tree Blob Overlay

## Usage

This kernel tree is designed to work with:

- [android_device_infinix_x6886](https://github.com/Il103/android_device_infinix_x6886)
- [vendor_infinix_x6886](https://github.com/Il103/vendor_infinix_x6886)

Place in your LineageOS source tree:

```
kernel/infinix/x6886/
```

Then `BoardConfig.mk` should reference:

```makefile
TARGET_PREBUILT_KERNEL := kernel/infinix/x6886/Image.gz
TARGET_PREBUILT_DTB := kernel/infinix/x6886/dtbs/dtbo.img
```

## Build

With this kernel tree in place, build LineageOS:

```bash
source build/envsetup.sh
lunch lineage_x6886-userdebug
mka bacon
```

## Git LFS

Large binary files are tracked with Git LFS:

```bash
git lfs pull
```

## Credits

- Stock ROM dump by [Il103](https://github.com/Il103)
- Kernel extracted from boot.img
- Config extracted via ikconfig
