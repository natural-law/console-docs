# cocos luacompile

## Overview

Compile the `.lua` files to `.luac`.

## Usage

`cocos luacompile [arguments]`

## Available Arguments

arg | available value | sample | description | necessary
:------------: | :-------------: | :------------: | :------------: | :------------:
-h, --help | - | - | Show the help message and exit  | no
-s, --src | source directory | 	`./projects/MyLuaGame/src` | Specify source directory of lua files needed to be compiled. | yes
-d, --dst | destination directory | `./projects/MyLuaGame/src` | Specify destination directory bytecode files to be stored. | yes
-e, --encrypt | - | - | Enable the encrypting of lua files. | no
-k, --encryptkey | any string | `MyLuaKey` | Specify the encrypt key for the encrypting of lua scripts. It's only take effect when `-e, --encrypt` is enabled. Default value is `2dxLua`. | no
-b, --encryptsign | any string | `MyLuaSign` |  Specify the encrypt sign for the encrypting of lua scripts. It's only take effect when `--encrypt` is enabled. Default value is `XXTEA`. | no

## Samples

* `cocos luacompile -h`. Show the help message.
* `cocos luacompile -s ./projects/MyLuaGame/src -d ./projects/MyLuaGame/src -e -k MyLuaKey -b MyLuaSign`  
	Compile the `*.lua` in directory `./projects/MyLuaGame/src` to `*.luac`. Then encrypt the luac files with key is `MyLuaKey` and sign is `MyLuaSign`.