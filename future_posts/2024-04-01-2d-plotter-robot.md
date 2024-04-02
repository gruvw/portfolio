---
layout: post
title: "2D Plotter Robot"
sub_title: "Building a robot that can draw shapes on paper using a regular pen."
introduction: "You can access the source code and the documentation regarding this project on the following GitHub repository:"
actions:
  - label: "Project's GitHub repository"
    icon: github
    url: "https://github.com/gruvw/2d_plotter"
image: "/assets/images/posts/2d_plotter/main.png"
tags:
  - C
  - Hardware
toc: true
---

<style>
    .process {
        height: 250px;
        margin: 3px;
    }

    .draw {
        height: 170px;
        margin: 3px;
    }

    .images {
        margin: 5px;
    }
</style>

Most of the project is already explained on the [README](https://github.com/gruvw/2d_plotter){:target="_blank"} of the project on GitHub.

## 🧠 Concept

I took a course at EPFL that taught students about the two sides of building things: the hardware part and the integration with software.

During this course, I learned to use a laser cutting machine and 3D printers.
It was my first time doing [CAD](https://en.wikipedia.org/wiki/Computer-aided_design){:target="_blank"}, and the process was really amazing to go from an idea, design it, and have it printed over the course of only a few hours.

I build a 2D Plotter Robot: a device that can draw user defined drawings on a small sheet of paper based on a provided computer program.

## ⏳ Process

Here are a few pictures demonstrating the whole process of building this robot:

<div class="images">
    <img src="/assets/images/posts/2d_plotter/process/process_1.png" class="process">
    <img src="/assets/images/posts/2d_plotter/process/process_2.png" class="process">
    <img src="/assets/images/posts/2d_plotter/process/process_3.png" class="process">
    <img src="/assets/images/posts/2d_plotter/process/process_4.png" class="process">
    <img src="/assets/images/posts/2d_plotter/process/process_5.png" class="process">
    <img src="/assets/images/posts/2d_plotter/process/process_6.png" class="process">
    <img src="/assets/images/posts/2d_plotter/process/process_7.png" class="process">
</div>

I started by laser cutting all the parts for the core structure.
Then I assembled the robot and soldered the cables to the external alimentation.

I initially 3D printed a static pen holder and wrote the basis of the software to test every component and make sure the plotter was drawing precise shapes.
Later, I designed the dynamic pen holder that can lift the pen up and down in order to draw more complex shapes.
I went through about 4 or 5 design iterations before having a convincing piece that would not be imprecise when lifting the pen.

I also added limit switches to automatically set the "home"/origin position of the plotter.
Additionally, I connected a buzzer to the Arduino.
It gives a nice audio feedback to the person using the plotter about the current state of the procedure (started, ready to draw, finished).

### Turtle language

I implemented a turtle language interpreter/[REPL](https://en.wikipedia.org/wiki/Read–eval–print_loop){:target="_blank"} (Read Eval Print Loop) in C so that we can provide instructions to the plotter using this language.

**Note**: learn more about the turtle language here <https://turtleacademy.com/playground>{:target="_blank"}.

One can input turtle programs directly using the Arduino Serial Monitor.
No modifications have been made to the original syntax of the language.
It supports multi-lines input (with indentation) and it is not spacing dependent.

### Code

The code for the project was mostly written in **C** (a few `.cpp` and `.ino` were required to interact with the [Arduino](https://www.arduino.cc/){:target="_blank"} ecosystem).  
To add a bit more to the challenge, I also decided not to use any external libraries (except for the `Arduino.h`).
I wrote the code that manages the servo and the steppers from scratch (see `2d_plotter/src/hardware` for more information).

## 🏁 Result

Here are a few pictures showing the final plotter from different angles:

<div class="images">
    <img src="/assets/images/posts/2d_plotter/result/plotter_top.png" class="process">
    <img src="/assets/images/posts/2d_plotter/result/plotter_side.png" class="process">
    <img src="/assets/images/posts/2d_plotter/result/plotter_iso_front.png" class="process">
<div><br>

Here is a short video demonstrating the result:

<div class="video-responsive">
  <iframe src="https://www.youtube-nocookie.com/embed/-nplPBwFOKw" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

The quality of the video is not perfect, but we can see the plotter drawing a dotted line correctly.<br>

Here are a few pictures of example drawings that the robot made:

<div class="images">
    <img src="/assets/images/posts/2d_plotter/drawings/heart.png" class="draw">
    <img src="/assets/images/posts/2d_plotter/drawings/hilbert.png" class="draw">
    <img src="/assets/images/posts/2d_plotter/drawings/magic_s.png" class="draw">
    <img src="/assets/images/posts/2d_plotter/drawings/rose.png" class="draw">
    <img src="/assets/images/posts/2d_plotter/drawings/sun.png" class="draw">
</div>

I had a lot of fun building this robot and programming the software for it.
It was the first time I programmed an interpreter in C, but it was simpler than I originally thought.<br>
I ended up receiving the maximum grade for this project, so the teaching staff seemed to also agree that I managed to produce a great 2D plotter robot.
