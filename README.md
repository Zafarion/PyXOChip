# PyXOChip
An incomplete XO-Chip emulator

After I finished PySuperChip, I took a look at the XO-Chip documentation, decided to implement the Octo instructions and PyXoChip came up lol.
BUT... to implement the multi-plane scheme, I would have to completely change my current routine of XORing pixels in the Pygame Surface directly, so I stopped here. Because of this, the emulator remained monochromatic, but oddly enough, despite some graphical flaws, it ran some games made for XO-Chip! Especially if they don't depend too much on additional colors and don't make too many plane transitions. I included some of them in this repository.
I also didn't worked on the new audio extensions.

But in truth, the main the objective is to run games made for the S-Chip, because I noticed that several of them were made with the modern emulators in mind. I noticed that games developed for S-Chip like EATY and BINDING OF COSMAC require the emulator to run at much higher speeds to avoid flickering and to reach smooth gameplay. At least 256 instructions per frame in Eaty and between 768-1024 in Binding. Curiously, the original Chip8 on COSMAC VIP runs only 8-11 instructions per frame and on the more advanced HP calculators were supposed to run at 17 to 50 instructions per frame, depending on the model.

For these Octo-era games not run too fast, I think they were coded in a way that their speed were limited by the chip8 internal delay timer. Because these games calls the drawing instruction so many times a second, they don't flicker, so in PyXOChip I disabled the trick I had done in PySuperChip to avoid flickering, especially because it can cause graphical glitches (but rarely) in some older games (so you can use PYXOChip to run them). Then if you don't want to stop flickering, want to play old games at much higher speeds and prefer yellow, use this version for Chip8 and S-Chip games.

![](https://github.com/Zafarion/PyXOChip/blob/main/083e6ea6-e9d1-4da9-b474-1685e3fa5cb1.jpg)
![](https://github.com/Zafarion/PyXOChip/blob/main/a15a070a-fc02-4a1b-a207-527d6f4c7bd7.jpg)
![](https://github.com/Zafarion/PyXOChip/blob/main/34fd878d-3947-4d2b-b537-b28470a6c37d.jpg)
![](https://github.com/Zafarion/PyXOChip/blob/main/420a2c51-d5af-4652-9539-57dd9ccec190.jpg)
![](https://github.com/Zafarion/PyXOChip/blob/main/4c02e4be-1990-49c0-b0ec-eedc54aa2104.jpg)
![](https://github.com/Zafarion/PyXOChip/blob/main/bd5f6af8-bc60-41db-b490-baba0a96a669.jpg)
![](https://github.com/Zafarion/PyXOChip/blob/main/c9dc610a-895d-4de9-b58b-ef185a7f2fb9.jpg)
![](https://github.com/Zafarion/PyXOChip/blob/main/cb99ae87-9253-4f40-aaa0-c2839f11ae82.jpg)
