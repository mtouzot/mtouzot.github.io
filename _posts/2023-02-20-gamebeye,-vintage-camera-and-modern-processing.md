---
layout: post
title: "GameBEye, vintage camera and modern processing"
category: [code, python, image processing]
---

> **GameBEye** is a **Python library** to do some **image processing** with **Game Boy Camera** images.<br>
> The **goal** for me was to write **Python** code, to use its **scientific libraries** (mainly **numpy**), to build a **package**, to write **Sphinx** documentation, and to share it.<br>
> The **documentation page** can be found [here](https://mtouzot.github.io/GameBEye/)!


[![GitHub](https://img.shields.io/github/stars/mtouzot/GameBEye?label=Github&logo=github)](https://github.com/mtouzot/GameBEye)
[![License](https://img.shields.io/github/license/mtouzot/GameBEye)](https://github.com/mtouzot/GameBEye/blob/master/LICENSE)
[![Release](https://img.shields.io/github/v/release/mtouzot/GameBEye)](https://github.com/mtouzot/GameBEye/releases)
[![Issues](https://img.shields.io/github/issues/mtouzot/GameBEye)](https://github.com/mtouzot/GameBEye/issues)

# Introduction
In the late 80's, **Nintendo** release a new **handheld game console**, the first of a new family : the **GameBoy**. In the following decade, a couple of year before my tenth birthday, this **8-bit** console was mine with an [_**Asterix**_](https://en.wikipedia.org/wiki/Asterix_(1993_video_game)) video game to play...

<center>
  <figure>
    <img src="{{"/assets/img/posts/gbcam/asterix_cover.jpg" | relative_url}}" alt="Asterix game cover for GameBoy">
    <figcaption>Asterix game cover for GameBoy</figcaption>
  </figure>
</center>

The same year _Les Bleus_, the France national football team, won their first FIFA World Cup - i.e. 1998 - a **four-grayscaled** world was born with the **GameBoy Camera**. All in a resolution of **128 x 112 pixels** (_0.014 Megapixels_). Pretty impressive, right ?

<center>
  <figure>
    <img src="https://media.githubusercontent.com/media/mtouzot/GameBEye/master/docs/_static/gameBoyCamera.png" alt="GameBoy Camera image">
    <figcaption>GameBoy Camera image</figcaption>
  </figure>
</center>

# :baby: Birth of the project

Surfing on the web, searching for some new **DIY projects** to start, I found [**Furrtek**](https://github.com/furrtek/) Game Boy Camera [project](https://github.com/furrtek/GBCameraProjects) to transform Game Boy Camera into a DSLR or a webcam. However, I do not own his electronic skills... But i know how to code !

<p align="center">
<a href="https://www.youtube.com/watch?v=gOtaw834G0g">
  <img src="https://img.youtube.com/vi/gOtaw834G0g/hqdefault.jpg" alt="Furrtek's YouTube video for his GameBoy Camcorder project" />
  <br>Furrtek's YouTube video for his GameBoy Camcorder project
</a>
</p>

<center>
  <figure>
    <img src="https://raw.githubusercontent.com/furrtek/GBCameraProjects/master/GBLiveCam/photo.jpg" alt="Furrtek's GBLiveCam" width="150">
    <img src="https://raw.githubusercontent.com/furrtek/GBCameraProjects/master/GBLiveCam/video.gif" alt="Furrtek's GBLiveCam result">
    <figcaption>Furrtek's GBLiveCam</figcaption>
  </figure>
</center>

# Project's development

## 1. Goals :question:
This project aims to become **a Python library**. It'll purely be used as an **external package** to process Game Boy Camera images in **scripts** or in the Python **console**.

My main goal was and is still **to learn** and **improve** my knowledge in a **programming language** (here, Python) and **scientific libraries** (here, numpy and OpenCV), to try **GitHub CI** and to discover and learn stuff along the way. I also wanted to maintain the [project **documentation**](https://mtouzot.github.io/GameBEye/) as up to date as possible by add the maximum of docstrings in my files.

## 2. Setup :computer:

### 2.1 Transfering images from GameBoy Camera to a computer
The first pitfall to overcome could be downloading the photo from the GameBoy Camera. Fortunately, there are many ways to avoid these by paying a few bucks :
 * [GB Operator](https://www.epilogue.co/product/gb-operator) from **Epilogue** allows users to play (thru an emulator) and manage (save games) Game Boy cartridges on any Windows or Apple computer.

 <center>
   <figure>
     <img src="https://pic.clubic.com/v1/images/2064426/raw" width="250" alt="Game Boy Camera on a GB Operator from Epilogue">
     <figcaption>Game Boy Camera on a GB Operator from :copyright:Epilogue</figcaption>
   </figure>
 </center>

 * [GBxCart RW](https://shop.insidegadgets.com/product/gbxcart-rw/) from **insideGadgets** reads cartridges to save backups of your games, to push your own games into new ones and also to save Game Boy Camera photos.

 <center>
   <figure>
     <img src="https://shop.insidegadgets.com/wp-content/uploads/2018/05/IMG_6816S.jpg" width="250" alt="GBxCart RW - Gameboy/GBC/GBA Cart Reader, Writer & Flasher">
     <figcaption>GBxCart RW (Gameboy/GBC/GBA Cart Reader, Writer & Flasher) from insideGadgets</figcaption>
   </figure>
 </center>

 * Other DIY PCB projects you can find on GitHub, Hackaday,... or various maker websites.

### 2.2 Using GameBEye to play with original Game Boy Camera pictures

Once installed, you can start using the library to process your images using examples or make your own.

For the moment, it allows a few effects as changing image colors from Black & White to a color from a [predefine palette](https://mtouzot.github.io/GameBEye/GameBEye/gbcamcolors.html) as :

<center>
  <figure>
    <img src="https://media.githubusercontent.com/media/mtouzot/GameBEye/master/docs/_static/colorPalettes/CHIG.png" width="250" alt="CHIG color palette">
    <figcaption>CHIG color palette</figcaption>
  </figure>
  <figure>
    <img src="https://media.githubusercontent.com/media/mtouzot/GameBEye/master/docs/_static/colorPalettes/PPR.png" width="250" alt="PPR color palette">
    <figcaption>PPR color palette</figcaption>
  </figure>
  <figure>
    <img src="https://media.githubusercontent.com/media/mtouzot/GameBEye/master/docs/_static/colorPalettes/BANANA.png" width="250" alt="BANANA color palette">
    <figcaption>BANANA color palette</figcaption>
  </figure>
</center>

You can also add a thermal printed effect to display images like this :

<center>
  <figure>
    <img src="https://media.githubusercontent.com/media/mtouzot/GameBEye/master/docs/_static/printedGameBoyCamera.png" width="250" alt="Thermal printed image">
    <figcaption>Thermal printed image</figcaption>
  </figure>
</center>

## 3. :chart_with_upwards_trend: Project's evolution

Before using this project with an **graphical computer interface**, I would like to keep improving and adding software functionalities to this library :
* changing colors from grayscale values to a selection of RGB values,
* creating new display filters,
* changing the image size up (or down),
* colorizing the image with you own colors choice ([_maybe using a deep learning algorithm_](https://hackaday.com/2017/02/20/neural-nets-and-game-boy-cameras/)),
* creating a command line interface to process images in a terminal,
* adding ideas or features people may want,
* ...

# :memo: Documentation

You'll find more information on how to use **GameBEye** in the [documentation page](https://mtouzot.github.io/GameBEye/)

_Let's see the world in quadricolor!_
