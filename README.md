<h1 align="center">Freemethyst</h1>

<img src="https://github.com/Kaedo17/Freemethyst-Android/blob/v3_openjdk/app_pojavlauncher/src/main/assets/amethyst.png" align="left" width="130" height="130" alt="Freemethyst logo">

[![Android CI](https://github.com/Kaedo17/Freemethyst-Android/workflows/Android%20CI/badge.svg)](https://github.com/Kaedo17/Freemethyst-Android/actions)
[![GitHub commit activity](https://img.shields.io/github/commit-activity/m/Kaedo17/Freemethyst-Android)](https://github.com/Kaedo17/Freemethyst-Android/actions)

Freemethyst is a fork of [Amethyst](https://github.com/AngelAuraMC/Amethyst-Android) (originally based on [Boardwalk](https://github.com/zhuowei/Boardwalk) and [PojavLauncher](https://github.com/PojavLauncherTeam/PojavLauncher)), a Minecraft: Java Edition launcher for Android.

## Table of Contents

* [Building](#building)
* [License](#license)
* [Credits & Dependencies](#credits--dependencies)

## Building

### Quick Build

1. Clone the repository: `git clone --recursive https://github.com/Kaedo17/Freemethyst-Android.git`
2. Build the launcher: `./gradlew :app_pojavlauncher:assembleDebug`

The built APK will be located in `app_pojavlauncher/build/outputs/apk/debug/`.

### Detailed Build

1. **Java Runtime Environment (JRE):** Download the `jre8-pojav` artifact from the [CI auto builds](https://github.com/AngelAuraMC/angelauramc-openjdk-build/actions). This package contains pre-built JREs for all supported architectures.

2. **LWJGL:** Build instructions are available in the [LWJGL repository](https://github.com/AngelAuraMC/lwjgl3).

3. **Language List:** Run the language list generator before building:
   * Linux/macOS: `bash scripts/languagelist_updater.sh`
   * Windows: `scripts\languagelist_updater.bat`

4. **Build GLFW stub:** `./gradlew :jre_lwjgl3glfw:build`

5. **Build the launcher:** `./gradlew :app_pojavlauncher:assembleDebug`

## License

Freemethyst is licensed under [GNU LGPLv3](https://github.com/Kaedo17/Freemethyst-Android/blob/v3_openjdk/LICENSE).

## Credits & Dependencies

* [Boardwalk](https://github.com/zhuowei/Boardwalk) (JVM Launcher): Unknown License/[Apache License 2.0](https://github.com/zhuowei/Boardwalk/blob/master/LICENSE) or GNU GPLv2.
* [PojavLauncher](https://github.com/PojavLauncherTeam/PojavLauncher): [LGPL](https://github.com/PojavLauncherTeam/PojavLauncher/blob/v3_openjdk/LICENSE)
* [Amethyst](https://github.com/AngelAuraMC/Amethyst-Android): [LGPL](https://github.com/AngelAuraMC/Amethyst-Android/blob/v3_openjdk/LICENSE)
* Android Support Libraries: [Apache License 2.0](https://android.googlesource.com/platform/prebuilts/maven_repo/android/+/master/NOTICE.txt).
* [GL4ES](https://github.com/AngelAuraMC/gl4es): [MIT License](https://github.com/ptitSeb/gl4es/blob/master/LICENSE).
* [MobileGlues](https://github.com/MobileGL-Dev/MobileGlues): [LGPL-2.1 License](https://github.com/MobileGL-Dev/MobileGlues/blob/dev-es/LICENSE).
* [Krypton Wrapper](https://github.com/BZLZHH/NG-GL4ES): [MIT License](https://github.com/BZLZHH/NG-GL4ES/blob/main/LICENSE)
* [ANGLE](https://chromium.googlesource.com/angle/angle): [All Rights Reserved](app_pojavlauncher/src/main/assets/licenses/ANGLE_LICENSE).
* [OpenJDK](https://github.com/AngelAuraMC/openjdk-multiarch-jdk8u): [GNU GPLv2 License](https://openjdk.java.net/legal/gplv2+ce.html).
* [LWJGL3](https://github.com/AngelAuraMC/lwjgl3): [BSD-3 License](https://github.com/LWJGL/lwjgl3/blob/master/LICENSE.md).
* [LWJGLX](https://github.com/AngelAuraMC/lwjglx) (LWJGL2 API compatibility layer for LWJGL3): unknown license.
* [Mesa 3D Graphics Library](https://gitlab.freedesktop.org/mesa/mesa): [MIT License](https://docs.mesa3d.org/license.html).
* [pro-grade](https://github.com/pro-grade/pro-grade) (Java sandboxing security manager): [Apache License 2.0](https://github.com/pro-grade/pro-grade/blob/master/LICENSE.txt).
* [bhook](https://github.com/bytedance/bhook) (Used for exit code trapping): [MIT license](https://github.com/bytedance/bhook/blob/main/LICENSE).
* [libepoxy](https://github.com/anholt/libepoxy): [MIT License](https://github.com/anholt/libepoxy/blob/master/COPYING).
* [virglrenderer](https://github.com/AngelAuraMC/virglrenderer): [MIT License](https://gitlab.freedesktop.org/virgl/virglrenderer/-/blob/master/COPYING).
* [OpenAL-Soft](https://github.com/kcat/openal-soft): [GNU GPLv2](app_pojavlauncher/src/main/assets/licenses/OPENAL-SOFT_GPL2)
  * [oboe](https://github.com/google/oboe): [Apache License 2.0](app_pojavlauncher/src/main/assets/licenses/OBOE_APACHE2).
  * [pfffft](https://bitbucket.org/jpommier/pffft/src/master/): [ARR](app_pojavlauncher/src/main/assets/licenses/PFFFT_LICENSE)
* [SDL3](https://github.com/libsdl-org/SDL): [zlib License](https://github.com/libsdl-org/SDL/blob/main/LICENSE.txt)
* [sdl2-compat](https://github.com/libsdl-org/sdl2-compat): [zlib License](https://github.com/libsdl-org/sdl2-compat/blob/main/LICENSE.txt)
* Thanks to [MCHeads](https://mc-heads.net) for providing Minecraft avatars.
