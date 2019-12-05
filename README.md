indent
======

A small tool to convert (or enforce) text file indentation. Tabs to spaces or spaces to tabs.

Installation
------------

Install via [composer](https://packagist.org/packages/cebe/indent) or just clone the repo.

### Global installation

Install it globally using:

    composer global require cebe/indent

Make sure your composer directory (`$HOME/.composer/vendor/bin`) is in your `PATH`.    

Usage
-----

    indent [--tabs|--spaces] [-r [--pattern=...]] [files or directories...]

    --tabs       convert all indentation to tabs. Assuming 4 spaces tab length.
    --spaces     convert all indentation to spaces.

    -r           recursively go over all directories given as argument and convert
                 files that match --pattern.

    --pattern    the pattern to match files for when using -r. Defaults to '*.php'.

    --tabstop=N  define number of spaces N to replace a tab with. Defaults to 4.

    --help       shows this usage information.

    If no file is specified input will be read from STDIN.

Examples
--------

Convert `myfile.php` to tabs:

    indent --tabs myfile.php

Convert all `.php`-files and the `README.md` in current dir to spaces:

    indent --spaces *.php README.md

Convert all `.php`-files in `dir` to tabs (recursively):

    indent --tabs -r dir

Convert all `.md`-files in dir to spaces (recursively):

    indent --spaces --pattern=*.md -r dir

Convert STDIN, which is the content of `myfile.php` to spaces and print the result to STDOUT:

    cat myfile.php | ./indent --spaces
