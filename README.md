## About

This script converts .md files to .html files through utility called *[pandoc](https://pandoc.org/)* **(which has to be installed on the machine).** It lets you specify array of directories or files in arguments, so you don't have to convert them manually one by one. Script also checks for existing html files and if they are up to date (based on modification date difference between .md and .html) they don't get recompiled to prevent unnecessary writes.

## Usage:

```bash
    icaled [options] [paths]

    -h          show help
```

SWITCH OPTIONS (one of these is mandatory)

- `-d` convert specified directories
- `-i` convert specified files
- `-t` convert this (local) folder

OPTIONAL OPTIONS

- `-s` choose stylesheet to be linked to the resulting `.html` files
- `-f` force option - skips the check if files are up to date