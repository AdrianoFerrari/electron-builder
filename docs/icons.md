Recommended tools: [AppIcon Generator](http://www.tweaknow.com/appicongenerator.php), [MakeAppIcon](https://makeappicon.com/), [iConvert Icons](https://iconverticons.com/online/).

## Minimal cross-platform build
The files

* `icon.icns` of at least 512x512
* `icon.ico` of at least 256x256

need to be in the [build](/configuration/configuration.md#MetadataDirectories-buildResources) directory. For this minimal cross-platform build setup, there should **not** be a file named `icon.png` in the same directory (causes [issues](https://github.com/electron-userland/electron-builder/issues/2577) with Linux icon).

## macOS

Files

* *Optional* `icon.icns` (macOS app icon) or `icon.png`. Icon size should be at least 512x512.
* *Optional* `background.png` (macOS DMG background).
* *Optional* `background@2x.png` (macOS DMG Retina background).

need to be placed in the [build](/configuration/configuration.md#MetadataDirectories-buildResources) directory. All files are optional — but it is important to provide `icon.icns` (or `icon.png`), otherwise default Electron icon will be used.

## Windows (NSIS)

* *Optional* `icon.ico` (Windows app icon) or `icon.png`. Icon size should be at least 256x256.

need to be placed in the [build](/configuration/configuration.md#MetadataDirectories-buildResources) directory. It is important to provide `icon.ico` (or `icon.png`), otherwise default Electron icon will be used.

## Linux

Linux icon set will be generated automatically based on the macOS `icns` file or common `icon.png`.

Or you can put them into the `build/icons` directory if you want to specify them yourself.
The filename must contain the size (e.g. `32x32.png`) of the icon). Recommended sizes: 16, 24, 32, 48, 64, 96, 128, 256. (or just 512).

## AppX

See [AppX Assets](/configuration/appx#appx-assets).
