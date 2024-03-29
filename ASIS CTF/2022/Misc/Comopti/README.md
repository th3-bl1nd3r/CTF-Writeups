# Comopti

## Description

We think they have used probabilistic graphical model to store the [comopti secret](https://asisctf.com/tasks/comopti_6c212baf35bf11edf5f43d3423a43fae9f3e6bda.txz). Can you find these magics and reveal the secret?

## Approach

- We have a `.raw` file so I opened it in [Autopsy](https://www.autopsy.com/) and we have something like this
![](Autopsy.png)
- There are 2 files with name "Papyri_Graecae_Magicae.pgm" or "Papyri_Graecae_Magicae.pgmb". I searched [`.pgm` file](https://netpbm.sourceforge.net/doc/pgm.html#format) on Google and I have some useful information.
- I am aware that An plain PGM file may contain images.
![](Pgmformat.png)
- I extracted the `Unalloc_1_0_51380223` file and open it in [Notepad++](https://notepad-plus-plus.org/). Zoomed it out and here is what I get
![](Notepad++View.png)
```
U2FsdGVkX18y5s1EWrMZLZCHf0BG5B2hjY9iazGPRGliZkEMIMjRG7dniuNp896aMVp/rUwi1vDc1U/lWdoCWQ==
Here is your key : "3b3gOa7RaVHPTmwKfLz"
Decryption : openssl aes-256-cbc -pbkdf2 -a -d -salt -k
```
- Just typed it all to the Terminal and we got the flag
![](Terminal.png)

Flag : `ASIS{pgm_1M4gE_f0Rma7_ManUpL4T!On!}`