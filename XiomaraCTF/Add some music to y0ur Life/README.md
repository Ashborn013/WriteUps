## Add some music to y0ur Life

you are given a audio file if played till it end you would hear some noise which is morse code by decoding this we get `F4K3FLAGBUTU53FULL`
if you try submiting this it would show incorrect flag

if you search for stegno tools for mp3 you will come acrose [mp3stegno](https://github.com/fabienpe/MP3Stego)
clone the repo and move the mp3 file into the  repo and run the cmd if you are using linux `wine Decode.exe -X -P F4K3FLAGBUTU53FULL final_chal.mp3`

```
 $ wine Decode.exe -X -P F4K3FLAGBUTU53FULL final_chal.mp3
007c:fixme:hid:handle_IRP_MN_QUERY_ID Unhandled type 00000005
007c:fixme:hid:handle_IRP_MN_QUERY_ID Unhandled type 00000005
007c:fixme:hid:handle_IRP_MN_QUERY_ID Unhandled type 00000005
007c:fixme:hid:handle_IRP_MN_QUERY_ID Unhandled type 00000005
MP3StegoEncoder 1.1.19
See README file for copyright info
Input file = 'final_chal.mp3'  output file = 'final_chal.mp3.pcm'
Will attempt to extract hidden information. Output: final_chal.mp3.txt
the bit stream file final_chal.mp3 is a BINARY file
HDR: s=FFF, id=1, l=3, ep=off, br=9, sf=0, pd=1, pr=0, m=0, js=0, c=0, o=0, e=0
alg.=MPEG-1, layer=III, tot bitrate=128, sfrq=44.1
mode=stereo, sblim=32, jsbd=32, ch=2
[Frame 2207]Avg slots/frame = 417.771; b/smp = 2.90; br = 127.942 kbps
Decoding of "final_chal.mp3" is finished
The decoded PCM output file name is "final_chal.mp3.pcm"
0024:fixme:kernelbase:AppPolicyGetProcessTerminationMethod FFFFFFFA, 00596D5C
```
the output have been saved in final_chall.mp3.txt
and the flag is `Xiomara{4ud10_5t3g0_15_fun_but_d33p}`
