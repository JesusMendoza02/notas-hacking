# Level 15 al Level 16

## Objetivo 
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL/TLS encryption.

**Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.**
## Datos de acceso al nivel 
**bandit.labs.overthewire.org**
cuenta
**bandit15**
passw
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo


## Solución 
```bash
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = SnakeOil
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = SnakeOil
verify return:1
---
Certificate chain
 0 s:CN = SnakeOil
   i:CN = SnakeOil
   a:PKEY: rsaEncryption, 4096 (bit); sigalg: RSA-SHA256
   v:NotBefore: Jun 10 03:59:50 2024 GMT; NotAfter: Jun  8 03:59:50 2034 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIFBzCCAu+gAwIBAgIUBLz7DBxA0IfojaL/WaJzE6Sbz7cwDQYJKoZIhvcNAQEL
BQAwEzERMA8GA1UEAwwIU25ha2VPaWwwHhcNMjQwNjEwMDM1OTUwWhcNMzQwNjA4
MDM1OTUwWjATMREwDwYDVQQDDAhTbmFrZU9pbDCCAiIwDQYJKoZIhvcNAQEBBQAD
ggIPADCCAgoCggIBANI+P5QXm9Bj21FIPsQqbqZRb5XmSZZJYaam7EIJ16Fxedf+
jXAv4d/FVqiEM4BuSNsNMeBMx2Gq0lAfN33h+RMTjRoMb8yBsZsC063MLfXCk4p+
09gtGP7BS6Iy5XdmfY/fPHvA3JDEScdlDDmd6Lsbdwhv93Q8M6POVO9sv4HuS4t/
jEjr+NhE+Bjr/wDbyg7GL71BP1WPZpQnRE4OzoSrt5+bZVLvODWUFwinB0fLaGRk
GmI0r5EUOUd7HpYyoIQbiNlePGfPpHRKnmdXTTEZEoxeWWAaM1VhPGqfrB/Pnca+
vAJX7iBOb3kHinmfVOScsG/YAUR94wSELeY+UlEWJaELVUntrJ5HeRDiTChiVQ++
wnnjNbepaW6shopybUF3XXfhIb4NvwLWpvoKFXVtcVjlOujF0snVvpE+MRT0wacy
tHtjZs7Ao7GYxDz6H8AdBLKJW67uQon37a4MI260ADFMS+2vEAbNSFP+f6ii5mrB
18cY64ZaF6oU8bjGK7BArDx56bRc3WFyuBIGWAFHEuB948BcshXY7baf5jjzPmgz
mq1zdRthQB31MOM2ii6vuTkheAvKfFf+llH4M9SnES4NSF2hj9NnHga9V08wfhYc
x0W6qu+S8HUdVF+V23yTvUNgz4Q+UoGs4sHSDEsIBFqNvInnpUmtNgcR2L5PAgMB
AAGjUzBRMB0GA1UdDgQWBBTPo8kfze4P9EgxNuyk7+xDGFtAYzAfBgNVHSMEGDAW
gBTPo8kfze4P9EgxNuyk7+xDGFtAYzAPBgNVHRMBAf8EBTADAQH/MA0GCSqGSIb3
DQEBCwUAA4ICAQAKHomtmcGqyiLnhziLe97Mq2+Sul5QgYVwfx/KYOXxv2T8ZmcR
Ae9XFhZT4jsAOUDK1OXx9aZgDGJHJLNEVTe9zWv1ONFfNxEBxQgP7hhmDBWdtj6d
taqEW/Jp06X+08BtnYK9NZsvDg2YRcvOHConeMjwvEL7tQK0m+GVyQfLYg6jnrhx
egH+abucTKxabFcWSE+Vk0uJYMqcbXvB4WNKz9vj4V5Hn7/DN4xIjFko+nREw6Oa
/AUFjNnO/FPjap+d68H1LdzMH3PSs+yjGid+6Zx9FCnt9qZydW13Miqg3nDnODXw
+Z682mQFjVlGPCA5ZOQbyMKY4tNazG2n8qy2famQT3+jF8Lb6a4NGbnpeWnLMkIu
jWLWIkA9MlbdNXuajiPNVyYIK9gdoBzbfaKwoOfSsLxEqlf8rio1GGcEV5Hlz5S2
txwI0xdW9MWeGWoiLbZSbRJH4TIBFFtoBG0LoEJi0C+UPwS8CDngJB4TyrZqEld3
rH87W+Et1t/Nepoc/Eoaux9PFp5VPXP+qwQGmhir/hv7OsgBhrkYuhkjxZ8+1uk7
tUWC/XM0mpLoxsq6vVl3AJaJe1ivdA9xLytsuG4iv02Juc593HXYR8yOpow0Eq2T
U5EyeuFg5RXYwAPi7ykw1PW7zAPL4MlonEVz+QXOSx6eyhimp1VZC11SCg==
-----END CERTIFICATE-----
subject=CN = SnakeOil
issuer=CN = SnakeOil
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 2103 bytes and written 373 bytes
Verification error: self-signed certificate
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 4096 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 18 (self-signed certificate)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 64A28267134FB2869FA8A5863C334B0405B7AE7BF986FC82F7D39A7E241DEB9D
    Session-ID-ctx:
    Resumption PSK: 7D529CD5D0BDC65E7F23CCC5A8A349B5726097A0D59E3A114462918629A81EBEFB5CEF8B8D79FD02B26BE186CECE5250
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - 43 87 d0 c4 a5 49 95 26-c8 3e eb 08 d7 47 78 ca   C....I.&.>...Gx.
    0010 - f1 ef c9 d6 d2 c7 81 90-7d 03 44 d6 67 c2 f1 2a   ........}.D.g..*
    0020 - c6 a4 e8 0a 55 75 f3 fe-5d ca b8 24 8a 81 9b 4f   ....Uu..]..$...O
    0030 - 2c c8 d0 27 98 90 ca 78-83 30 2f f7 fa 08 ce 70   ,..'...x.0/....p
    0040 - 1e e1 d1 ee 1f f6 e1 c0-ab 07 63 be b0 09 a1 ac   ..........c.....
    0050 - de 1a b0 47 eb 79 40 85-ed e7 71 fb 10 30 cf 7a   ...G.y@...q..0.z
    0060 - 51 fc d8 f5 7e 0f 79 28-bb 5e c9 57 67 77 c5 b6   Q...~.y(.^.Wgw..
    0070 - df b0 e0 87 0f 4f 56 18-6c 09 6f 89 79 a7 ae 59   .....OV.l.o.y..Y
    0080 - e8 ee 18 aa 48 6c 56 2e-3c 6e bf 40 9e 38 2f c8   ....HlV.<n.@.8/.
    0090 - f0 9c f7 49 de d1 56 54-e5 2f ac f1 49 2f a4 8f   ...I..VT./..I/..
    00a0 - dd 05 1b 6d a9 8d 06 2e-b9 92 a2 19 aa 61 ee 69   ...m.........a.i
    00b0 - fd 62 f9 d4 88 d4 74 4d-8d 3b a5 85 1a 50 33 fc   .b....tM.;...P3.
    00c0 - 4e b1 1f e2 12 c9 32 43-c2 92 28 c2 78 d9 b1 42   N.....2C..(.x..B
    00d0 - e4 da 28 02 b6 c2 a2 6d-f2 a9 48 53 15 fa 1f f4   ..(....m..HS....

    Start Time: 1724949816
    Timeout   : 7200 (sec)
    Verify return code: 18 (self-signed certificate)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: F69E338A35E67ACE6B1CF87A0C0DD997076FDAED1D496A32A95BDE4BE941E7A6
    Session-ID-ctx:
    Resumption PSK: 89971F9592E7D722488245993D98907BA10BBF83F0A71D9A06C741432A4D3B51CF41566D7F4FD11B8BD388262EF28BD9
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - 43 87 d0 c4 a5 49 95 26-c8 3e eb 08 d7 47 78 ca   C....I.&.>...Gx.
    0010 - 1b d3 44 de 1f 3f 37 91-52 38 7c 07 4c 9a 89 e4   ..D..?7.R8|.L...
    0020 - 6d 7e 8d 5c 3d fb 05 da-8f 79 2f 76 12 ac 40 48   m~.\=....y/v..@H
    0030 - 78 59 5a 9b 9d 25 e8 71-4a bd 3a 5c d6 0e 2f 4f   xYZ..%.qJ.:\../O
    0040 - da 6c 08 93 4e 3b 9d fc-fe f0 9f b3 8c 4d 6f a5   .l..N;.......Mo.
    0050 - 73 24 5f 4b 83 c0 9d c1-c4 62 9b 85 7a 70 68 16   s$_K.....b..zph.
    0060 - d4 c2 70 44 aa c7 b1 ff-81 f7 11 dc 9f 4c 1e 76   ..pD.........L.v
    0070 - 88 06 09 9e 7d 1b 12 36-7a ee e6 1b db ae fb 54   ....}..6z......T
    0080 - 9f b1 ad c7 b6 6d 7d 5c-f3 5e 79 fd a6 a9 6e 2d   .....m}\.^y...n-
    0090 - 00 0d 0a 41 ce 6c d2 45-6a 2d 92 6d e2 c5 ab 3d   ...A.l.Ej-.m...=
    00a0 - 4b ed 3e 4e e7 32 1e ce-01 7c 68 4f b2 41 86 13   K.>N.2...|hO.A..
    00b0 - b7 ec f2 0e bf 07 60 88-56 fb ac d5 91 c4 05 13   ......`.V.......
    00c0 - 11 51 93 ba 39 cf 4f df-68 b2 26 08 3c 36 9d ad   .Q..9.O.h.&.<6..
    00d0 - 21 10 89 a0 cb 7c d1 b5-a5 7f 4d d6 7f e6 7d f5   !....|....M...}.

    Start Time: 1724949816
    Timeout   : 7200 (sec)
    Verify return code: 18 (self-signed certificate)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
Correct!
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

closed
bandit15@bandit:~$

```

## Notas adicionales

Una vez conectado, debo enviar la contraseña actual al puerto 30001 en localhost utilizando SSL/TLS. Para hacer esto, utilizo el comando openssl, que permite establecer una conexión segura. Despues enviamos la password de este nivel para que de la del bandit16.
## Referencias 
https://www.busindre.com/comandos_openssl_utiles_para_certificados