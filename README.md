# Luma3DS playtime patch
Add a timer mechanism to Luma3DS for limit child's playtime powering off the console.

1) Download source code of Luma3DS-10.1.3 from internet:
```bash
:~# wget --output-document=Luma3DS-10.1.3.zip https://github.com/AuroraWright/Luma3DS/archive/v10.1.3.zip
```

2) Extract Luma3DS-10.1.3.zip
```bash
:~# unzip Luma3DS-10.1.3.zip && mv Luma3DS-10.1.3 Luma3DS
```

3) Apply patch to Luma3DS-10.1.3 original directory:
```bash
:~# patch -t -p0 < luma3ds_mod_offplay.patch
```

4) Built... boot.firm
Prerequisites for compile Luma3DS: (git, makerom in PATH, firmtool ,Up-to-date devkitARM+libctru)
```bash
:~# cd Luma3DS/ && make clean
:~# make
```

Now you have your modded and compiled Luma3DS/boot.firm to copy in the root of SD card.  
Power on 3DS with (select + Power) to set the playtime countdown in the menù.  
Use rosalina->miscelanous for disable timer in-game mode.

Testet with (old)3DS fimrware 11.3 and boot9strap 1.91.
