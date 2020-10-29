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

## 💎 The Envy

I just bought the [Xiaomi Band 4](https://www.mi.com/en/mi-smart-band-4/){:target="_blank"} which was the very new smart watch model from Xiaomi at the time. As I already had bought the Xiaomi Band 2 and I was really happy about it, I already knew that I would not be disappointed by the new one.

Anyway, I received the watch and I liked it a lot. There was a hole community around this watch because with this model, you could customize the home screen the way you want. As some design were very cool, I downloaded some and tried them on my band. I downloaded many of them and that inspired me to do create my very own watch face design. I thought that if so many people can create these designs, why not me?

## 🛠 The Creation

### How to do it

I never did this kind of things before so I absolutely did not know where to start. So I did what everyone else would do: Google it. I did some quick research and I found [this tutorial](https://c.mi.com/thread-2281025-1-0.html){:target="_blank"} posted on the Xiaomi forum. It described well what I wanted to do and seems pretty easy.

What you need to do in order to create a watch face is to split your design idea in very small pieces (Every numbers, every logos, etc). After that, you need to save all the images you have designed in the same folder and rename it with a number (first image 0, second image 2, ...).

Once you did that, there is a program to download which will convert everything into a single .bin file. Then you can upload this .bin file to your watch and you are done.

### Design

For me, this project was more about image design than about actual coding.
Even if there is a bit of [json](https://fr.wikipedia.org/wiki/JavaScript_Object_Notation){:target="_blank"} file, everything else is just image editing.

I wanted to use the wellknown Adobe PhotoShop editor but it was too expensive for my simple use so it looked for an alternative.
After some quick researches, I found [Paint.NET](https://www.getpaint.net/){:target="_blank"}: a very easy to use, PhotoShop like image editor. It was fine for what I wanted to do.

This is where I started to design my different elements. I started with the numbers (big and small ones) and date. I drew then pixel by pixel but as the screen of the band is small, it did not took that long.
Once I finished with the numbers and date, I started to design the background. I wanted something colorful and funny so this is what I tried to achieve.
After that, I designed the daily steps goal progress bar. Unfortunately we cannot see it in action in the generated images (white jauge filled with black) but as you get closer to your daily steps goal, the bar is filling itself with some blue to green gradient.
I finished the designing part with the small icons (lock, bluetooth, ...) that I wanted as simple as possible.

### Export

At this point, I was pretty satisfied by the design. I renamed every images (there were 101 images) with a number going from 0 to 100.

I was now ready for writing the json file. This is just a file that will tell the program that "compiles" the watch face where each image is and what is its purpose.

This is an example taken from the json file:

{% highlight json linenos %}
"Background": {
  "Image": {
    "X": 0,
    "Y": 0,
    "ImageIndex": 0
  }
}
{% endhighlight %}

In the example, we can see that I indicate to the program that the background image has the Index (file name) 0 and that it need to be placed on the top left corner of the screen (x=0, y=0).

I did the exact same thing for each image (Image index and position). Hopefully you can sometime define the index by ranges: for example the numbers from 0 to 9 are indexes 59 to 68.

When I designed the different images, I also made some weather related ones (temperature, ...) but I finally decided not to put them into the watch face because it would make things too much close to each other and I preferred to have more room between each elements.

After that I filled the entier json file, I executed the program (AmazfitBipTools_Mi4_1.0.3) in charge to convert all my work into a .bin  file that can be read by my watch.

I highly encourage you to take a look into the (project's GitHub repository) if you are interested in learning more about the files I described.

### How it looks

This is a gif of the final result of my watch face:

![Watch face animated gif](https://raw.githubusercontent.com/gruvw/rainbow-watch-face/master/Gruvw_en_wf_packed_animated.gif)

It rotates between random hours and dates etc in order to show multiple configuration. The only problem in this gif is that the steps progress bar does not fill up and stays black.

## 🚀 Publication

Before publishing this watch face to make it available to anyone worldwide, I wanted to give it a simple name. I chose _Gruvw Rainbow_ because it has some kind of rainbow colors and I wanted my name in it.

I decided to publish my work on the same platform/site I was using in the beginning where I was downloading and testing watch faces done by other users: <https://amazfitwatchfaces.com/mi-band-4/view/3018>

It has (at the time I am writing this) over 800 views and over 280 downloads. I am very happy about that and it is pretty fun to think that someone could literally be looking at his watch right now and see the time on the watch face I designed.

## 📄 Conclusion

In the end, I am very satisfied about what I have done in this project. Even though it is not a project that took me weeks to realise (it took me about 3 days), I am still very happy to had learned a way to customize my smart watch. On top of that, it is very satisfying to look at my wrist and see the design I created.
