---
layout: post
title: "This website 💻"
sub_title: "The creation of a website used to share and keep track of my coding projects."
introduction: "You can access the source code and all the files regarding my website on the following GitHub repository where it is hosted:"
actions:
  - label: "Project's GitHub repository"
    icon: github
    url: "https://github.com/gruvw/portfolio"
# image: "/assets/images/posts/"
tags:
  - Web
---

In july 2020, I decided to build a website where I would be able to publish my different projects related to programming. That led to this website hosted on GitHub (powered by [GitHub Pages](https://pages.github.com/) and [Jekyll](https://jekyllrb.com/)).

## The concept

I had the idea of creating this kind of website a while ago.
I wanted something in between a portfolio website that is here to show of my work and amaze people and a medium blog where I would just publish my work in case someone was interested.
I also wanted a way to keep track of what I was doing and when.
Creating a website was a cool solution because when I finished a programming project I would just write a text about it, add some pictures if necessary and in one or two years come back to it and see my progression.

The only thing is that I wanted it to be really straight forward to publish my work on the website.
I didn't want to spend hours every single time I would write about something to style everything and make the article look great.
I wanted to write what I want and click on a button to publish it.
Markdown was the perfect solution for this:

* Very simple to format everything
* No waste of time writing tags and split into multiple divs...
* Easy to include links and photos

This fitted perfectly the need that I had.

The only issue about it was to actually create the website from scratch...
I would have had to make:

* A program that converted my markdown files into html
* The landing page
* Create styles for the website
* Make everything responsive
* Create an easy way to publish new projects
* ...

This is why I did not make the website earlier.
I was often thinking about it but I was too lazy to do everything and I preferred spending time on more interesting and newer projects.

### Solution

Someday I decided to find an alternative.
As I wasn't motivated enough to build my very own website from scratch, I decided to learn a bit more about [GitHub Pages](https://pages.github.com/).
I had heard of it before but I never interested myself about it that much.
When I read about how easy it was to setup a repository to become a GitHub Pages website I was blown away.
I immediately found motivation to build the whole website and this is when I started this project.
This was perfect for what I wanted: you just need to push any new article that you wrote to the GitHub repository and your site would be automatically updated.

What really put the cherry on top was when I find out about [Jekyll](https://jekyllrb.com/) integration in GitHub pages.
I had never heard about Jekyll before but this was the exact thing I needed, already built for me.
It is basically a way to convert markdown files directly into static blogs and websites.

In one day I found the solutions to all the things that were keeping me from doing this website that I wanted so much.
The only thing about Jekyll and GitHub Pages was that my website will not be the most dynamic website out there with tones of javascript animations etc...
But in reality, this wasn't so bad because this was not what I was looking for.
I just wanted a place to publish and keep track of my work so why bothering myself about to having the fanciest website if this wasn't the purpose at all.

## Setting up

Even if I found the solutions I needed to build this website easily, I still needed to actually do it.
I never used either of GitHub Pages or Jekyll before.
I also needed to buy a domain name and redirect it to GitHub Pages.
So it was far from done yet.

### Hosting

I needed to do three different things about hosting my website:

1. Creating the github repository
2. Setting up GitHub Pages
3. Buy a domain name and connect it with GitHub pages

The first one was pretty easy: I just created a repository and named it _portfolio_.
On the moment I thought I would do a website that would be more similar to a real portfolio and a more professional like website.
But once I really got into the creation I chose to change a bit the purpose to just be a way to keep track of what projects I was doing when and share it with whoever I want.
In the end it is a bit in between a portfolio and a blog but I am pretty happy about it.

The second thing was to actually transform the freshly created repository in an actual website.
For that I used GitHub pages which is a really easy way to host a static website for free.
In order to set it up I just went into the repository settings tab and scrolled down to the GitHub Pages section.
Then I just needed to select the branch and the root directory and I was good to go.

The last thing I wanted to change about the hosting part was the url that GitHub generated for the repository website which was something like _gruvw.github.io/portfolio_.
I looked to see if the domain gruvw.com was still available and it was so I bought it.
Luckily my username is not really a common english word so it was pretty cheap (about 10$ a year).
After buying the domain I set up the DNS records to point on my GitHub repository as explained in the [GitHub Pages documentation](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site#configuring-a-subdomain).

At this point the hosting part was finished and I was ready to start creating my website.

### Jekyll

configuration, gemfiles, plugins, search etc, include configurations snippets?

## Publishing projects

how I write a new project motivation etc, layouts, include code snippets

## Conclusion
