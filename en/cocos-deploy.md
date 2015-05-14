# cocos deploy

## Overview

Deploy a project to the target.

## Usage

`cocos deploy [-h] [-s SRC_DIR] [-q] [-p PLATFORM] [-m MODE]`

## Depend on Commands

* [compile](cocos-compile.md)

## Available Arguments

arg | available value | sample | description | necessary
:------------: | :-------------: | :------------: | :------------: | :------------:
-h, --help | - | - | Show the help message and exit  | no
-s, --src | project path | 	`./projects/MyLuaGame` | Specify the project path. Default value is current directory. | no
-p, --platform | the target platform | `android` | Specify the target platform. | yes
-m, --mode | the compiling mode | `release` | Set the compile mode, should be `debug` or `release`. Default is debug. | no

## Attentions

* Now this command only take effect when target platform is `android`. It will re-install the specified project to the android device or simulator.

## Samples

* `cocos deploy -h`. Show the help message.
* `cocos deploy -s ./projects/MyLuaGame -p andoird -m release`  
	Deploy `MyLuaGame` to an android device or simulator.