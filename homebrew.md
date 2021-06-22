{% include navigation.html %}

# GBA Homebrew Development

## Engine

### GBALVNS

![GitHub](https://img.shields.io/github/license/laqieer/gbalvns)

GBALVNS is a Visual Novel / AVG / ADV / Galgame engine on Game Boy Advance.

![](https://media.discordapp.net/attachments/682141375587680274/820353613573652481/summer-2.png)![](https://media.discordapp.net/attachments/682141375587680274/820353609774530580/summer-0.png)![](https://media.discordapp.net/attachments/682141375587680274/820353612844498994/summer-1.png)![](https://media.discordapp.net/attachments/682141375587680274/820353615485992960/summer-3.png)![](https://media.discordapp.net/attachments/682141375587680274/820558326080339988/summer-1.png)![](https://media.discordapp.net/attachments/682141375587680274/820558322981404692/summer-0.png)

[Demo](https://github.com/laqieer/gbalvns/releases/latest){: .btn} | [Source Code](https://github.com/laqieer/gbalvns){: .btn}

### SS6PlayerForGBA

![GitHub](https://img.shields.io/github/license/laqieer/SS6PlayerForGBA)

SS6PlayerForGBA is a 2D skeletal animation engine on Game Boy Advance. It works with [OPTPiX SpriteStudio 6](http://www.webtech.co.jp/eng/spritestudio/).

![](https://media.discordapp.net/attachments/682141375587680274/840278168560467988/character_sample1-0.png)![](https://media.discordapp.net/attachments/682141375587680274/840278166294888459/character_sample1-1.png)

[Demo](https://github.com/laqieer/SS6PlayerForGBA/releases/latest){: .btn} | [Source Code](https://github.com/laqieer/SS6PlayerForGBA){: .btn}

## Library

### libgbabackup

![GitHub](https://img.shields.io/github/license/laqieer/libgbabackup)

libgbabackup is a library to access backup media on Game Boy Advance. It supports all save types and works with flashcarts and emulators.

|Devices|EZ-FLASH OMEGA|EverDrive-GBA X5|SuperCard MINI SD|mGBA|visualboyadvance-m|NO$GBA|VisualBoyAdvance|
|---|---|---|---|---|---|---|---|
|sram|✅|✅|✅|✅|✅|✅|✅|
|sram(fast)|✅|✅|✅|✅|✅|✅|✅|
|flash(512k)|✅|✅|❌|✅|✅|✅|✅|
|flash(1m)|✅|✅|❌|✅|✅|✅|✅|
|eeprom(4k)|✅|✅|❌|✅|✅|✅|✅|
|eeprom(64k)|✅|❌|❌|✅|❌|✅|✅|

[Download](https://github.com/laqieer/libgbabackup/releases/latest){: .btn} | [Source Code](https://github.com/laqieer/libgbabackup){: .btn}

### libsysgba

![GitHub](https://img.shields.io/github/license/laqieer/libsysgba)

libsysgba is a library to implement standard system calls to support C/C++ standard library functions such as file I/O and fstream.

```C
int fd = open("xxx.txt", O_RDONLY);
read(fd, dest, size);
```
```C
int i, j;
FILE *fp = fopen("xxx.txt", "r");
fscanf(fp, "%d %d", &i, &j);
```
```C++
std::ifstream fs("xxx.txt");
std::stringstream ss;
ss << fs.rdbuf();
```

[Download](https://github.com/laqieer/libsysgba/releases/latest){: .btn} | [Source Code](https://github.com/laqieer/libsysgba){: .btn}

## Kernel

### omega-kernel

![GitHub](https://img.shields.io/github/license/laqieer/omega-kernel)

omega-kernel is a custom EZ-FLASH OMEGA Kernel with new features such as running [ELF](https://en.wikipedia.org/wiki/Executable_and_Linkable_Format) and debug print.

[Download](https://github.com/laqieer/omega-kernel/releases/latest){: .btn} | [Source Code](https://github.com/laqieer/omega-kernel){: .btn}

## Toolchain

### build-your-own-gba-toolchain

![GitHub](https://img.shields.io/github/license/laqieer/build-your-own-gba-toolchain)

🤓 Build your own toolchain for GBA homebrew development!

[Download](https://github.com/laqieer/build-your-own-gba-toolchain/releases/latest){: .btn} | [Source Code](https://github.com/laqieer/build-your-own-gba-toolchain){: .btn}
