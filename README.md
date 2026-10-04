# Pixel Sprint
One-thumb endless runner. Unity 6.6, Android (sideload), URP, IL2CPP, ARM64.

The CA1 build is a title screen with a draft main menu, made to prove the signing, install and release pipeline.

## Signing
- Keystore: pixelsprint-release.keystore, stored outside the repo (not committed)
- Alias: pixelsprint
- Validity: 4 Oct 2026 to 21 Sep 2076
- SHA-256: 93:E3:84:C7:0B:ED:68:D5:06:B1:BB:88:FA:E6:AD:91:5D:69:88:3F:BD:DD:5A:30:4F:21:61:79:09:6B:21:C2
- Passwords are kept in a password manager, never in the repo
- A second backup copy of the keystore is kept in a separate location
- keytool reports the certificate as SHA1withRSA (weak). This is fine for sideloading.
- *.keystore and *.jks are in .gitignore

## Build
1. Clone the repo and open it in Unity 6.6 with Android Build Support.
2. File > Build Profiles > Android > Switch Platform.
3. Player Settings: IL2CPP, ARM64 only, package name com.ahmedsekhni.pixelsprint, Version 0.2.0, Bundle Version Code 2.
4. Publishing Settings: Custom Keystore with your own keystore and alias. Build App Bundle off.
5. Use the release profile (Development Build off) and build to releases/PixelSprint-0.2.0-arm64.apk.
6. Install: adb install -r releases/PixelSprint-0.2.0-arm64.apk

## Device targets
- Minimum API 26, target API 36
- Tested: Samsung Galaxy S22 (SM-S901B), Android 16, Vulkan, 1080x2340
- Play target API policy: https://support.google.com/googleplay/android-developer/answer/11926878

## Releases
releases/ holds the release-signed APK. Tags: v0.2.0, v0.2.0-ca1.

## AI assistance
I used an AI assistant (Claude) to help plan the steps, troubleshoot adb, Git and Unity build problems, and draft documentation. I built and tested the project myself and can explain it.