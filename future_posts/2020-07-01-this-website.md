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

In july 2020, I decided to build a website where I would be able to publish my different projects related to programming. That led to this website hosted on GitHub (powered by [GitHub Pages](https://pages.github.com/){:target="_blank"} and [Jekyll](https://jekyllrb.com/){:target="_blank"}).

## 📡 The concept

I had the idea of creating this kind of website a while ago.
I wanted something in between a portfolio website that is here to show of my work and amaze people and a medium blog where I would just publish my work in case someone was interested.
I also wanted a way to keep track of what I was doing and when.
Creating a website was a cool solution because when I finished a programming project I would just write a text about it, add some pictures if necessary and in one or two years come back to it and see my progression.

The only thing is that I wanted it to be really straight forward to publish my work on the website.
I didn't want to spend hours every single time I would write about something to style everything and make the article look great.
I wanted to write what I want and click on a button to publish it.
[Markdown](https://fr.wikipedia.org/wiki/Markdown){:target="_blank"} was the perfect solution for this:

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
As I wasn't motivated enough to build my very own website from scratch, I decided to learn a bit more about [GitHub Pages](https://pages.github.com/){:target="_blank"}.
I had heard of it before but I never interested myself about it that much.
When I read about how easy it was to setup a repository to become a GitHub Pages website I was blown away.
I immediately found motivation to build the whole website and this is when I started this project.
This was perfect for what I wanted: you just need to push any new article that you wrote to the GitHub repository and your site would be automatically updated.

What really put the cherry on top was when I find out about [Jekyll](https://jekyllrb.com/){:target="_blank"} integration in GitHub pages.
I had never heard about Jekyll before but this was the exact thing I needed, already built for me.
It is basically a way to convert markdown files directly into static blogs and websites.

In one day I found the solutions to all the things that were keeping me from doing this website that I wanted so much.
The only thing about Jekyll and GitHub Pages was that my website will not be the most dynamic website out there with tones of javascript animations etc...
But in reality, this wasn't so bad because this was not what I was looking for.
I just wanted a place to publish and keep track of my work so why bothering myself about to having the fanciest website if this wasn't the purpose at all.

## 🚧 Setting up

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
After buying the domain I set up the DNS records to point on my GitHub repository as explained in the [GitHub Pages documentation](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site#configuring-a-subdomain){:target="_blank"}.

At this point the hosting part was finished and I was ready to start creating my website.

### Jekyll

Jekyll allowed me to build and update my static website with the theme I wanted.
I stared by looking for a theme I liked on a [theme collection website](http://jekyllthemes.org/){:target="_blank"}.
There are a tons of them and I was surprised when I discovered that the [Read The Docs theme](https://github.com/rundocs/jekyll-rtd-theme){:target="_blank"} was available (i might use that if I need to create a documentation for a futur project).
I went with the [Basically Basic theme](https://github.com/mmistakes/jekyll-theme-basically-basic){:target="_blank"} because I wanted something simple and straight forward.

Jekyll is though in order to build blog websites but I wanted something a bit different so I modify the template to interpret a blog post as a projet.

Once I set up the theme in the repository and got the local ruby server running I was ready to configure the website.
There were few things to configure in order to have everything like I wanted:

* Title
* Description
* Links to GitHub and socials
* Contact email
* Domain name and url
* Pictures
* Search
* Plugins
* SEO

When I finally got the technical aspect of jekyll configured, I needed slightly adust the css and html templates in order to fix little details thant I wanted (open links in new tabs, lines number in codes fences, ...).

I finished by writing the default pages:

#### 404 Not found

A simple page that will inform a user that the page he is trying to access do not exists.

#### The index

The landing page of the website which was a bit wired to write: I needed to write it in markdown but name the file with a `.html` extension and the markdown file needed to be written in a strange way...

#### About page

Just wrote a text about me and my life.

I needed to modify the template in order to have my images to render correctly side by side and the page to still be responsive.

#### JSON Resume

With this project I discovered [JSON resume](https://jsonresume.org/){:target="_blank"} which is a very cool way to make and update your resume.
So I made my resume in json and integrated it in my website automatically, very easy.

If you are interested into seeing my resume you can find it there:

* On this website: [Resume Page](https://gruvw.com/resume.html){:target="_blank"}
* The raw JSON data on [this GitHub Gist](https://gist.github.com/gruvw/510ea6adf8679429e6078282a87f782e){:target="_blank"}
* On the JSON resume registry: [Gruvw](https://registry.jsonresume.org/gruvw){:target="_blank"}

#### Projects list

The page where all my projects are listed by tags.

## 📝 Publishing projects

Once the site was finally ready, I just needed to actually write an article for each of my past projects.
I create a new article by adding a markdown file and providing basic informations in the preamble.
This is what this project's preamble looks like:

```m
---
layout: post
title: "This website 💻"
sub_title: "The creation of a website used to share and keep track of my coding projects."
introduction: "You can access the source code and all the files regarding my website on the following GitHub repository where it is hosted:"
actions:
  - label: "Project's GitHub repository"
    icon: github
    url: "https://github.com/gruvw/portfolio"
tags:
  - Web
---
```

Just after that I started writing the article like I would write any classic markdown file.

The only thing that remained to be done and that took **a lot** of time was to write all the previous projects that I wanted to list on the website.
I chose to try to write a few lines every day even if I was not writing a lot I wanted to do it daily.
It turned out that doing it daily was hard but I managed to write 2 to 3 times a week in my free time.

## ⚖️ Conclusion

Perfect that I can write any new project that easily, still very motivated to see the evolution of the website with the new articles: track my work and progress along with sharing with others
