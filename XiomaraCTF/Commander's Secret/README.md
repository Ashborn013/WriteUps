## Commander's Secret

in this challenge you are given a image file first things first lets [binwalk](https://github.com/ReFirmLabs/binwalk/tree/master) the image and we will get this 
```
->binwalk  ervin.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             JPEG image data, JFIF standard 1.01
30            0x1E            TIFF image data, little-endian offset of first image directory: 8
110814        0x1B0DE         Zip archive data, encrypted at least v2.0 to extract, compressed size: 572, uncompressed size: 1322, name: flag.txt
111546        0x1B3BA         End of Zip archive, footer length: 22

```
