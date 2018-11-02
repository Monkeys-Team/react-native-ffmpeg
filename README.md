# React Native FFmpeg [![Join the chat at https://gitter.im/react-native-ffmpeg/Lobby](https://badges.gitter.im/react-native-ffmpeg/Lobby.svg)](https://gitter.im/react-native-ffmpeg/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) ![GitHub release](https://img.shields.io/badge/release-v0.2.1-blue.svg) [![npm](https://img.shields.io/npm/v/react-native-ffmpeg.svg)](react-native-ffmpeg)

FFmpeg for React Native

<img src="https://github.com/tanersener/react-native-ffmpeg/raw/master/docs/assets/react-native-ffmpeg-logo-v2.png" width="280">

### 1. Features
- Based on Mobile FFmpeg
- Supports
    - Both Android and IOS
    - FFmpeg `v4.0.x` and `v4.1-dev-x` (master) releases
    - `arm-v7a`, `arm-v7a-neon`, `arm64-v8a`, `x86` and `x86_64` architectures on Android
    - `armv7`, `armv7s`, `arm64`, `i386` and `x86_64` architectures on IOS
    - 27 external libraries
    
        `chromaprint`, `fontconfig`, `freetype`, `fribidi`, `gmp`, `gnutls`, `kvazaar`, `lame`, `libaom`, `libass`, `libiconv`, `libilbc`, `libtheora`, `libvorbis`, `libvpx`, `libwebp`, `libxml2`, `opencore-amr`, `opus`, `sdl`, `shine`, `snappy`, `soxr`, `speex`, `tesseract`, `twolame`, `wavpack`
    
    - 4 external libraries with GPL license
    
        `vid.stab`, `x264`, `x265`, `xvidcore`
        
    - `zlib` and `MediaCodec` Android system libraries
    - `bzip2`, `zlib` IOS system libraries and `AudioToolbox`, `CoreImage`, `VideoToolbox`, `AVFoundation` IOS system frameworks

- Licensed under LGPL 3.0, can be customized to support GPL v3.0
- Includes eight different packages with different external libraries enabled in FFmpeg

<table>
<thead>
<tr>
<th align="center"></th>
<th align="center">min</th>
<th align="center">min-gpl</th>
<th align="center">https</th>
<th align="center">https-gpl</th>
<th align="center">audio</th>
<th align="center">video</th>
<th align="center">full</th>
<th align="center">full-gpl</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center"><sup>external libraries</sup></td>
<td align="center">-</td>
<td align="center"><sup>vid.stab</sup><br><sup>x264</sup><br><sup>x265</sup><br><sup>xvidcore</sup></td>
<td align="center"><sup>gmp</sup><br><sup>gnutls</sup></td>
<td align="center"><sup>gmp</sup><br><sup>gnutls</sup><br><sup>vid.stab</sup><br><sup>x264</sup><br><sup>x265</sup><br><sup>xvidcore</sup></td>
<td align="center"><sup>chromaprint</sup><br><sup>lame</sup><br><sup>libilbc</sup><br><sup>libvorbis</sup><br><sup>opencore-amr</sup><br><sup>opus</sup><br><sup>shine</sup><br><sup>soxr</sup><br><sup>speex</sup><br><sup>twolame</sup><br><sup>wavpack</sup></td>
<td align="center"><sup>fontconfig</sup><br><sup>freetype</sup><br><sup>fribidi</sup><br><sup>kvazaar</sup><br><sup>libaom</sup><br><sup>libass</sup><br><sup>libiconv</sup><br><sup>libtheora</sup><br><sup>libvpx</sup><br><sup>libwebp</sup><br><sup>snappy</sup></td>
<td align="center"><sup>chromaprint</sup><br><sup>fontconfig</sup><br><sup>freetype</sup><br><sup>fribidi</sup><br><sup>gmp</sup><br><sup>gnutls</sup><br><sup>kvazaar</sup><br><sup>lame</sup><br><sup>libaom</sup><br><sup>libass</sup><br><sup>libiconv</sup><br><sup>libilbc</sup><br><sup>libtheora</sup><br><sup>libvorbis</sup><br><sup>libvpx</sup><br><sup>libwebp</sup><br><sup>libxml2</sup><br><sup>opencore-amr</sup><br><sup>opus</sup><br><sup>sdl</sup><br><sup>shine</sup><br><sup>snappy</sup><br><sup>soxr</sup><br><sup>speex</sup><br><sup>tesseract</sup><br><sup>twolame</sup><br><sup>wavpack</sup></td>
<td align="center"><sup>chromaprint</sup><br><sup>fontconfig</sup><br><sup>freetype</sup><br><sup>fribidi</sup><br><sup>gmp</sup><br><sup>gnutls</sup><br><sup>kvazaar</sup><br><sup>lame</sup><br><sup>libaom</sup><br><sup>libass</sup><br><sup>libiconv</sup><br><sup>libilbc</sup><br><sup>libtheora</sup><br><sup>libvorbis</sup><br><sup>libvpx</sup><br><sup>libwebp</sup><br><sup>libxml2</sup><br><sup>opencore-amr</sup><br><sup>opus</sup><br><sup>sdl</sup><br><sup>shine</sup><br><sup>snappy</sup><br><sup>soxr</sup><br><sup>speex</sup><br><sup>tesseract</sup><br><sup>twolame</sup><br><sup>vid.stab</sup><br><sup>wavpack</sup><br><sup>x264</sup><br><sup>x265</sup><br><sup>xvidcore</sup></td>
</tr>
<tr>
<td align="center"><sup>android system libraries</sup></td>
<td align="center" colspan=8><sup>zlib</sup><br><sup>MediaCodec</sup></td>
</tr>
<tr>
<td align="center"><sup>ios system libraries</sup></td>
<td align="center" colspan=8><sup>zlib</sup><br><sup>AudioToolbox</sup><br><sup>AVFoundation</sup><br><sup>CoreImage</sup><br><sup>VideoToolbox</sup><br><sup>bzip2</sup></td>
</tr>
</tbody>
</table>


### 2. Installation

`$ yarn add react-native-ffmpeg`

#### 2.1 Android

    $ react-native link react-native-ffmpeg
    
#### 2.2 iOS

##### 2.2.1 Basic
  - Add `react-native-ffmpeg` pod to your `Podfile` and run `pod install`

    ```
    pod 'react-native-ffmpeg', :podspec => '../node_modules/react-native-ffmpeg/ios/react-native-ffmpeg.podspec'
    ```

##### 2.2.2 Advanced
  - See [react-native-ffmpeg-test](https://github.com/tanersener/react-native-ffmpeg-test) for linking alternatives

#### 2.3 Using Packages

Default installation of `ReactNativeFFmpeg` using instructions in `2.1` and `2.2` enables the default package, which is based 
on `https` package. It is possible to enable other installed packages using following steps.  

#### 2.3.1 Android

- Edit `android/settings.gradle` file and modify `projectDir` for `react-native-ffmpeg` by appending package name at
the end of the path.
    ```
    project(':react-native-ffmpeg').projectDir = new File(rootProject.projectDir, '../node_modules/react-native-ffmpeg/android/<package name>')
    ```

#### 2.3.2 IOS

- Edit `ios/Podfile` file and modify `podspec` path for `react-native-ffmpeg` by appending package name at the end of 
the name. After that run `pod install` again.
    ```
    pod 'react-native-ffmpeg-<package name>', :podspec => '../node_modules/react-native-ffmpeg/ios/react-native-ffmpeg-<package name>.podspec'
    ```

### 3. Using

1. Execute commands.
    ```
    import { LogLevel, RNFFmpeg } from 'react-native-ffmpeg';
    
    RNFFmpeg.execute('-i file1.mp4 -c:v mpeg4 file2.mp4');
    ```

2. Check execution output.
    ```
    RNFFmpeg.getLastReturnCode().then(result => {
        console.log("Last return code: " + result.lastRc);
    });

    RNFFmpeg.getLastCommandOutput().then(result => {
        console.log("Last command output: " + result.lastCommandOutput);
    });
    ```

3. Stop an ongoing operation.
    ```
    RNFFmpeg.cancel();
    ```

4. Get media information for a file.
    ```
    RNFFmpeg.getMediaInformation('<file path or uri>').then(info => {
        console.log('Result: ' + JSON.stringify(info));
    });
    ```

5. List enabled external libraries.
    ```
    RNFFmpeg.getExternalLibraries().then(externalLibraries => {
        console.log(externalLibraries);
    });
    ```

6. Enable log callback.
    ```
    logCallback = (logData) => {
        console.log(logData.log);
    };
    ...
    RNFFmpeg.enableLogCallback(this.logCallback);
    ```

7. Enable statistics callback.
    ```
    statisticsCallback = (statisticsData) => {
        console.log('Statistics; frame: ' + statisticsData.videoFrameNumber.toFixed(1) + ', fps: ' + statisticsData.videoFps.toFixed(1) + ', quality: ' + statisticsData.videoQuality.toFixed(1) +
        ', size: ' + statisticsData.size + ', time: ' + statisticsData.time);
    };
    ...
    RNFFmpeg.enableStatisticsCallback(this.statisticsCallback);
    ```
    
8. Set log level.
    ```
    RNFFmpeg.setLogLevel(LogLevel.AV_LOG_WARNING);
    ```

9. Register custom fonts directory.
    ```
    RNFFmpeg.setFontDirectory('<folder with fonts>');
    ```
    
### 4. Versions

#### 4.1 Releases

- `0.1.x` releases are based on `FFmpeg v4.0.2` and `MobileFFmpeg v2.x` 
- `0.2.x` releases are based on `FFmpeg v4.1-dev` and `MobileFFmpeg v3.x`

#### 4.1 Source Code

- `master` includes latest released version `v0.2.1`
- `development` branch includes new features and unreleased fixes

### 5. Updates

Refer to [Changelog](CHANGELOG.md) for updates.

### 6. Tips

Apply provided solutions if you encounter one of the following issues.

- Sometimes `react-native run-ios` fails with weird build errors. Execute commands below and try again.

    ```
    rm -rf ios/Pods ios/build ios/Podfile.lock
    cd ios
    pod install
    ```

- Add `"postinstall": "sed -i '' 's\/#import <RCTAnimation\\/RCTValueAnimatedNode.h>\/#import \"RCTValueAnimatedNode.h\"\/' ./node_modules/react-native/Libraries/NativeAnimation/RCTNativeAnimatedNodesManager.h"` 
line to the scripts section of your package.json as recommended in [react-native issue # 13198](https://github.com/facebook/react-native/issues/13198#issuecomment-302917321), 
if your build receives the following error for IOS.

    ```
    ../node_modules/react-native/Libraries/NativeAnimation/RCTNativeAnimatedNodesManager.h:10:9: fatal error: 'RCTAnimation/RCTValueAnimatedNode.h' file not found
    #import <RCTAnimation/RCTValueAnimatedNode.h>
            ^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    1 error generated.
    ```

- When `pod install` is not successful with the following message, delete `Podfile.lock` file and run `pod install` again.

    ```
    [!] Unable to find a specification for 'react-native-ffmpeg'.
    ```

- If `react-native link` is used for IOS linking, building may fail with this error. Running `pod install` again 
fixes this issue.

    ```
    ../node_modules/react-native-ffmpeg/ios/Pods/Target Support Files/Pods-ReactNativeFFmpeg/Pods-ReactNativeFFmpeg.debug.xcconfig: unable to open file (in target "ReactNativeFFmpeg" in project "ReactNativeFFmpeg") (in target 'ReactNativeFFmpeg')
    ```
    
- Using `cocoapods` for IOS dependency management may produce duplicate symbols for `libReact.a` and `libyoga.a`. 
Add the following block to your `Podfile` and run `pod install` again.
 
    ```
    post_install do |installer|
        installer.pods_project.targets.each do |target|
          targets_to_ignore = %w(React yoga)
          if targets_to_ignore.include? target.name
            target.remove_from_project
          end
        end
    end

    ```

### 7. Test Application

You can see how `React Native FFmpeg` is used inside an application by running test applications provided under [react-native-ffmpeg-test](https://github.com/tanersener/react-native-ffmpeg-test) repository. All applications provide the same functionality; performs command execution and video encoding operations. The difference between them is IOS dependency management mechanism applied.

<img src="https://github.com/tanersener/react-native-ffmpeg/raw/master/docs/assets/ios_test_app.gif" width="240">

### 8. License

This project is licensed under the LGPL v3.0. However, if installation is customized to use a package with `-gpl` postfix (min-gpl, https-gpl, full-gpl) then `React Native FFmpeg` is subject to the GPL v3.0 license.

Digital assets used in test applications are published in the public domain.

### 9. Contributing

Feel free to submit issues or pull requests.

### 10. See Also

- [FFmpeg](https://www.ffmpeg.org)
- [Mobile FFmpeg Wiki](https://github.com/tanersener/mobile-ffmpeg/wiki)
- [FFmpeg License and Legal Considerations](https://ffmpeg.org/legal.html)
