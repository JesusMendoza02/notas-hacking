# Concurso CTF


## Objetivo 

A Traffic from an unknown user has been captured, analyze this capture and find out what happened

Remember to use the flag format: flagmx{XXXX}
## Solución 

```
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ xxd -100 r4.pcap 
Usage:
       xxd [options] [infile [outfile]]
    or
       xxd -r [-s [-]offset] [-c cols] [-ps] [infile [outfile]]
Options:
    -a          toggle autoskip: A single '*' replaces nul-lines. Default off.
    -b          binary digit dump (incompatible with -ps,-i,-r). Default hex.
    -C          capitalize variable names in C include file style (-i).
    -c cols     format <cols> octets per line. Default 16 (-i: 12, -ps: 30).
    -E          show characters in EBCDIC. Default ASCII.
    -e          little-endian dump (incompatible with -ps,-i,-r).
    -g          number of octets per group in normal output. Default 2 (-e: 4).
    -h          print this summary.
    -i          output in C include file style.
    -l len      stop after <len> octets.
    -o off      add <off> to the displayed file position.
    -ps         output in postscript plain hexdump style.
    -r          reverse operation: convert (or patch) hexdump into binary.
    -r -s off   revert with <off> added to file positions found in hexdump.
    -s [+][-]seek  start at <seek> bytes abs. (or +: rel.) infile offset.
    -u          use upper case hex letters.
    -v          show version: "xxd V1.10 27oct98 by Juergen Weigert".
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ xxd -l 100 r4.pcap 
00000000: d4c3 b2a1 0200 0400 0000 0000 0000 0000  ................
00000010: 0000 0400 0100 0000 6a66 eb66 9029 0700  ........jf.f.)..
00000020: 4a00 0000 4a00 0000 0800 278d 437e 0800  J...J.....'.C~..
00000030: 27f8 c013 0800 4500 003c 0ef6 4000 4006  '.....E..<..@.@.
00000040: a872 c0a8 0101 c0a8 0102 abc8 0015 2487  .r............$.
00000050: fae6 0000 0000 a002 ffff 8382 0000 0204  ................
00000060: 05b4 0402                                ....
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ wireshark r4.pcap 
^C
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ mv r4.pcap r3.png
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ eog r3.png r3.png

(eog:7778): EOG-WARNING **: 10:02:44.315: Couldn't load icon: El icono «image-loading» no está presente en el tema Adwaita
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ file r3.png 
r3.png: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 262144)
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ mv r3.png r4.pcap
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ ls
r4.pcap
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ wireshark r4.pcap 
^C
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ ls
r3  r4.pcap
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ file r3 
r3: ASCII text, with CRLF line terminators
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ cat r3
220 (vsFTPd 3.0.5)
USER r1
331 Please specify the password.
PASS r1
230 Login successful.
SYST
215 UNIX Type: L8
FEAT
211-Features:
 EPRT
 EPSV
 MDTM
 PASV
 REST STREAM
 SIZE
 TVFS
211 End
TYPE I
200 Switching to Binary mode.
EPSV
229 Entering Extended Passive Mode (|||52688|)
STOR r2.7z
150 Ok to send data.
226 Transfer complete.
EPSV
229 Entering Extended Passive Mode (|||19186|)
STOR r3.png
150 Ok to send data.
226 Transfer complete.
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ wireshark r4.pcap 
^C
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ wireshark r4.pcap &
[1] 7999
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ ls
r3  r4.pcap
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ file r3
r3: PNG image data, 100 x 100, 8-bit/color RGB, non-interlaced
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ mv r3 r3.png
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ eog r3.png 

(eog:8088): EOG-WARNING **: 10:12:03.838: Couldn't load icon: El icono «image-loading» no está presente en el tema Adwaita
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ string r3.png | grep flagmx

Orden «string» no encontrada. Quizá quiso decir:

  la orden «strings» del paquete deb «binutils (2.34-6ubuntu1.9)»
  la orden «spring» del paquete deb «ruby-spring (2.1.0-1)»
  la orden «spring» del paquete deb «spring (104.0+dfsg-4ubuntu7)»

Pruebe con: sudo apt install <nombre del paquete deb>

jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ strings r3.png | grep flagmx
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ ls
r3.png  r4.pcap
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ ls
r2  r3.png  r4.pcap
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ file r2
r2: 7-zip archive data, version 0.4
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ mv r2 r2.7z
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ unzip r2.7z
Archive:  r2.7z
  End-of-central-directory signature not found.  Either this file is not
  a zipfile, or it constitutes one disk of a multi-part archive.  In the
  latter case the central directory and zipfile comment will be found on
  the last disk(s) of this archive.
unzip:  cannot find zipfile directory in one of r2.7z or
        r2.7z.zip, and cannot find r2.7z.ZIP, period.
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ p7zip r2.7z
/usr/bin/p7zip: r2.7z already has the 7z suffix
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ ls
r2.7z  r3.png  r4.pcap
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ string r2.7z | grep flagmx

Orden «string» no encontrada. Quizá quiso decir:

  la orden «spring» del paquete deb «ruby-spring (2.1.0-1)»
  la orden «spring» del paquete deb «spring (104.0+dfsg-4ubuntu7)»
  la orden «strings» del paquete deb «binutils (2.34-6ubuntu1.9)»

Pruebe con: sudo apt install <nombre del paquete deb>

jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ strings r2.7z | grep flagmx
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ 7z x r2.7z 

7-Zip [64] 16.02 : Copyright (c) 1999-2016 Igor Pavlov : 2016-05-21
p7zip Version 16.02 (locale=es_MX.UTF-8,Utf16=on,HugeFiles=on,64 bits,4 CPUs Intel(R) Core(TM) i5-2520M CPU @ 2.50GHz (206A7),ASM,AES-NI)

Scanning the drive for archives:
1 file, 222 bytes (1 KiB)

Extracting archive: r2.7z

Enter password (will not be echoed):
--
Path = r2.7z
Type = 7z
Physical Size = 222
Headers Size = 190
Method = LZMA2:12 7zAES
Solid = -
Blocks = 1

Everything is Ok

Size:       16
Compressed: 222
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ ls
r1.txt  r2.7z  r3.png  r4.pcap
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ cat r1.txt 
flagmx{cuv4v3}
jesus@jesus-ThinkPad-T420:~/ConcuroCTFOct15/network/uhhaha$ 

```

## Notas adicionales 

## Referencias 
