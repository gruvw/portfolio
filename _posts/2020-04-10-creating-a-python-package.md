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

Doing it like that let me have the prefix before the statement but didn't store anything in a log file.

## The Creation

### Introduction

Although I coded a lot in Python, I never wrote a package or anything close to it. I took it like a good opportunity to learn a new skill in this language.
I wanted my package to be easily install on any computer with a [pip](https://packaging.python.org/key_projects/#pip) command like the other packages I installed in the past.
This is where I stared.

### PyPi

I needed to first understand where and how to make my futur package available to anyone using the pip command. That led me to search where the different python packages are stored. I found that they are stored on [PyPi](https://pypi.org/), the **Python Package Index**.
Once I knew that I searched a way to publish any package on PyPi. I found [this](https://medium.com/@joel.barmettler/how-to-upload-your-python-package-to-pypi-65edc5fe9c56) tutorial on [Medium](https://medium.com/) wrote by [joelbarmettlerUZH](https://medium.com/@joel.barmettler).
It was really helpful and it was covering everything from the point where you finished writing your code to the `pip install your_package` command.
I read this article so that I knew how to write my code in order to make it easier to publish on PyPi once I would have finished coding my package.

### Coding

Now that I knew how to write my package in a way to make it accessible to anyone, I needed to actually code it.
I started my réflexion by asking myself which categories of statements I wanted my package to be able to display. I found 3 main categories:

1. An information
2. A warning
3. An error

I did some research about log files in python and this is where I found the [logging](https://docs.python.org/3/library/logging.html) package. This discovery made my work a lot simpler because it matched almost perfectly my goal of keeping track of what I was printing inside a log file.
I learned a bit about how to use this package and ran some tests. I was pretty satisfied about it and I started implementing it inside my own package.
It wasn't an issue to use it inside my package because it is part of the [Python Standard Library](https://docs.python.org/3/library/index.html). That meant that I didn't need to mess with requirements or anything like that because (almost) everyone already had the logging package installed on their machines.

I coded the main methods of my package which were:

* The initialisation method, `init`
* The exit method, `exit`
* The info method, `info`
* The warning method, `warn`
* The error method, `err`
* I also added a new category which was the debug method, `debug`

(I am not going to describe each method here but you can read more about them in the documentation of the project that you can found on the [project's GitHub repository](https://github.com/gruvw/printbetter).)

### Customisation

I wanted my package to be as customizable as possible. In order to let the users customise the package, I created the following methods:

1. Customise the printing prefix the way they want, `custom_PRINTPREFIXFORMAT`
2. Customise the logging prefix the way they want, `custom_LOGFORMAT`
3. Disabling or enabling the printing on the console, `disable_PRINTOUT` `enable_PRINTOUT`
4. Disabling or enabling the record of the statements on a log file, `disable_LOGFILE` `enable_LOGFILE`
5. Modify the directory where the log files will be save, `custom_LOGPATH`

(I am not going to describe each method here but you can read more about them in the documentation of the project that you can found on the [project's GitHub repository](https://github.com/gruvw/printbetter).)

### Documentation

### The name

## Publishing

Even thought I read all the explanations detail in the article (see [PyPi](#pypi)) about publishing my package to PyPi I ran into multiple difficulties durning this process.

## Conclusion
