# BiwaScheme Reading Guide

This is a brief guide for reading the source code of BiwaScheme.

## Directory organization

- bin/
  - biwas : Entry point of the `biwas` command (installed by `npm install biwascheme -g`)
- release/
  - biwascheme.js : Generated by `make` command
- src/
  - deps/ : Contains dependent JavaScript libraries (such as underscore.js)
  - library/ : Library functions
  - platforms/ : Code only runs on a certain platform (browser or Node)
  - system/ : Main source code of BiwaScheme
  - development_initializer.js
  - header.js
  - version.js
  - version.js.in
- test/
  - unit.js : Unit test
  - spec.html : Runs unit test

Some of the most important files are:

- src/library/r6rs_lib.js 
  - Contains most of the library functions
- src/system/parser.js
  - `BiwaScheme.Parser` parses Scheme program (given as JavaScript String)
- src/system/compiler.js
  - `BiwaScheme.Compiler` compiles parsed program into BiwaScheme intermediate language
- src/system/interpreter.js
  - `BiwaScheme.Interpreter` executes the intermediate lanugage

## The intermediate language

See [internal/opecodes](opecodes.html).
