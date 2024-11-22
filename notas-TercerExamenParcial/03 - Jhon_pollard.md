# Retos PicoCTF


## Objetivo 

Sometimes RSA [certificates](https://jupiter.challenges.picoctf.org/static/c882787a19ed5d627eea50f318d87ac5/cert) are breakable
## Solución 

```
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/johnpollard]
└─$ ls
cert
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/johnpollard]
└─$ openssl x509 -pubkey -in cert -out cert.pub
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/johnpollard]
└─$ openssl rsa -pubin -in cert -text
Could not find private key of public key from cert
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/johnpollard]
└─$ openssl rsa -pubin -in cert.pub -text
Public-Key: (53 bit)
Modulus: 4966306421059967 (0x11a4d45212b17f)
Exponent: 65537 (0x10001)
writing RSA key
-----BEGIN PUBLIC KEY-----
MCIwDQYJKoZIhvcNAQEBBQADEQAwDgIHEaTUUhKxfwIDAQAB
-----END PUBLIC KEY-----
                                                                                                
┌──(kali㉿kali)-[~/picoCTF/retos/tercerparcial/johnpollard]
└─$ 


picoCTF{73176001,67867967}
```

## Notas adicionales 

## Referencias 
