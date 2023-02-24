---
layout: post
title: "PapibotPi, to quote or not to quote"
category: [code, python, mysql]
---

> **PapibotPi** was designed to made me learn both Python and MySQL, two things I did not master back in 2018. That's for the why.
> Back in a time when **Twitter API** was **free**, we could create bot to post **140 character** long tweet. [**Papibot Revillon**](https://twitter.com/papibotrevillon) was one of them, quoting **thoughts** and **reflections** from French chocolates called "**papillotes**", only sold during **Christmas time**. The archived code is stored [here](https://github.com/mtouzot/PapibotPi)!

<center>
  <figure>
    <img height="500" src="https://upload.wikimedia.org/wikipedia/commons/4/4a/Papillotes_de_Lyon.JPG" alt="Papillotes from Lyon">
    <figcaption>Papillotes from Lyon</figcaption>
  </figure>
</center>

# Introduction

Back in 2018, I was in **Clermont-Ferrand** spending time at the **[ACoLab](https://acolab.fr/)**, the city's [FabLab](https://www.wikiwand.com/en/Fab%20lab), learning plenty of new stuffs as laser cutting, 3D printing or coding. One member had developed a Twitter bot to inform members or future newcomers of the opening and closing hours or news about Arduino initiation workshops.

With Christmas approaching, I convinced myself to try program such a bot with quotes we can find in French chocolates called papillotes.

<center>
  <blockquote class="twitter-tweet"><p lang="fr" dir="ltr">Antoine de Saint-Exupéry ( 1900 - 1944 )<br>&quot;Faites que le rêve dévore votre vie afin que la vie ne dévore pas votre rêve.&quot;</p>&mdash; Papibot Révillon (@PapibotRevillon) <a href="https://twitter.com/PapibotRevillon/status/1217340673516625920?ref_src=twsrc%5Etfw">January 15, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
</center>

# Setup :computer:

The software can be found in my **[PapibotPi](https://github.com/mtouzot/PapibotPi)** repository. Once connected to **[Papibot Revillon](https://twitter.com/papibotrevillon)** account thanks the **Twitter API**, it's basically a **Python** program searching a single quote for an author in a **MySQL** database then publishing it on Twitter.

This was running on a desktop-less **[Raspberry Pi Zero](https://www.raspberrypi.com/products/raspberry-pi-zero/)** connected to Internet and a cron task ask the program to be run three times a day.

<center>
  <figure>
    <img height="300" src="https://images.prismic.io/rpf-products/e60c1946-a745-4dbc-8c0e-238d7094a3ec_Pi%20ZERO%20Angle%202.jpg?ixlib=gatsbyFP&auto=compress%2Cformat&fit=max&w=600&h=400" alt="Raspberry Pi Zero">
    <figcaption>Raspberry Pi Zero</figcaption>
  </figure>
</center>

# Overview and future of the project

There may be **errors** in the code, the software solutions I chose may not have been the best. Was MySQL a good idea? Has the database management been well thought out ? But the first purpose of this project was to known if I was able to do so. I consider this project as a personnal state of the art, a draft to be worked on. However...

Back in **Febuary 2023**, with the acquisition of the social media by **Elon Musk** months before, some changes came. Among them, the addition of a **paywall** to the Twitter API.

<center>
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Starting February 9, we will no longer support free access to the Twitter API, both v2 and v1.1. A paid basic tier will be available instead 🧵</p>&mdash; Twitter Dev (@TwitterDev) <a href="https://twitter.com/TwitterDev/status/1621026986784337922?ref_src=twsrc%5Etfw">February 2, 2023</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
</center>

As I write this blog post, I don't know how this project will evolve. The GitHub repo is an archive in read-only . The Twitter account is dead and don't tweet anymore.

_**PapibotRevillon** is dead, long live **PapibotRevillon**_.
