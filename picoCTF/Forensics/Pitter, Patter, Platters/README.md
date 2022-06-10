# Pitter, Patter, Platters!
Category: Forensics </br>
AUTHOR: th3_bl1nd3r

## Description
'Suspicious' is written all over this disk image. Download [suspicious.dd.sda1](https://jupiter.challenges.picoctf.org/static/47f3cb40aed42fbd74fd644e11d08007/suspicious.dd.sda1)</br>
## Solution
Use [Autospy](https://www.autopsy.com/) and you will get this
![Autospy GUI](https://github.com/GiaNghia056/CTF-Writeups/blob/main/picoCTF/Forensics/Pitter%2C%20Patter%2C%20Platters/Screenshot1.png)
Use srch_strings
```
srch_strings dds1-alpine.flag.img | grep picoCTF
```
Then, I got this
`  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_ad5c96c0}`</br>

Flag:`picoCTF{f0r3ns1c4t0r_n30phyt3_ad5c96c0}`