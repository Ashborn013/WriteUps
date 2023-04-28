## Super SUS

use [zsteg](https://github.com/zed-0xff/zsteg) on the file png image 
```
 $ zsteg chall_sus.png

imagedata           .. text: "GGG111   $$$"
b1,r,lsb,xy         .. text: "Bwq<R1Z'/"
b1,rgb,lsb,xy       .. text: "44:WGlvbWFyYXtsNDV0X2J1dF9uMHRfdGgzX2wzNDV0fQo=?"
b1,bgr,lsb,xy       .. file: OpenPGP Secret Key
b4,b,lsb,xy         .. file: AIX core file fulldump 64-bit
b4,b,msb,xy         .. file: MPEG ADTS, layer I, v2, 112 kbps, 24 kHz, JntStereo
```
this is `WGlvbWFyYXtsNDV0X2J1dF9uMHRfdGgzX2wzNDV0fQo=` is base64 decode this and you get the flag 
`Xiomara{l45t_but_n0t_th3_l345t}`

another way to solve is the put the image in the online wesite [aperisolve](http://www.aperisolve.com/)
which will run the image with most common tools if we navigate to zsteg we see same output
