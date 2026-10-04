  # Pixel Sprint
   One-thumb endless runner (Option: endless runner). Unity 6.6, Android.

   ## Test device
   - Phone: Samsung Galaxy S22 (SM-S901B)
   - Android: 16 (API 36)
   - Graphics API: Vulkan
   - [Boot] line: samsung SM-S901B | Android OS 16 / API-36 | Vulkan | 1080x2340 @ 480 dpi

   ## Build steps
   1. Open the project in Unity 6.6 and switch the platform to Android (File > Build Profiles).
   2. Player Settings: IL2CPP, ARM64 only, package name com.ahmedsekhni.pixelsprint.
   3. Build to Builds/PixelSprint-dev.apk, then run `adb install -r Builds/PixelSprint-dev.apk`.

      
