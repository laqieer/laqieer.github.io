{% include navigation.html %}

# GBA Homebrew Development

## Game

### Piano on GBA

Piano on GBA is a piano emulator on Game Boy Advance.

![](https://github.com/laqieer/piano-on-GBA/raw/main/logo.png)![](https://github.com/laqieer/piano-on-GBA/raw/main/graphics/keyboard_61.png)

[Demo](https://github.com/laqieer/piano-on-GBA/releases/latest){: .btn} | [Source Code](https://github.com/laqieer/piano-on-GBA){: .btn}

## Engine

### GBALVNS

![GitHub](https://img.shields.io/github/license/laqieer/gbalvns)

GBALVNS is a Visual Novel / AVG / ADV / Galgame engine on Game Boy Advance.

![](https://user-images.githubusercontent.com/8841957/185962493-bed92953-1d01-4a38-9be2-50333a5123ab.png)![](https://user-images.githubusercontent.com/8841957/185962498-8d2f0b4f-6571-4fc3-9dcc-15ec573b4934.png)![](https://user-images.githubusercontent.com/8841957/185962500-e2cd89bd-8dd3-4eef-82dc-c3b00a7e701f.png)![](https://user-images.githubusercontent.com/8841957/185962501-b465de1c-11c8-418e-91a5-37847e6193dd.png)![](https://user-images.githubusercontent.com/8841957/185962503-53b15280-12da-46c6-9dd2-4f0cfef7b1b3.png)![](https://user-images.githubusercontent.com/8841957/185962509-4350b9be-4f07-4d39-ae42-454ceff77712.png)

[Demo](https://github.com/laqieer/gbalvns/releases/latest){: .btn} | [Source Code](https://github.com/laqieer/gbalvns){: .btn}

### SS6PlayerForGBA

![GitHub](https://img.shields.io/github/license/laqieer/SS6PlayerForGBA)

SS6PlayerForGBA is a 2D skeletal animation engine on Game Boy Advance. It works with [OPTPiX SpriteStudio 6](http://www.webtech.co.jp/eng/spritestudio/).

![](https://user-images.githubusercontent.com/8841957/185961538-3a157c70-ae67-49fe-bc97-9356f7faac1c.gif)![](https://user-images.githubusercontent.com/8841957/185961567-89fa8cfc-2e41-43b1-8ad6-374dc6580cef.gif)

[Demo](https://github.com/laqieer/SS6PlayerForGBA/releases/latest){: .btn} | [Source Code](https://github.com/laqieer/SS6PlayerForGBA){: .btn}

## Library

### libsavgba

![GitHub](https://img.shields.io/github/license/laqieer/libsavgba)

libsavgba is a library to access backup media on Game Boy Advance. It supports all save types and works with flashcarts and emulators.

|Save Type|SRAM|EEPROM(512B)|EEPROM(8KB)|Flash(64KB)|Flash(128KB)|
|---|---|---|---|---|---|
|![](https://upload.wikimedia.org/wikipedia/commons/thumb/8/88/Gba-cartridge.png/64px-Gba-cartridge.png)**Flashcarts**||||||
|[EZ-FLASH OMEGA](https://www.ezflash.cn/product/omega/)|✔|✔|✔|✔|✔|
|[EverDrive-GBA X5](https://krikzz.com/store/home/42-everdrive-gba-x5.html)|✔|✔|✘|✔|✔|
|[SuperCard MINI SD](http://chn.supercard.sc/manual/mini_sd.htm)|✔|✘|✘|✘|✘|
|![](https://icons.iconarchive.com/icons/custom-icon-design/flatastic-11/64/Application-icon.png)**Emulators**||||||
|[mGBA](https://mgba.io/)|✔|✔|✔|✔|✔|
|[VisualBoyAdvance-M](https://vba-m.com/)|✔|✔|✔|✔|✔|
|[NanoBoyAdvance](https://github.com/fleroviux/NanoBoyAdvance)|✔|✔|✔|✔|✔|
|[No$GBA](https://www.nogba.com/)|✔|✔|✔|✔|✔|
|[VisualBoyAdvance](http://www.emulator-zone.com/doc.php/gba/vboyadvance.html)|✔|✔|✔|✔|✔|

[Download](https://github.com/laqieer/libsavgba/releases/latest){: .btn} | [Documentation](https://laqieer.github.io/libsavgba/){: .btn} | [Source Code](https://github.com/laqieer/libsavgba){: .btn}

### libgbabackup

![GitHub](https://img.shields.io/github/license/laqieer/libgbabackup)

libgbabackup is a library to access backup media on Game Boy Advance. It supports all save types and works with flashcarts and emulators.

|Devices|EZ-FLASH OMEGA|EverDrive-GBA X5|SuperCard MINI SD|mGBA|visualboyadvance-m|NO$GBA|VisualBoyAdvance|NanoBoyAdvance|
|---|---|---|---|---|---|---|---|---|
|sram|✅|✅|✅|✅|✅|✅|✅|✅|
|sram(fast)|✅|✅|✅|✅|✅|✅|✅|✅|
|flash(512k)|✅|✅|❌|✅|✅|✅|✅|✅|
|flash(1m)|✅|✅|❌|✅|✅|✅|✅|✅|
|eeprom(4k)|✅|✅|❌|✅|✅|✅|✅|✅|
|eeprom(64k)|✅|❌|❌|✅|❌|✅|✅|✅|

[Download](https://github.com/laqieer/libgbabackup/releases/latest){: .btn} | [Source Code](https://github.com/laqieer/libgbabackup){: .btn}

### libsysgba

![GitHub](https://img.shields.io/github/license/laqieer/libsysgba)

libsysgba is a library to implement standard system calls to support C/C++ standard library functions such as file I/O and fstream. It can also access backup media as a file.

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
```C
int fd = open("sram:", O_RDWR);
int fd = open("eeprom:", O_RDWR);
```
```C
FILE *fp = fopen("sram:", "r+");
FILE *fp = fopen("eeprom:", "r+");
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

## Tool

### detect-save-type

![GitHub](https://img.shields.io/github/license/laqieer/libsavgba)

detect-save-type is a tool to detect backup media type.

![](https://media.discordapp.net/attachments/682141375587680274/861456724882882581/detect-save-type-0.png)![](https://media.discordapp.net/attachments/682141375587680274/861456723197689906/detect-save-type-1.png)![](https://media.discordapp.net/attachments/682141375587680274/861456721600184340/detect-save-type-2.png)![](https://media.discordapp.net/attachments/682141375587680274/861456720156033044/detect-save-type-3.png)

[Download](https://github.com/laqieer/libsavgba/releases/download/v3.2.0/detect-save-type.gba){: .btn} | [Source Code](https://github.com/laqieer/libsavgba/tree/main/test/detect-save-type){: .btn}

## Tutorial

### gba-dev-best-practice

gba-dev-best-practice is a series of videos to share best practice for GBA homebrew development.

<iframe src="//player.bilibili.com/player.html?aid=851094054&bvid=BV1UL4y1x7qc&cid=495873915&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

[Read](https://laqieer.gitbook.io/gba-dev-best-practice/){: .btn} | [Source Code](https://github.com/laqieer/gba-dev-best-practice){: .btn}

## Resource

### gba-free-fonts

gba-free-fonts is a series of easy-to-use free fonts for GBA homebrew development.

![](https://user-images.githubusercontent.com/8841957/153871980-5ab179f1-b13c-4c08-89cb-45e28936e4aa.png)![](https://user-images.githubusercontent.com/8841957/153871992-f420e32d-caa5-4802-9d17-4850b5fa20a9.png)![](https://user-images.githubusercontent.com/8841957/153871997-d65dd80c-1b46-455a-ade1-820a33b746e4.png)

[Download](https://github.com/laqieer/gba-free-fonts/releases/latest){: .btn} | [Repo](https://github.com/laqieer/gba-free-fonts){: .btn}
