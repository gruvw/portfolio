---
layout: post
title: "Designing my own watch face"
sub_title: "How I designed and created my own smart watch home screen."
introduction: "You can access the source files regarding the watch face on the following GitHub repository:"
actions:
  - label: "Project's GitHub repository"
    icon: github
    url: "https://github.com/gruvw/rainbow-watch-face"
image: "/assets/images/posts/own_smart_watch_home_screen/main.jpg"
tags:
  - Side Project
---

I designed my own smart watch home screen and customized it the way I wanted it to be.

## 💎 The envy

I just bought the [Xiaomi Band 4](https://www.mi.com/en/mi-smart-band-4/) which was the very new smart watch model from Xiaomi at the time. As I already had bought the Xiaomi Band 2 and I was really happy about it, I already knew that I would not be disappointed by the new one.

Anyway, I received the watch and I liked it a lot. There was a hole community around this watch because with this model, you could customize the home screen the way you want. As some design were very cool, I downloaded some and tried them on my band. I downloaded many of them and that inspired me to do create my very own watch face design. I thought that if so many people can create these designs, why not me?

## 🛠 The Creation

### How to do it

I never did this kind of things before so I absolutely did not know where to start. So I did what everyone else would do: Google it. I did some quick research and I found [this tutorial](https://c.mi.com/thread-2281025-1-0.html) posted on the Xiaomi forum. It described well what I wanted to do and seems pretty easy.

What you need to do in order to create a watch face is to split your design idea in very small pieces (Every numbers, every logos, etc). After that, you need to save all the images you have designed in the same folder and rename it with a number (first image 0, second image 2, ...).

Once you did that, there is a program to download which will convert everything into a single .bin file. Then you can upload this .bin file to your watch and you are done.

### Design

For me, this project was more about image design than about actual coding.
Even if there is a bit of [json](https://fr.wikipedia.org/wiki/JavaScript_Object_Notation) file, everything else is just image editing.

I wanted to use the wellknown Adobe PhotoShop editor but it was too expensive for my simple use so it looked for an alternative.
After some quick researches, I found [Paint.NET](https://www.getpaint.net/): a very easy to use, PhotoShop like image editor. It was fine for what I wanted to do.

This is where I started to design my different elements. I started with the numbers (big and small ones). I drew then pixel by pixel but as the screen of the band is small, it did not took that long.
Once I finished with the numbers, I started to design the background. I wanted something colorful and funny so this is what I tried to achieve.
After that, I designed the daily steps goal progress bar. Unfortunately we cannot see it in action in the generated images (white jauge filled with black) but as you get closer to your daily steps goal, the bar is filling itself with some blue to green gradient.
I finished the designing part with the small icons (lock, bluetooth, ...) that I wanted as simple as possible.

### Export

Formatting and telling the program what were my images using json, Using the .exe program to generate the .bin (and the images ?)

### How it looks

like that

![Watch face animated gif](https://raw.githubusercontent.com/gruvw/rainbow-watch-face/master/Gruvw_en_wf_packed_animated.gif)

## 🚀 Publication

named it «Gruvw Rainbow», published my face where I found the one I tried in the beginning, <https://amazfitwatchfaces.com/mi-band-4/view/3018>, > 800 views and > 280 downloads, very happy about it, bit wired thinking someone could be looking to his watch with my face on it right now

## 📄 Conclusion

Satisfied about what I have done, not a big project, side project, still about one full time weekend xD, not wearing my mi band anymore but still happy to learned a way to customise a watch face, more design thant coding, still interesting tho
