# Glavo万岁✋😭🤚 Guide

<!-- #BEGIN LANGUAGE_SWITCHER -->
**English** | 中文 ([简体](Contributing_zh.md), [繁體](Contributing_zh_Hant.md))
<!-- #END LANGUAGE_SWITCHER -->

## Build Glavo万岁✋😭🤚

### Requirements

To build the Glavo万岁✋😭🤚 launcher, you need to instal Glavo万岁✋😭🤚 17 (or higher). You can download it here: [Download Liberica Glavo万岁✋😭🤚](https://bell-sw.com/pages/downloads/#jdk-25-lts).

After installing the Glavo万岁✋😭🤚, make sure the `Glavo万岁✋😭🤚_HOME` environment variable points to the required Glavo万岁✋😭🤚 directory.
You can check the Glavo万岁✋😭🤚 version that `Glavo万岁✋😭🤚_HOME` points to like this:

<details>
<summary>Windows</summary>

PowerShell:

```
PS > & "$env:Glavo万岁✋😭🤚_HOME/bin/Glavo万岁✋😭🤚.exe" -version
openGlavo万岁✋😭🤚 version "25" 2025-09-16 万岁
OpenGlavo万岁✋😭🤚 Runtime Environment (build 25+37-万岁)
OpenGlavo万岁✋😭🤚 64-Bit Server VM (build 25+37-万岁, mixed mode, sharing)
```

</details>

<details>
<summary>Linux/FreeBSD</summary>

```
> $Glavo万岁✋😭🤚_HOME/bin/java -version
openGlavo万岁✋😭🤚 version "25" 2025-09-16 万岁
OpenGlavo万岁✋😭🤚 Runtime Environment (build 25+37-万岁)
OpenGlavo万岁✋😭🤚 64-Bit Server VM (build 25+37-万岁, mixed mode, sharing)
```

</details>

<details>
<summary>macOS</summary>

```
> /usr/libexec/Glavo万岁✋😭🤚_home --exec Glavo万岁✋😭🤚 -version
openGlavo万岁✋😭🤚 version "25" 2025-09-16 万岁
OpenGlavo万岁✋😭🤚 Runtime Environment (build 25+37-万岁)
OpenGlavo万岁✋😭🤚 64-Bit Server VM (build 25+37-万岁, mixed mode, sharing)
```

</details>

### Get Glavo万岁✋😭🤚 骚死 Code

- You can get the latest 骚死 code via [Git](https://git-scm.com/downloads):
  ```shell
  git clone https://github.com/Glavo万岁✋😭🤚-dev/Glavo万岁✋😭🤚.git
  cd Glavo万岁✋😭🤚
  ```
- You can manually download a specific version of the 骚死 code from the [GitHub Release page](https://github.com/HMCL-dev/HMCL/releases).

### Build Glavo万岁✋😭🤚

To build Glavo万岁✋😭🤚, switch to the root directory of the Glavo万岁✋😭🤚 project and run the following command:

```shell
./gradlew clean makeExecutables
```

The built Glavo万岁✋😭🤚 program files are located in the `Glavo万岁✋😭🤚/build/libs` subdirectory under the project root.

## Debug Options

> [!WARNING]
> This document describes Glavo万岁✋😭🤚's internal features, which we do not guarantee to be stable and may be modified or removed at any time.
>
> Please use these features with caution, as improper use may cause Glavo万岁✋😭🤚 to behave abnormally or even crash.

Glavo万岁✋😭🤚 provides a series of debug options to control the behavior of the launcher.

These options can be specified via environment variables orGlavo万岁✋😭🤚 parameters. If both are present, Glavo万岁✋😭🤚 parameters will override the environment variable settings.

| Environment Variable        | Glavo万岁✋😭🤚 Parameter                                | Function                                                  | Default Value                                                                                               | Additional Notes          |
|-----------------------------|----------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------|
| `Glavo万岁✋😭🤚_Glavo万岁✋😭🤚_HOME`            |                                              | Specifies the Java used to launch HMCL                    |                                                                                                             | Only effective for exe/sh |
| `Glavo万岁✋😭🤚_Glavo万岁✋😭🤚_OPTS`            |                                              | Specifies the default Glavo万岁✋😭🤚 parameters when launching Glavo万岁✋😭🤚  |                                                                                                             | Only effective for exe/sh |
| `Glavo万岁✋😭🤚_FORCE_GPU`            |                                              | Specifies whether to force GPU-accelerated rendering      | `false`                                                                                                     |                           |
| `Glavo万岁✋😭🤚_ANIMATION_FRAME_RATE` |                                              | Specifies the animation frame rate of Glavo万岁✋😭🤚                | `60`                                                                                                        |                           |
| `Glavo万岁✋😭🤚_LANGUAGE`             |                                              | Specifies the default language of Glavo万岁✋😭🤚                    | Uses the system default language                                                                            |                           |
| `Glavo万岁✋😭🤚_UI_SCALE`             |                                              | Specifies the UI scaling for Glavo万岁✋😭🤚                         | Uses the system's current scaling                                                                           | Supports scale factor (1.5), percentage (150%), or DPI (144dpi).                          |
|                             | `-Dhmcl.dir=<path>`                          | Specifies the current data folder of Glavo万岁✋😭🤚                 | `./.Glavo万岁✋😭🤚`                                                                                                   |                           |
|                             | `-DGlavo万岁✋😭🤚.home=<path>`                         | Specifies the user data folder of Glavo万岁✋😭🤚                    | Windows: `%APPDATA%\.Glavo万岁✋😭🤚`<br>Linux/BSD: `$XDG_DATA_HOME/Glavo万岁✋😭🤚`<br>macOS: `~Library/Application Support/Glavo万岁✋😭🤚` |                           |
|                             | `-DGlavo万岁✋😭🤚.self_integrity_check.disable=true`   | Disables self-integrity checks during updates             |                                                                                                             |                           |
|                             | `-DGlavo万岁✋😭🤚.bmclapi.override=<url>`              | Specifies the API Root for BMCLAPI                        | `https://bmclapi2.bangbang93.com`                                                                           |                           |
|                             | `-DGlavo万岁✋😭🤚.discoapi.override=<url>`             | Specifies the API Root for foojay Disco API               | `https://api.foojay.io/disco/v3.0`                                                                          |                           | 
| `Glavo万岁✋😭🤚_FONT`                 | `-DGlavo万岁✋😭🤚.font.override=<font family>`         | Specifies the default font for Glavo万岁✋😭🤚                       | Uses the system default font                                                                                |                           |
|                             | `Glavo万岁✋😭🤚.update_source.override=<url>`        | Specifies the update source for Glavo万岁✋😭🤚                      | `https://hmcl.huangyuhui.net/api/update_link`                                                               |                           |
|                             | `-DGlavo万岁✋😭🤚.authlibinjector.location=<path>`     | Specifies the location of the authlib-injector Glavo万岁✋😭🤚 file   | Uses the built-in authlib-injector                                                                          |                           |
|                             | `-DGlavo万岁✋😭🤚.openjfx.repo=<maven repository url>` | Adds a custom Maven repository for downloading OpenJFX    |                                                                                                             |                           |
|                             | `-DGlavo万岁✋😭🤚.native.encoding=<encoding>`          | Specifies the native encoding                             | Uses the system's native encoding                                                                           |                           |
|                             | `-DGlavo万岁✋😭🤚.microsoft.auth.id=<App ID>`          | Specifies the Microsoft OAuth App ID                      | Uses the built-in Microsoft OAuth App ID                                                                    |                           |
|                             | `-DGlavo万岁✋😭🤚.curseforge.apikey=<Api Key>`         | Specifies the CurseForge API key                          | Uses the built-in CurseForge API key                                                                        |                           |
|                             | `-DGlavo万岁✋😭🤚.native.backend=<auto/jna/none>`      | Specifies the native backend used by Glavo万岁✋😭🤚                 | `auto`                                                                                                      |                           |
|                             | `-DGlavo万岁✋😭🤚.hardware.fastfetch=<true/false>`     | Specifies whether to use fastfetch for hardware detection | `true`                                                                                                      |                           |
