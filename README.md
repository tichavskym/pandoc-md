## About

This script converts .md files to .html files through utility called *[pandoc](https://pandoc.org/)* **(which has to be installed on the machine).** It lets you specify an array of directories or files in arguments, so you don't have to convert them manually one by one. Script also checks for existing html files and if they are up to date (based on modification date difference between .md and .html) they don't get recompiled to prevent unnecessary writes.

## Usage:

```bash
    icaled [options] [paths]
```

- `-h` show help

SWITCH OPTIONS (one of these is mandatory)

- `-d` convert specified directories
- `-i` convert specified files
- `-t` convert this (local) folder

OPTIONAL OPTIONS

- `-s` choose stylesheet to be linked to the resulting `.html` files
- `-f` force option - skips the check if files are up to date
- `-r` recursively convert folders (convert files in the working directory and in all containing directories)

If you keep using the same style file for the most of your scripts, you can set an environment variable `PANDOC_MD_STYLE` to contain a path to that script. The path in `PANDOC_MD_STYLE` will be used by default (that is when you don't use `-s` option).
