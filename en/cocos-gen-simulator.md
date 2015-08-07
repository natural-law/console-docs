# cocos gen-simulator

## Overview

Generate Cocos Simulator.

## Usage

`usage: cocos gen-simulator [-h] [-c] [-e ENGINE_PATH] [-m {debug,release}]
                           [-o OUT_DIR] [-p {ios,mac,android,win32}]
                           [--vs VS_VERSION]`

## Available Arguments

arg | available value | sample | description | necessary
:------------: | :-------------: | :------------: | :------------: | :------------:
-h, --help | - | - | Show the help message and exit  | no
-c | - | - | Remove the 'prebuilt' folder at first. | no
-e | Path of engine. | `~/Work/cocos2d-x` | Specify the engine path. Default is the engine root path of current tools. | no
-m | debug, release | `debug` | Generate cocos libs for debug or release. Default is release. | no
-o, --output | The output path. | `~/MySimulator` | Where to save Cocos Simulator. Default is the `simulator` folder in the root path of engine. | no
-p | ios, mac, android, win32 | `mac` | Specify the target platform. Can specify multi platform by using '-p' multi times. Default generate all available platforms. | no
--vs | int value | `2013` | Specify the Visual Studio version will be used. Such as: 2013. Default find available version automatically. | no

## Attentions

* The available target platform is different for Mac, Windows, Linux:
	
	* Mac : ios, mac, android  
	* Windows : android, win32  
	* Linux : android

* If you want to generate prebuilt libs for multi targat platforms, you can use `-p` multi times. For example: `-p ios -p mac` will generate prebuilt libs for both ios & mac.

## Samples

* `cocos gen-simulator -h`. Show the help message.
* `cocos gen-simulator -c`  
Remove the specified output directory. Then generate simulator for all available target platforms.
* `cocos gen-simulator -e ~/Work/cocos2d-x -o ~/MySimulator -p ios -p android`  
Specify the engine path `~/Work/cocos2d-x`. Then generate simulator for iOS & Android, output the simulator to `~/MySimulator`.
* `cocos gen-simulator -p win32 --vs 2015 -m debug`  
Generate simulator for Win32 with VS2015 & debug mode.
