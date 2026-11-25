# APK Extraction Report

Date: 2026-11-25

## What was extracted

Both APK variants were successfully decoded locally with Apktool 2.12.1:

- STANDARD
- CLASSIC

Decoded output is kept locally in `apk_extracted/standard` and `apk_extracted/classic` (case as produced by Apktool), and is not committed.

## Findings

- Package ID: `org.nx2a.t010035f022078000`
- Version: `2.0.76` (version code `327696`)
- ABI: `arm64-v8a`
- Android minimum: API 29 / Android 10
- Target API: 36
- Native Android activity / landscape
- The APKs contain native shared libraries and bundled resources/assets.
- The variants mainly differ in controller prompt/theme resources.

## Source-code limitation

Apktool can decode the manifest, resource tables, and assets, but this does **not** reconstruct the original project or source code. Native libraries remain compiled binaries. No original source tree was found in the provided project folder.

## Publishing policy for this repository

This repository contains documentation. The decoded APK contents are not published because they include compiled native libraries and bundled assets with unclear redistribution/licensing status. APK build files are attached to the GitHub Release separately for distribution of these user-provided builds.

