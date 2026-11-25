# DRAGON BALL: Sparking! ZERO — Android Port (Overlay Variants)

> Documentation based on inspection of the two APK packages in this folder. This repository documentation does not include the game itself or proprietary game files.

## Package overview

Two signed Android APK variants were inspected:

- **Standard prompts:** `DragonBallSparkingZero_prompts_STANDARD_signed.apk`
- **Classic prompts:** `DragonBallSparkingZero_prompts_CLASSIC_signed.apk`

Both packages report:
- Application label: DRAGON BALL: Sparking! ZERO
- Package ID: `org.nx2a.t010035f022078000`
- Version name: `2.0.76` (version code `327696`)
- Android minimum SDK: 29 (Android 10)
- Target SDK: 36
- Native ABI: `arm64-v8a`
- Main activity: Android NativeActivity
- Landscape orientation

## Variant differences

The APKs share the same package structure and files except for signing metadata and the selected overlay theme configuration.

- **Standard:** uses `glyph/standard_phone.png` and `glyph/standard_tablet.png`, with Nintendo Switch-style prompt badges on controller buttons.
- **Classic:** uses `glyph/classic_phone.png` and `glyph/classic_tablet.png`, presenting the Classic control artwork with prompt badges.
- Both include alternate theme configuration tables and art for phone/tablet layouts.
- The overlay's documented opacity is 0.9. Sprite atlas coordinates and layout metadata are stored in TSV theme files.

## APK contents observed

- Native libraries: `libdmhost.so`, `libadrenotools.so`, `libhook_impl.so`, `libmain_hook.so`, `libfile_redirect_hook.so`, `libgsl_alloc_hook.so`
- Touch-control overlay atlases and theme tables
- Font assets and associated license files (including OFL notices)
- Unlock-save data files
- Android manifest and application resources

The APK contains compiled native libraries, not a complete editable source-code project. This inspection does not establish the origin or license of every binary or resource. No proprietary game files, APK binaries, extracted native code, or unverified assets are included in this documentation.

## Credits and upstream

The previous/base port is credited by the project maintainer as **YOBI FF**. This attribution is based on the maintainer's information and should be accompanied by the upstream project link and license when confirmed.

This project should only be published with materials whose redistribution is permitted by their respective owners/licenses. The DRAGON BALL and Sparking! ZERO names and assets belong to their respective rights holders.

## Open-source status

A source release should be based on the original upstream source repository or source files that the maintainer is authorized to publish. The APK alone is not a clean source-code release; its native libraries are compiled binaries. Reverse-engineered/disassembled output is not substituted here for original source code.

## Technical notes

Android manifest inspection shows permissions for network access, Wi-Fi/network state, vibration, and file access. Storage permissions include legacy read/write permissions capped at API 29 and `MANAGE_EXTERNAL_STORAGE`.

This is a package-structure analysis only. It is not a claim that the port works on every Android device or that any specific game-performance result was tested.
