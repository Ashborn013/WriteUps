## Zip It Up

a zip file was provied for this challenge
if you try to unzip you would get a error like this 
```
unzip 1001.zip
Archive:  1001.zip
file #1:  bad zipfile offset (local header sig):  0
```
which would indicate ther is a problem with the header 

open the file any hex editor i will use [ghex](https://github.com/GNOME/ghex.git)
<img src="img/zipit_img1.png">

if you check the [magic number of file](https://en.wikipedia.org/wiki/List_of_file_signatures) you can see a zip file header starts with `PK` not `pk` by corecting this we can unzip the file 
after unziping we get another archive of .rar unzip it again we get another one ,now we just need to write a script to automate this process
here is a python script which which will do this task 

```python
#!/bin/python3
import os
for i in range(0,1001):
    #print(101-i)
    os.system(f'./unarc.sh {1001-i}.*')
    os.system(f'rm -rf {101-i}.*')
```
unarc.sh
```bash
    if [ -f $1 ] ; then
            case $1 in
            *.tar.bz2)    tar xvjf $1    ;;
            *.tar.gz)    tar xvzf $1    ;;
            *.tar.xz)    tar xf $1      ;;
            *.bz2)        bunzip2 $1     ;;
            *.rar)        unrar x $1     ;;
            *.gz)        gunzip $1      ;;
            *.tar)        tar xvf $1     ;;
            *.tbz2)        tar xvjf $1    ;;
            *.tgz)        tar xvzf $1    ;;
            *.zip)        unzip $1       ;;
            *.Z)        uncompress $1  ;;
            *.7z)        7z x $1        ;;
            *)        echo "I don't know how to unzip this '$1'..." ;;
            esac
    else
            echo "'$1' is not a valid file!"
    fi

```
note : unarc.sh is shell script i wrote which will unarchive most of the file archive formats 

run the python script and you will end up with `0.tar.gz` unarchive it and `flag.zip` and unzip that vola `flag.txt` which has the flag `Xiomara{d0wn_the_h0le_we_meRRy_g0}`

