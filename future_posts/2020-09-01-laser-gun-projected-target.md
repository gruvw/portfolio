---
layout: post
title: "Laser gun projected target"
sub_title: "A target projected on the wall that you can shoot on using a laser gun."
image: "/assets/images/posts/laser_gun_projected_target/main.jpg"
tags:
  - Python
---

There is sadly no code that I will share for this project as I was payed to build the software.
I will however describe and explain my work as best as I can below.

## My first coding job

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

## The idea

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

## Program and challenges

python program ,many challenges and things that I had never done

### Camera detection

Feedback after the shot, camera looking at the projected user interface, camera initialisation and detection, not easy as the projecteur emmets a lot of light, plan transformation in order to go from a trapeze to a rectangle, establishing an axis, laser detection and getting the coordinates on the axis, not enough fps because the laser hit duration was slow and as the hand moves you need to recognize the impact location as fast as possible, started here as it was proving if I was capable of achieving the requested idea, built a small laser pointer and try it out

<div class="video-responsive">
  <iframe src="https://www.youtube-nocookie.com/embed/RavyzJ8D4Is?rel=0" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<div class="video-responsive">
  <iframe src="https://www.youtube-nocookie.com/embed/8LZnIDVj-8g?rel=0" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### User interface

design all the images targets and impacts, tkinter window in full screen mode sent as video input to the projector as application support, remove the mouse pointer, module the target image size depending on the distance you wanted it to be artificially, made the button that can be triggered by shooting on them, display impacts, making the menus to change the settings, made the final screen with the results, menu thumbnails with preselected settings

<div class="video-responsive">
  <iframe src="https://www.youtube-nocookie.com/embed/r6u0h7QLznI?rel=0" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Saving the results to access them afterwards

upload ending results after crop image, upload to MEGA, accessible on your phone, track your progress

### Raspberry pi too weak

started on my laptop so it was powerful enough, planning to deploy on raspberry pi, overheated the pi the first time, thought about buying a mini PC but it was expensive, try a lot to optimized the code, found a way over: decrease the video from the webcam resolution

### The real laser was too fast

finally there was this big issue: the real laser cartouche he bought was not long enough to be detected by the camera every time, sometimes the laser turned on and off between two recorded frames from the webcam, big issue but not really my fault as I was not engaged for the hardware part (inside the gun), I told him many times that it would be really great to have all the hardware parts as fast as possible in order to see if everything would work, Everything on my side was working great he just needed to find a way to increase the laser duration so we ended here

## Conclusion

about one month of work, met a couple of times, installation, learned a lot about the programmation part but also about how to talk with a client and exchange about how he wanted things to be etc
