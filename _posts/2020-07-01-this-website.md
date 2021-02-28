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
toc: true
---

In july 2020, I decided to build a website where I would be able to publish my different projects related to programming. That led to this website hosted on GitHub (powered by [GitHub Pages](https://pages.github.com/){:target="_blank"} and [Jekyll](https://jekyllrb.com/){:target="_blank"}).

## 📡 The Concept

I had the idea of creating this kind of website a while ago.
I wanted something in between a portfolio website that I would use to show of my work and a medium blog where I would just publish my work in case someone was interested.
I also wanted a way to keep track of what I was doing and when.
Creating a website was a cool solution because when I finished a programming project I would just write a text about it, add some pictures if necessary and publish it.
That way I could come back to it in one or two years and track my progress.

The only issue I had was that I wanted the publishing process to be as straight forward as possible.
I didn't want to spend hours every single time I was going to write about something styling everything and make the article look great.
I wanted to write whatever I wanted and click on a button in order to publish it.
[Markdown](https://fr.wikipedia.org/wiki/Markdown){:target="_blank"} was the perfect solution for this:

* Very simple to format everything
* No waste of time writing tags and dividing into multiple divs...
* Easy to include links and photos

This matched up exactly what I was looking for.

The only issue about it was to actually create the website from scratch...
I would have had to make:

* A program that converted my markdown files into [HTMl](https://fr.wikipedia.org/wiki/Hypertext_Markup_Language){:target="_blank"}
* The landing page
* Create styles for the website
* Make everything responsive
* Create an easy way to publish new projects
* ...

That is why I did not make the website earlier.
I was often thinking about it but I was too lazy to do everything and I preferred spending time on more interesting and newer projects.

### Solution

Someday I decided to find an alternative.
As I was not motivated enough to build my very own website from scratch, I decided to learn a bit more about [GitHub Pages](https://pages.github.com/){:target="_blank"}.
I had heard of it before but I never really took the time to investigate it.
When I read about how easy it was to set up a repository to become a GitHub Pages website I was blown away.
I immediately found motivation to build the whole website and that is when I started this project.
GitHub Pages was perfect for what I wanted: you just need to push any new article that you wrote to the GitHub repository and your site would be automatically updated.

What really put the cherry on top was when I found out about [Jekyll](https://jekyllrb.com/){:target="_blank"} integration in GitHub Pages.
I had never heard about Jekyll before but it was perfect for what I needed, already built for me.
It is basically a way to convert markdown files directly into static blogs and websites.

In one day I found the solutions to all the things that were keeping me from doing this website that I wanted so much.
The only issue about Jekyll and GitHub Pages was that my website will not be the most dynamic and original one out there with tones of javascript animations etc...
But in reality, that was not too bad because it was not essential.
I just wanted a place to publish and keep track of my work so why bother having the fanciest website if that was not the main purpose.

## 🚧 Setting Up

Even if I found the solutions I needed to build this website easily, I still needed to actually do it.
I had never used either of GitHub Pages or Jekyll before.
I also needed to buy a domain name and redirect it to GitHub Pages.
So it was far from done yet.

### Hosting

I needed to do three different things in order to host my website:

1. Creating the github repository
2. Setting up GitHub Pages
3. Buy a domain name and connect it with GitHub pages

The first one was pretty easy: I just created a repository and named it _portfolio_.
At the time I thought I would do a website that would be more similar to a real portfolio and a more professional kind of website.
But once I really got into creating I chose to change the purpose into just being a way to keep track of what projects I was doing when and share it with whoever I wanted.
In the end it is a bit in between a portfolio and a blog but I am pretty happy about it.

The second thing was to actually transform the freshly created repository into an actual website.
For that I used GitHub pages which is a really easy way to host a static website for free.
In order to set it up I just went into the repository settings tab and scrolled down to the GitHub Pages section.
Then I just needed to select the branch along with the root directory and I was good to go.

The last thing I wanted to change about the hosting part was the url that GitHub generated for the repository website which was something like _gruvw.github.io/portfolio_.
I looked to see if the domain gruvw.com was still available and it was so I bought it.
Luckily my username is not a really common english word so it was pretty cheap (about 10$ a year).
After buying the domain I set up the DNS records to point on my GitHub repository as explained in the [GitHub Pages documentation](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site#configuring-a-subdomain){:target="_blank"}.

At this point the hosting part was finished and I was ready to start creating my website.

### Jekyll

Jekyll allowed me to build and update my static website with the theme I wanted.
I stared with looking for a theme I liked on a [theme collection website](http://jekyllthemes.org/){:target="_blank"}.
There are a ton of them and I was surprised when I discovered that the [Read The Docs theme](https://github.com/rundocs/jekyll-rtd-theme){:target="_blank"} was available (I might use it if I need to create a documentation for a futur project).
I went with the [Basically Basic theme](https://github.com/mmistakes/jekyll-theme-basically-basic){:target="_blank"} because I wanted something simple and straightforward.

Jekyll was designed for building blog websites but I wanted something a bit different so I modified the template to interpret a blog post as a projet.

Once I set up the theme in the repository and got the local [Ruby](https://www.ruby-lang.org/fr/){:target="_blank"} server running I was ready to configure the website.
There were a few things to configure in order for everything to be the way I wanted:

* Title
* Description
* Links to GitHub and socials
* Contact email
* Domain name and url
* Pictures
* Search
* Plugins
* SEO

When I finally got the technical aspect of Jekyll configured, I needed to slightly adust the [CSS](https://fr.wikipedia.org/wiki/Feuilles_de_style_en_cascade){:target="_blank"} and HTML templates in order to fix little details (open links in new tabs, lines number in code fences, ...).
I also added small things like a table of contents.

I finished by writing the default pages:

#### 404 Not found

A simple page that will inform a user that the page he is trying to access does not exist.

#### The index

The landing page of the website which was a bit weird to write: I needed to write it in markdown but name the file with a `.html` extension and the markdown file needed to be written in a strange way...

#### About page

Just wrote a text about me and my life.

I needed to modify the template in order to make my images render correctly side by side and the page to still be responsive.

#### JSON Resume

With this project I discovered [JSON resume](https://jsonresume.org/){:target="_blank"} which is a very cool way to write and update your resume.
So I wrote my resume in JSON and integrated it in my website automatically.
It was very easy.

If you are interested in seeing my resume you can find it here:

* On this website: [Resume Page](https://gruvw.com/resume.html){:target="_blank"}
* The raw JSON data on [this GitHub Gist](https://gist.github.com/gruvw/510ea6adf8679429e6078282a87f782e){:target="_blank"}
* On the JSON resume registry: [Gruvw](https://registry.jsonresume.org/gruvw){:target="_blank"}

#### Projects list

The page where all my projects are listed by tags.

## 📝 Publishing Projects

Once the site was finally ready, I just needed to actually write an article for each of my past projects.
I created a new article by adding a markdown file and providing basic informations in the preamble.
This is what this project's preamble looks like:

{% highlight markdown linenos %}
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
{% endhighlight %}

Just after that I started writing the article like I would write any classic markdown file.

The only thing that remained to be done and that took **a lot** of time was to write all the previous projects that I wanted to list on the website.
I chose to try to write a few lines every day even if I was not writing a lot.
It turned out that doing it daily was hard but I managed to write 2 to 3 times a week in my free time.

## ⚖️ Conclusion

In the end I am very happy that I took the time to set up this website because it is really useful.
I now have a way to track my work and progress along with sharing it with others.
All my important projects are listed and summarized in one single place.

The main goal was to be able to publish new articles and projects very easily by writing markdown files and I think that it was 100% achieved thanks to Jekyll.
I recommend for anyone wanting to build something similar to try it out.
The best thing is that it integrates perfectly with GitHub and GitHub Pages which does not even require any maintenance on my side as the website is stored on a repository.
On top of that the hosting is totally free.
The main downside is the website template which is fine but it is not the exact website that I would have created on my own and it lacks a bit of personality.
I tried to fill this lack by writing good content and overall it is not really that big of an issue for me.

It took me a lot of time to write all the projects I wanted to include (projects that I had already made) but once that was done the site looked perfect and I am very happy about it!
