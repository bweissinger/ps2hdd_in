# ps2hdd_in

`ps2hdd_in` is a bash script utilizing `hdl-dump` to make the process of transferring backup .ios's to a PS2 hdd quicker and easier. `ps2hdd_in` has several handy features.

The default behavior is to install all images in the specified directory to the given PS2 HDD,
using the filename as the title. If a file is passed instead of directory,
it will install only the specified file. It will not install image if the
Game ID already exists in the PS2 HDD. Will use default values of
`dma = *u4`, `media = cd` for .cue, and `media = dvd` for .iso and all other valid image
formats, unless flags are specified.

`ps2hdd_in` allows for title retrieval by index file through use of flag `-i` and specifying the index file. The index file must be a semicolon ";" delineated .csv or .txt file.
Each line is one entry and consists of:  
Game Title;Region Code;GameID  

For example:  
Ape Escape 3;NTSC-U;SCUS-97501  
Ape Escape 3;PAL-Unk;SCES-53642  
...  
Armored Core - Silent Line;PAL-Unk;SLES-52203  
...  
