---
layout: post
title: "Laser gun projected target"
sub_title: "A target projected on the wall that you can shoot on using a laser gun."
image: "/assets/images/posts/laser_gun_projected_target/main.jpg"
tags:
  - Python
---

no code to see as it was payed but I will explain the project below

## My first coding job

recommended after my TM by my teacher, freelance kind, not first money from coding -> robotic competition, first coding job, talking with a client, making what he wants, comptes rendus, confirmed my will to work as a dev

## The idea

shooting costs a lot of money and time during déplacements, train to shoot from home with a laser in the gun shooting at a projected target and place an impact where you shot after, custom targets with custom emulated distances, access the menu with the buttons you can shoot on, see your stats after

## Program and challenges

python program ,many challenges and things that I had never done

### User interface

design all the images targets and impacts, tkinter window in full screen mode sent as video input to the projector as application support, remove the mouse pointer, module the target image size depending on the distance you wanted it to be artificially, made the button that can be triggered by shooting on them, display impacts, making the menus to change the settings, made the final screen with the results, menu thumbnails with preselected settings

### Feedback after the shot

camera looking at the projected user interface, camera initialisation and detection, not easy as the projecteur emmets a lot of light, plan transformation in order to go from a trapeze to a rectangle, establishing an axis, laser detection and getting the coordinates on the axis, not enough fps because the laser hit duration was slow and as the hand moves you need to recognize the impact location as fast as possible, started here as it was proving if I was capable of achieving the requested idea, built a small laser pointer and try it out

### Saving the results to access them afterwards

upload ending results after crop image, upload to MEGA, accessible on your phone, track your progress

### Raspberry pi too weak

started on my laptop so it was powerful enough, planning to deploy on raspberry pi, overheated the pi the first time, thought about buying a mini PC but it was expensive, try a lot to optimized the code, found a way over: decrease the video from the webcam resolution

### The real laser was too fast

finally there was this big issue: the real laser cartouche he bought was not long enough to be detected by the camera every time, sometimes the laser turned on and off between two recorded frames from the webcam, big issue but not really my fault as I was not engaged for the hardware part (inside the gun), I told him many times that it would be really great to have all the hardware parts as fast as possible in order to see if everything would work, Everything on my side was working great he just needed to find a way to increase the laser duration so we ended here

## Conclusion

about one month of work, met a couple of times, installation, learned a lot about the programmation part but also about how to talk with a client and exchange about how he wanted things to be etc
