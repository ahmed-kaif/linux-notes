# Metadata Anonymisation Toolkit 2 (pkg: mat2)

>Metadata can expose many sensative information about the device we used. It is wiser to clean the data and then upload it to the web. The **Metadata Anonymisation Toolkit 2** (mat2) can be very helpful in this regard.

To install it in debian based distro:
```sh
$ sudo apt install mat2
```
### Mat2 options and flags:
---
```powershell
$ mat2 -h

usage: mat2 [-h] [-V] [--unknown-members policy] [--inplace] [--no-sandbox] [-v] [-l]
            [--check-dependencies] [-L | -s]
            [files [files ...]]

Metadata anonymisation toolkit 2

positional arguments:
  files                 the files to process

optional arguments:
  -h, --help            show this help message and exit
  -V, --verbose         show more verbose status information
  --unknown-members policy
                        how to handle unknown members of archive-style files (policy should be one
                        of: abort, omit, keep) [Default: abort]
  --inplace             clean in place, without backup
  --no-sandbox          Disable bubblewrap's sandboxing.
  -v, --version         show program's version number and exit
  -l, --list            list all supported fileformats
  --check-dependencies  check if mat2 has all the dependencies it needs
  -L, --lightweight     remove SOME metadata
  -s, --show            list harmful metadata detectable by mat2 without removing them
```
---
```powershell
$ mat2 -s <file> # Displaying Metadata For A Single File
```
```powershell
$ mat2 <file> # Removes all the metadata and create a new file <file>.cleaned.*
```
This will create a new file with the same name appended with *.cleaned* at the last. like `<file>.cleaned.<file_format>`

**To avoid creating a new file:**
```powershell
$ mat2 --inplace <file> # this will remove all the metadata but no new file will be created
```
```powershell
$ mat2 -s /path/to/folder # Shows metadata for all files in the folder

$ mat2 /path/to/folder # cleans metadata for all files and creates a new file for each
```
