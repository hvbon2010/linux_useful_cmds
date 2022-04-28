# Change a file name
`mv abc.xxx def.xxx`

# Create a new file
`touch abc.xxx`

# Find all files with pattern matching
`find [path] -name [patern]`

Example: `find ./out/ -name '*skgraphics*'`

# Find contents in all files of a folder
`grep -rnw [path] -e pattern`

Example: `grep -rnw /home/hvbon/MAC/.microej/ -e "systemMicroUI"`

# Excute command
Remove all files with pattern matching in a folder:

`find [path] -name [patern] -exec rm -rf {} \;`

Example: `find ./out/ -name '*skgraphics*' -exec rm -rf {} \;`

Change extension of a all files in a folder:

`find [path] -name abc.xxx -exec rename 's/\.xxx$/.yyy/' \{} \;`

`xxx`: old extension.

`yyy`: new extension.

Example: `find ./ -name README.MD -exec rename 's/\.MD$/.md/' \{} \;`

# Compress/Decompress
## tar
`tar [options] [archive-file] [file or directory to be archived]`

Options:

`-c` : Creates Archive

`-x` : Extract the archive

`-f` : creates archive with given filename

`-t` : displays or lists files in archived file

`-u` : archives and adds to an existing archive file

`-v` : Displays Verbose Information

`-A` : Concatenates the archive files

`-z` : zip, tells tar command that creates tar file using gzip

`-j` : filter archive tar file using tbzip

`-W` : Verify a archive file

`-r` : update or add file or directory in already existed .tar file

`-C` : set directory to extract files

Compress file/folder:

`tar -czvf [archive-file] [file or directory to be archived]`

Example:

`tar -czvf WebRTC.tar.gz WebRTC/`

Decompress file/folder:

`tar -xzvf [archive-file] -C [file or directory to be archived]`

Example:

`tar -xzvf WebRTC.tar.gz`

`tar -xzvf WebRTC.tar.gz -C /mnt/ext_ssd/`

## zip/unzip

`zip -r abc.zip abc/`

`unzip abc.zip -d abc`

## Note when use copy cmd
Do not use the / at the end of folder when copy folder to other directory

Ex: ~~`cp -r /Volumes/VirtualHereUniversal/VirtualHereUniversal.app/ ~/Applications`~~

Must use: `cp -r /Volumes/VirtualHereUniversal/VirtualHereUniversal.app ~/Applications`
