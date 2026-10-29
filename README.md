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
- There are dots on the screen. Pac-Man moves slowly where there are dots and quickly where there aren't. He is not affected by monster dots.
- The left and right sides of the screen are warp tunnels that take you to the opposite side. Note that you cannot change the direction in which monsters are moving at the entrance to a warp tunnel.
- The left and right sides of the screen are warp tunnels that take you to the opposite side.
- When a monster catches Pac-Man, Pac-Man is eliminated and a new Pac-Man appears. Additionally, the dots on the half of the screen opposite the monster’s position respawn, and a Power Pellet appears somewhere on the screen.
- When Pac-Man eats a Power Pellet, the monsters get sulky for a certain amount of time, slowing their movement speed, while Pac-Man moves faster. If a monster is caught by Pac-Man during this time, it’s game over.
- When Pac-Man eats all the dots on the screen, the game advances to the next level, which becomes slightly more difficult. Level 4 is the hardest, and the difficulty level remains similar to that of Levels 3 and 4 thereafter.
- Note that the game also ends if Pac-Man eats all the dots without being caught even once.

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

## Play on sc61box

Copy the following file to the `~/.sc61box/programs` directory.

```
/src/CatchThePac.bas
/dist/CatchThePac.bin
```

Add the following line to the top of `CatchThePac.bas`.

```
# bin: CatchThePac.bin &C500
```

Start the sc61box, and it will run when you select it with [Ctrl]+[O].

<br>

## Author

Hitoshi Iwai (aburi6800)

<br>

## Update History

October 24, 2026, ver. 1.00
- Initial release

<br>

## Licence

MIT Licence

<br>

## Thanks

- [SC61860 Asembler YASM61860](https://www.oit.ac.jp/labs/rd/rssrv/kobayashi-lab/~yagshi/old_web/misc/pocketcom/yasm.html)
- [Pocket Tools](http://pocket.free.fr/html/soft/pocket-tools_e.html)
- [Genymotion](https://www.genymotion.com/)
- [Pokecom Go](https://digihori.jimdofree.com/index/emulator/)
- [sc61box](https://github.com/woriguchi/sc61box)
