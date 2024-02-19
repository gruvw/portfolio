---
layout: post
title: "Nintendo DS Wi-Fi Game"
sub_title: "Programming a Nintendo DS game and adding Wi-Fi cappabilities."
introduction: "You can access the source code and the documentation regarding this project on the following GitHub repository:"
actions:
  - label: "Project's GitHub repository"
    icon: github
    url: "https://github.com/gruvw/epfl-nds-game"
image: "/assets/images/posts/nds_wifi_game/main.png"
tags:
  - C
  - Hardware
toc: true
---

Programming a Nintendo DS game and adding Wi-Fi capabilities.

## 🧠 Concept

I took a course at EPFL that teached students on programming "microprogrammed embedded systems".
We used the [Nintendo DS](https://en.wikipedia.org/wiki/Nintendo_DS){:target="_blank"} Lite as the platform to practice and program what we learned.  
I decided to build a [Tic-Tac-Toe](https://en.wikipedia.org/wiki/Tic-tac-toe){:target="_blank"} clone on an Nintendo DS and later add Wi-Fi functionalities to enable two player games on two different devices.

**Note**: I strongly encourage you to look at the [GitHub repository](https://github.com/gruvw/epfl-nds-game){:target="_blank"} of the project if you are interested.
The README is very detailed and goes deep into the technicalities.

## 🏁 Result

Here is a short video demonstrating the resulting game:

<div class="video-responsive">
  <iframe src="https://www.youtube-nocookie.com/embed/PG9ud13ZhmE" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

The quality of the video is not perfect but we can see the game running correctly.  
I start by showcasing the game on a single device and then bring a second Nintendo DS and play using a Wi-Fi connection.

## 🛠️ Process



### Wi-Fi stack

<img src="https://github.com/gruvw/epfl-nds-game/blob/main/docs/P2P-BOP.png?raw=true" alt="P2P-BOP" width="600px">

<img src="https://github.com/gruvw/epfl-nds-game/blob/main/docs/Message_Queue_FSM.png?raw=true" alt="Message Queue FSM" width="700px">

## 📝 Conclusion
