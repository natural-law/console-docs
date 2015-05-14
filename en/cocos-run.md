# cocos run

## Overview

Compiles & deploy project and then run it on the target.

## Usage

```
cocos run [-h] [-s SRC_DIR] [-q] [-p PLATFORM] [-m MODE]
          [--host [SERVER_HOST]] [SERVER_PORT]
```

## Depend on Commands

* [deploy](cocos-deploy.md)

## Available Arguments

* **Common Arguments:**  

	arg | available value | sample | description | necessary
	:------------: | :-------------: | :------------: | :------------: | :------------:
	-h, --help | - | - | Show the help message and exit  | no
	-s, --src | project path | 	`./projects/MyLuaGame` | Specify the project path. Default value is current directory. | no
	-p, --platform | the target platform | `android` | Specify the target platform. | yes
	-m, --mode | the compiling mode | `release` | Set the compile mode, should be `debug` or `release`. Default is debug. | no
* **Web project Arguments:**

	arg | available value | sample | description | necessary
	:------------: | :-------------: | :------------: | :------------: | :------------:
	--host | host ip of server | `127.0.0.1` | Set the host of the local web server, defualt is `127.0.0.1`. | no
	SERVER_PORT | the port of server | `8000` | Set the port of the local web server, defualt is 8000 | no


## Attentions

* Now not support run project on iOS device with `-m, -mode` is release.

## Samples

* `cocos run -h`. Show the help message.
* `cocos run -s ./projects/MyLuaGame -p android -m release`  
	Build `MyLuaGame` with release mode & run it on android device or simulator.