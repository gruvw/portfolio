---
layout: post
title: "AI in video games"
sub_title: "My first artificial intelligence project involving artificial neural networks: computer learns how to play Snake."
introduction: "You can access the files and the videos regarding this project on the following GitHub repository:"
actions:
  - label: "Project's GitHub repository"
    icon: github
    url: "https://github.com/gruvw/TM-AI-video-games"
image: "/assets/images/posts/ai_in_video_games/main.jpg"
tags:
  - Python
---

I programmed a computer to learn how to play the game Snake on its own.

## ⭐ A High-School Project

In my high school, I needed to create a graded project that I would submitted during my last year. We could choose any project we wanted but I already knew that I wanted something related to programming.
I was watching the videos of a youtuber called [CodeBullet](https://www.youtube.com/channel/UC0e3QhIYukixgh5VVpKHH9Q){:target="_blank"}. He is programming small artificial intelligence projects and that inspired me to program something similar for my project.

## 📝 The Concept

I decided to recreate two programs that CodeBullet did on his channel:

1. The first program that I coded was a way for me to get in touch with machine learning. The purpose is simple: you have a population of dots that need to find a way to reach a target located behind an obstacle. In the beginning the dots don't know anything about their environnement so they move randomly. I wanted the dots to find a way to go around the obstacle and reach the goal. In order to achieve that, I used a genetic algorithm with natural selection.
2. The second program is the more important one. I wanted to make a computer learn by itself how to play the famous game [Snake](https://en.wikipedia.org/wiki/Snake_(video_game_genre)){:target="_blank"}. I did this by using artificial neural networks combined with a more advanced genetic algorithm (than the one in my first program) and natural selection.

I will not detail everything in this article because I already wrote a whole document (the one I needed to write in order to submit my project for school) explaining everything about how I did it.

## 📃 Full Document

If you find this project interesting, I highly encourage you to read this document that I wrote about it.
I didn't want to write everything again here because there is too much for a web page and because I already wrote a clean document that explains the whole project in detail.
It contains **everything**, from the creation to the machine learning algorithm and the maths. It is written in french because I wrote it for school but there are many illustrations and code fences.

<!-- > <embed src="https://drive.google.com/viewerng/viewer?embedded=true&url=https://github.com/gruvw/TM-AI-video-games/raw/main/TM_Jung_Lucas_3M6.pdf" width="500" height="375"> -->

> [Full document (web viewer)](https://drive.google.com/file/d/18cwXNYcJRHXCFUsAlBJro7pRDsxV4ysZ/preview){:target="_blank"} _reload the page if needed_  
> [Full document (github)](https://github.com/gruvw/TM-AI-video-games/blob/main/TM_Jung_Lucas_3M6.pdf){:target="_blank"}

The pdf is written in [LaTeX](https://www.latex-project.org/){:target="_blank"} which is a programming language that is used to write documents (like Microsoft Office word).
As I knew nothing about LaTeX before writing this document, a part of my project was to learn how to code in that language.
It was pretty hard when I began but I got used to it and I can write in LaTeX now.
I am happy to have learned it because it is a very useful language that I will definitely use again when writing professional looking documents integrating maths and code.

## 📽️ The Result

There are three videos below that show the results that I achieved.

### Dots AI

This is a video of my first program in action. It shows the dots learning how to get around an obstacle:

<div class="video-responsive">
<iframe src="https://www.youtube-nocookie.com/embed/-AbSTfHwl3o?rel=0" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

This video shows the learning of the dots.
In the beginning they don't know where to go and they explore the word randomly.
As the number of generations and iterations increases, some of the dots will succeed more than others.
The genetic algorithm selects the ones that did a better job based on a fitness function.
That way, in the end we can see that they managed to achieve their goal with a low number of steps.

In the top left corner of the screen there are two informations displayed:

1. Gen: the number of generations
2. Steps: the number of steps that the best dot did from the spawn point to the goal

We can easily see that as the number of generations increases, the number of steps reduces. They learn how to get to the goal faster and faster.

### Snake AI

The two following videos are about my second program.

#### Snake learning

This video shows the computer learning how to play Snake:

<div class="video-responsive">
<iframe src="https://www.youtube-nocookie.com/embed/QtNxrumyY-E?rel=0" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

As you can see, it takes more time to learn how to play snake well than how to get around an obstacle.
In this video, I don't display the whole population of snakes learning at the same time (like with the dots) because they would take the whole window and we would not be able to see what is going on.
Instead, I only display the game of the best snake for each generation.
We can see the computer trying to learn what makes him lose and adjust his model.

There are 4 informations displayed at the bottom of the screen:

1. Gen: the number of generations.
2. Max steps: The maximum amount of steps allowed to the snakes of the current generation. This pushes the snakes to have a good score in few steps. It increases as the snakes get better.
3. Score: the number of fruits eaten by the best snake.
4. KB: means Killed By. Indicates what killed the snake. It could either be the wall, its tail or the maximum number of steps allowed.

These informations help to understand the evolution of the computer a little bit better.

#### Snake score 81

This is a video of a game of Snake played by the computer after about 700 generations:

<div class="video-responsive">
<iframe src="https://www.youtube-nocookie.com/embed/mH_wvQgb-_o?rel=0" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

At this point we can see that the computer has really understood the rules of the game and is limited by its vision (see the [Full document](#-full-document)).
It is even able to dodge its tail multiple times!

There are 3 informations displayed at the bottom of the screen:

1. Max steps: the maximum amount of steps allowed to the snake.
2. Score: the number of fruits eaten.
3. KB: means Killed By. Indicates what killed the snake. It could either be the wall, its tail or the maximum number of steps allowed.

It is really interesting to watch the snake forced to hit the wall because it got stuck by its tail. It could not avoid that due to the limitation of its vision (see the [Full document](#-full-document)).

## ✅ Conclusion

I am very happy about this project.
It is one of the most technical projects I have done so far and I am proud of myself for managing to achieve something like this considering I was only 17 at the time.
I finished my project by giving a live presentation in front of my teacher, an expert along with a small public of interested people (mostly my friends that were here to encourage me ^^).
I finally received the highest grade possible.
I read and learned so much about AI, machine learning and genetic algorithms by doing this project and that is probably why I am most happy to have done it.
I highly encourage you to take a look at the [full document](#-full-document) that I have written about it if you want to further understand theses programs.
