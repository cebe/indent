indent
======

A small tool to convert text file indentation.

Installation
------------

Install via [composer](https://packagist.org/packages/cebe/indent) or just clone the repo.

Usage
-----

    indent [--tabs|--spaces] [file1 file2 ...]

    --tabs    convert all indentation to tabs. Assuming 4 spaces tab length.
    --spaces  convert all indentation to spaces.

    --help    shows this usage information.

    If no file is specified input will be read from STDIN.

Examples:

- `indent --tabs myfile.php` - convert myfile.php
- `indent --spaces dir/*.php` - all php files in `dir`
