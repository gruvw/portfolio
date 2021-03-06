---
layout: post
title: "Laser gun projected target"
sub_title: "A target projected on the wall that you can shoot on using a laser gun."
image: "/assets/images/posts/laser_gun_projected_target/main.jpg"
tags:
  - Python
toc: true
---

There is sadly no code that I will share for this project as I was payed to build the software.
I will however describe and explain my work as best as I can below.

## My First Coding Job

I already had a job planned for the summer 2020 but the COVID19 pandemic made it not happening finally.
I was left without anyway to work and gain money that summer till the day that I receive an email from a person.
It was in fact a friend of the teacher that was following me for my high school project [AI in video games](/2019/10/25/artificial-intelligence-in-video-games.html){:target="_blank"} that had an idea and needed someone that knew how to build it.
My teacher recommended him me as he knew my coding level form the hight school project.

It was a bit like a freelance type of work as he was not a corporation and he just wanted a particular program form me.
It was not the first time that I made money from coding as when I was about 13 years old, I arrived at the second place in the Grip-It robotic competition at the Leman Make and the price was some money.
However it was my first coding job where I would get payed for doing something that someone requested.

It made me learn how to talk to a client and understand what he wanted.
I regularly made some reports containing the avancement of the project.
It ultimately confirmed my will to work as a developper.

## The Idea

The project that I needed to build was about training to shoot.
Shooting casts a lot of money: you need to pay the location where you train and all the bullets that you use.
It also takes a lot of time to go to this location and therefore you do not train really often.

The solution that I needed to build was a way to train in a room of your house but not using real bullets but a laser gun.
That way, you are not spending a lot of money on bullets and you can train anytime you want as it only takes a few minutes (even seconds) to set up the system.
If you have a 20 minutes break you could now practice in your room.

In order to do so, there is a little laser bullet that you can insert into your usual gun and when you press on the trigger, it turns the laser on for an instant and you can repeat the operation.

My work was to build a target to shoot on with the laser bullet.
The target was projected on a wall with a video projector.
That way I could chose what to show and build a user interface to change what target to use or to emulate the distance by reducing the size of the projected image.
I also used a camera to detect the laser impact and to place an impact image on the projected target precisely where the shot hit.
Shooting on the button shown on the user interface would trigger them.
That way navigating through the menus and changing the settings could also be done using the laser weapon.
I also made a system to see your statistics afterwards and therefore track your progress.

It was a big project but I was very motivated by this cool idea even thought there was a lot of difficulties that I did not knew how to solve in the beginning.

## ⚙️ Program And Challenges

I chose to code this project in Python because it was the language that I knew the best.
I ran it on a [Raspberry Pi](https://www.raspberrypi.org/) to keep things compact an easy to set up.
I knew that there was a lot of challenges about things that I had never done before like video recognition.
I needed to be able to detect a laser shot on the wall with a carmera while displaying feedbacks and the user interface on the wall with a projector.

This is a little representation of the architecture I built:

<div align="center">
  <img width="550px" alt="Hardware project architecture" src="/assets/images/posts/laser_gun_projected_target/documentation/Architecture_Hardware_en.jpg">
</div><br>

So the user interface was projected on a wall and the laser shots were recorded with a small webcam.
The gun did not need to be connected to the Raspberry Pi because it just fires a laser.

### Camera Detection

The first thing that I decided to do was to get the input from the user: detecting a laser shot on the wall.
I chose to do that first because it was the thing that I was the least confident about so I would not waste time on the other things if I could not built the detection.

I decided to build a proof of concept where the goal was to record a laser shot and display the impact on the wall where it landed. I also wanted to try the user interface interaction by shooting on buttons.
Therefore I had two things to build in order to test if I was really qualified to build this project:

1. A plain laser detection on the wall with a simple webcam
2. Camera calibration with the projector
3. Basic user interface projected on the wall where I can display an impact along with a single button to clear all the displayed impacts

I made the choice to go with the [OpenCV](https://opencv.org/){:target="_blank"} library and a simple Logitech webcam.

#### Laser Detection

In order to test the laser detection I build a small box with a red button on it that will activate a laser. The box had two modes:

1. While the button is pressed the laser will remain activated (like a presentation pointer)
2. On button press a laser shot is simulated: the laser is activated for 25 milliseconds before turning off automatically

As I did not have the final laser bullet at the time, I was forced to build this small system to try it out.
This is how it looked:

![Home made laser bullet](/assets/images/posts/laser_gun_projected_target/documentation/simulateur_cartouche_laser.jpg)

I successfully built the laser detection from the webcam with mode 1 (constantly showing the laser).
This is a small demonstration of the laser recognition:

<img width="1000px" alt="Laser tracking demo" src="/assets/images/posts/laser_gun_projected_target/documentation/Laser_Tracking.gif">

On the left image you can see the raw feed from the webcam.
In the middle there is the image after the image processing.
On the right image you can see the extracted informations on top of the raw image (blue circle around the laser with a red dot in the center).

Nothing really changes for mode 2 except that I just wait until there is a frame recorded by the camera that contains a laser dot.

#### Camera calibration

I needed to use a projector in order to report the position of the laser shot onto the wall.
But before that, I needed to calibrate the camera with the projector.
The camera needs to know where is the projected surface in order to communicate the position of the shot relatively to the surface of projection.
This calibration will be the first thing to be done when executing the program.
It is establishing a main two coordinates axis system after used across the camera feed (input) and the projected area (output).

That calibration is done in two parts:

1. In the first part, 4 black circles are placed (on a white background) in the 4 corners of the projected area. I coded a function that is detecting those circles and that calculates the center of them.
2. In the second part, a black rectangle is displayed in order to match its corner with the center of the circles from part 1.

The following gif illustrates the circles detection system:

<img width="1000px" alt="Circles detection demo" src="/assets/images/posts/laser_gun_projected_target/documentation/Marks_Tracking_Circles.gif">

We can see the projected area in white on the wall with the four circles on it.
Like the laser detection gif, on the left there is the raw camera feed, in the middle is the image after being processed and on the right is the extracted data displayed on top of the camera feed.
The circles detection is working pretty well.

The next gif shows the rectangle detection system:

<img width="1000px" alt="Rectangle detection demo" src="/assets/images/posts/laser_gun_projected_target/documentation/Marks_Tracking_Rectangles.gif">

As we can see, sometimes the program detects the border of the projection surface as a valid rectangle.
I solved this issue by taking the one with the smallest area if two rectangles are detected.

Once that the program knows the centers and the corners, it calculates the mean two by two in order to have four precise points that it can use to determinate the position of the projected surface in the camera feed.
I decided to cumulate the circles and the rectangle detection in order to gain in precision because the impact needs to be placed exactly where you shot.

I also needed to correct the perspective effect that is deforming a rectangle if we are not looking at it perfectly perpendicular and from its center:

<img width="500px" title="https://www.pyimagesearch.com/2014/08/25/4-point-opencv-getperspective-transform-example/" alt="Perspective correction" src="/assets/images/posts/laser_gun_projected_target/documentation/perspective_transform.jpg">

Once the shared axis system is established the camera must not move at all.
I later added a button in the user interface that re-calibrates the camera just in case the impacts placement feels a bit inaccurate (the camera is moving a bit because of vibrations and other small factors).

The following short video taken with my phone shows the full calibration process:

<div class="video-responsive">
  <iframe src="https://www.youtube-nocookie.com/embed/RavyzJ8D4Is?rel=0" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

It is detecting the shapes pretty fast which makes the whole calibration process short.

#### Display impacts

the last part of the proof of concept was to, feedback after the shot, not easy as the projecteur emmets a lot of light, not enough fps because the laser hit duration was slow and as the hand moves you need to recognize the impact location as fast as possible, it was proving if I was capable of achieving the requested idea

<div class="video-responsive">
  <iframe src="https://www.youtube-nocookie.com/embed/8LZnIDVj-8g?rel=0" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### User Interface

design all the images targets and impacts, tkinter window in full screen mode sent as video input to the projector as application support, remove the mouse pointer, module the target image size depending on the distance you wanted it to be artificially, made the button that can be triggered by shooting on them, display impacts, making the menus to change the settings, made the final screen with the results, menu thumbnails with preselected settings

<div class="video-responsive">
  <iframe src="https://www.youtube-nocookie.com/embed/r6u0h7QLznI?rel=0" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<!-- Targets images -->

<img width="150px" alt="Real impact picture" src="/assets/images/posts/laser_gun_projected_target/documentation/real_impact.jpg">

<!-- Ui menus -->

### Saving the results to access them afterwards

upload ending results screen shot of the ui after crop image, upload to MEGA, accessible on your phone, track your progress

### Raspberry Pi Too Weak

started on my laptop so it was powerful enough to run camera video recognition and user interface output to projector, planning to deploy on raspberry pi, overheated the pi the first time, thought about buying a mini PC but it was expensive, try a lot to optimized the code, found a way over: decrease the video from the webcam resolution

<img width="400px" alt="Raspberry Pi heat sink" src="/assets/images/posts/laser_gun_projected_target/documentation/rpi_heat_sink.jpg">

### The Real Laser Was Too Fast

finally there was this big issue: the real laser cartouche he bought was not long enough to be detected by the camera every time, sometimes the laser turned on and off between two recorded frames from the webcam, big issue but not really my fault as I was not engaged for the hardware part (inside the gun), I told him many times that it would be really great to have all the hardware parts as fast as possible in order to see if everything would work, Everything on my side was working great he just needed to find a way to increase the laser duration so we ended here

## Conclusion

about one month of work, met a couple of times, installation, learned a lot about the programmation (user interface and video recognition) part but also about how to talk with a client and exchange about how he wanted things to be (not building something for myself even if I enjoyed the project, I would not have done some things that way but I listen to his wills) etc
