[ [Engligh](README.md) | [日本語](README_ja.md) ]

---

# PC1245-Catch The Pac!

<img src="./images/CatchThePac.png">

## Overview

This is a program for the “PC-1245” pocket computer, released by Sharp in Japan in 1983. <br>
It consists of BASIC and machine code. <br>

<br>

## How to Play

- The goal of this game is to control a monster and catch Pac-Man.
- The screen contains dots and power pellets. Pac-Man moves slowly where there are dots and quickly where there aren’t. The monster, on the other hand, moves quickly where there are dots and slowly where there aren’t.
- The left and right sides of the screen are warp tunnels that transport you to the opposite side.
- When a monster catches Pac-Man, Pac-Man is eliminated and the next Pac-Man appears.
- When Pac-Man eats a Power Pellet, the monsters become sluggish for a certain amount of time. If Pac-Man is caught by a monster during this time, it’s game over. Pac-Man moves faster at all times after eating a Power Pellet.

<br>

## Controls

- [4][6] : Move the Monster

<br>

## Loading to the real machine

Connect the cassette interface to the Pocket Computer, then connect it to the PC's headphone jack. <br>
On the Pocket Computer, use the following command to enter machine language program loading mode. <br>

```
CLOADM &C500
```

You can load the program by playing the following WAV file on your PC. <br>

```
/wav/CatchThePac-bin-C500.wav
```

Next, use the following command on the pocket computer to enter BASIC program load mode. <br>

```
CLOAD
```

You can load the program by playing the following WAV file on your PC. <br>

```
/wav/CatchThePac-bas.wav
```

<br>

## Play on PokecomGo

Please transfer the following two files to your smartphone and load them into the app.

```
/src/CatchThePac.bas
/dist/CatchThePac.bin
```

> If you name the .bin file `CatchThePac-C500.bin`, the start address will be set automatically when it is loaded.

<br>

## Play on PC-1251 Emulator

Copy the following file to the `~/.pc1251/programs` directory.

```
/src/CatchThePac.bas
/dist/CatchThePac.bin
```

Add the following line to the top of `/src/CatchThePac.bas`.

```
# bin: CatchThePac.bin &C500
```

Start the PC-1251 Emulator, and it will run when you select it with [Ctrl]+[O].

<br>

## Author

Hitoshi Iwai (aburi6800)

<br>

## Update History

October 21, 2026, ver. 0.50
- Beta release

<br>

## Licence

MIT Licence

<br>

## Thanks

- [SC61860 Asembler YASM61860](https://www.oit.ac.jp/labs/rd/rssrv/kobayashi-lab/~yagshi/old_web/misc/pocketcom/yasm.html)
- [Pocket Tools](http://pocket.free.fr/html/soft/pocket-tools_e.html)
- [Genymotion](https://www.genymotion.com/)
- [Pokecom Go](https://digihori.jimdofree.com/index/emulator/)
- [PC-1251 Emulator](https://github.com/woriguchi/pc1251-emulator/tree/main)
