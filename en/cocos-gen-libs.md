# cocos gen-libs

## Overview

Generate prebuilt libs of engine. The libs will be placed in `prebuilt` folder of the engine root path.

## Usage

```
usage: cocos gen-libs [-h] [-c] [-e ENGINE_PATH] [-p {ios,mac,android,win32}]
                      [-m {debug,release}] [--dis-strip] [--vs VS_VERSION]
                      [--app-abi APP_ABI]
```

## Available Arguments

* **Common Arguments:**

	arg | available value | sample | description | necessary
	:------------: | :-------------: | :------------: | :------------: | :------------:
	-h, --help | - | - | Show the help message and exit  | no
	-c | - | - | Remove the 'prebuilt' folder at first. | no
	-e | Path of engine. | `~/Work/cocos2d-x` | Specify the engine path. Default is the engine root path of current tools. | no
	-p | ios, mac, android, win32 | `mac` | Specify the target platform. Can specify multi platform by using '-p' multi times. Default generate all available platforms. | no
	-m | debug, release | `debug` | Generate cocos libs for debug or release. Default is release. | no
	--dis-strip | - | - | Disable the strip of the generated libs. | no

* **Android Arguments:**

	arg | available value | sample | description | necessary
	:------------: | :-------------: | :------------: | :------------: | :------------:
	--app-abi | x86, armeabi, armeabi-v7a | `armeabi:x86` | Set the APP_ABI of ndk-build. Can be multi value separated with ':'. Sample : --app-aib armeabi:x86:mips. Default value is 'armeabi'. | no
	
* **Windows Arguments:**

	arg | available value | sample | description | necessary
	:------------: | :-------------: | :------------: | :------------: | :------------:
	--vs | int value | `2013` | Specify the Visual Studio version will be used. Such as: 2013. Default find available version automatically. | no

## Attentions

* The available target platform is different for Mac, Windows, Linux:
	
	* Mac : ios, mac, android  
	* Windows : android, win32  
	* Linux : android

* If you want to generate prebuilt libs for multi targat platforms, you can use `-p` multi times. For example: `-p ios -p mac` will generate prebuilt libs for both ios & mac.

## Samples

* `cocos gen-libs -h`. Show the help message.
* `cocos gen-libs -c`  
Remove the `prebuilt` folder. Then generate prebuilt libs for all available target platforms.
* `cocos gen-libs -e ~/Work/cocos2d-x -p ios -p android`  
Specify the engine path `~/Work/cocos2d-x`. Then generate prebuilt libs for ios & android
* `cocos gen-libs -p win32 --vs 2015 -m debug`  
Generate prebuilt libs for win32 with VS2015 & debug mode.
