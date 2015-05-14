# cocos jscompile

## Overview

Compile the `.js` files to `.jsc`.

## Usage

`cocos jscompile -s src_dir -d dst_dir [-c] [-o COMPRESSED_FILENAME] [-j COMPILER_CONFIG] [-m closure_extra_parameters] -v`

## Available Arguments

arg | available value | sample | description | necessary
:------------: | :-------------: | :------------: | :------------: | :------------:
-h, --help | - | - | Show the help message and exit  | no
-s, --src | source directory | 	`./projects/MyJSGame/src` | Specify source directory of js files needed to be compiled. | yes
-d, --dst | destination directory | `./projects/MyJSGame/src` | Specify destination directory bytecode files to be stored. | yes
-c, --use_closure_compiler | - | - | Whether to use closure compiler to compress all js files into just a big file. | no
-o, --output_compressed_filename | any string | `MyJS.js` | Specify the output file name of the big file. Only available when '-c' option is used | no
-j, --compiler_config | - | - | The configuration for closure compiler by using JSON, please refer to compiler_config_sample.json | no
-m, --closure_params | - | - | Extra parameters to pass to Google Closure Compiler. Values supplied here override the ones defined in the compiler config. | no

## Samples

* `cocos jscompile -h`. Show the help message.
* `cocos jscompile -s ./projects/MyJSGame/src -d ./projects/MyJSGame/src`  
	Compile the `*.js` in directory `./projects/MyJSGame/src` to `*.jsc`