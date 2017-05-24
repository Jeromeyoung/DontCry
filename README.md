# DontCry
## Introduction
This utility allows machines infected by the WannaCry ransomware to recover their files.

**DontCry** is based on [wanakiwi](https://github.com/gentilkiwi/wanakiwi/) which makes possible for lucky users to :
- Recover the private user key in memory to save it as `00000000.dky`
- Decrypt all of their files

The primes extraction method is based on Adrien Guinet's [wannakey](https://github.com/aguinet/wannakey) which consist of scanning the WannaCry process memory to recover the prime numbers that were not cleaned during CryptReleaseContext().

## Limitations of wanakiwi
Given the fact this method relies on scanning the address space of the process that generated those keys, this means that if this process had been killed by, for instance, a reboot - the original process memory will be lost. It is very important for users to *NOT* reboot their system before trying this tool.

Secondly, because of the same reason we do not know how long the prime numbers will be kept in the address space before being reused by the process. This is why it is important to try this utility ASAP.

This is not a perfect tool, but this has been so far the best solution for victims who had no backup.

## Compatibility

O.S.  | x86 | x64 |
------------- | ------------- | ------------- 
Windows XP  | :white_check_mark:  | ?
Windows 2003  | :white_check_mark:  | ?
Windows 7  | :white_check_mark:  | ? 

## Acknowledgement
This product includes software developed by the OpenSSL Project for use in the OpenSSL Toolkit (http://www.openssl.org/)

With BIG thanks and love to:
- @msuiche
- @halsten
- @malwareunicorn
- @adriengnt
- @dsahoo90
- @th3snehasish
- Niladri Bihari Mohanty
