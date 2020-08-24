---
layout: post
title: "Creating a python package"
sub_title: "The creation of my first python package: PrintBetter"
introduction: "You can access the source code and the documentation regarding this package on the following GitHub repository:"
actions:
  - label: "Project's GitHub repository"
    icon: github
    url: "https://github.com/gruvw/printbetter"
image: "/assets/images/posts/creating_a_python_package/main.png"
tags:
  - Python
---

I created a Python package which keeps track of what I am printing to the console in a log file along with the possibility to add a prefix to what I am printing.

## The Idea

As I coded multiple python programs that were running on a [Raspberry Pi](https://www.raspberrypi.org/) all day long, I always wanted to keep track of what my program was doing when. In order to do so, every time that my program received a piece of information or was actually doing something, I printed a text explaining what was going on to the console.
This way, it is easy to debug after a problem occurred on some part of a project as I was knowing if the server received or not the information and if it took the right actions based on it.  
I was obviously not constantly watching the console feed all the time so I also needed to print the time before printing out a statement. Therefore, I was easily able to debug what when wrong at a certain time based on the console feed.

I was still facing two issues:

1. When a bug causes my python program to crash, I loose all the console feed containing the precious debugging data.
2. When I restart my program, I am not able to get back the previous console feed. This way I only had the currently running console feed and no history of the previous runs.

This is when I had the idea of creating a python package which could print out statements directly with a prefix containing the currently day and time. The package could also save the console feed inside a log file. I would then be able to see the console feed after closing the program and access any past run output.

## The Old Way

Before the creation of this package, I was printing out a statement this way:

```python
import time  # one time only

hour = time.strftime("%d.%m %H:%M:%S |  ")
statement = "-> Data sent successfully"
print(hour + statement)
```

Every time I needed to print out something I was creating a prefix using the [_strftime_](https://docs.python.org/fr/3/library/time.html#time.strftime) method of the [_time_](https://docs.python.org/fr/3/library/time.html) package (line 3).
After that I concatenated the prefix with the statement before printing the result (line 5).
