---
layout: post
title: "LaTeX writing setup"
sub_title: "Setting up a LaTeX writing environment designed to write LaTeX faster and easier."
introduction: "You can access all my configuration files regarding my LaTeX writing environment on the following GitHub repository:"
actions:
  - label: "Project's GitHub repository"
    icon: github
    url: "https://github.com/gruvw/latex-setup"
image: "/assets/images/posts/latex_writing_setup/main.png"
tags:
  - Side Project
toc: true
---

I decided to take notes during lectures with LaTeX and this is how I set up my LaTeX writing environment.

## 🗂️ Environment decision

I went through a lot of different writing environments before settling with LaTeX on VSCode.

### Markdown note taking

Before switching to [LaTeX](https://www.latex-project.org/), I was taking notes in [Markdown](https://en.wikipedia.org/wiki/Markdown) using the [Typora](https://typora.io/) editor.
Typora is, by far, the best Markdown editor available. I is a [WYSIWYG](https://en.wikipedia.org/wiki/WYSIWYG) application that has support for math equations preview, images copy-paste, code fences, diagrams, etc.
I really liked taking notes in Markdown using Typora as it was easy to use and WYSIWYG was very convenient.

One issue that I had with Typora is that it did not have a way to create and use snippets (textual shortcuts).
As I were typing a lot of math during lectures, I needed a way to write math faster.
I found the [AutoKey](https://github.com/autokey/autokey) application which allowed me to define some snippets that I could use in any desktop application, Typora included.

This markdown setup was great and I enjoyed using it for a while until some issues came up:

1. Files containing a lot of math or code fences were starting to lag, there was some delay when typing
2. I wanted to include some LaTeX packages but that was not possible due to the fact that Typora is using [MathJax](https://www.mathjax.org/) to render equations.
3. I needed a better snippets support to write faster

It is because of all these reasons that I decided to switch from Markdown to LaTeX even though I knew that I will not be able to have the same WYSIWYG quality as in Typora.

### LaTeX on Vim

As I decided to take my notes in LaTeX, I needed an [IDE](https://en.wikipedia.org/wiki/Integrated_development_environment) to write LaTeX more easily.

I already knew the blog post from Gilles Castel, [How I'm able to take notes in mathematics lectures using LaTeX and Vim](https://castel.dev/post/lecture-notes-1/) (which I highly recommend you to read), so I decided to take notes in [Vim](https://www.vim.org/).
I was familiar with Vim keybindings so that was not an issue at all for me.

Vim was pretty hard to configure correctly.
The "live" compilation mechanism took me a long time to set up and SyncTex was not working properly.

I used [Zathura](https://pwmt.org/projects/zathura/) as my pdf viewer.
I used the [UltiSnips](https://github.com/SirVer/ultisnips) plugin as my main snippet engine.
This plugin is just amazing! It works perfectly and the possibilities are endless.

After using Vim as my main LaTeX editor for a week, I was not really convinced about it...
I think that I needed an IDE with more features than vim when working with LaTeX documents.
LaTeX files can get long pretty fast and the whole compilation process was not as good as I wanted it to be.
I was just not confortable enough with Vim so I decided to switch once again.

## 🔵 VSCode

I am pretty used to [Visual Studio Code](https://code.visualstudio.com/) as it is my main IDE.
I already wrote some LaTeX is VSCode so I had some idea about how to configure it the way I wanted it to be.

I use two LaTeX specific extensions:

- [LaTeX Workshop](https://github.com/James-Yu/LaTeX-Workshop): Providing core features for LaTeX typesetting
- [LaTeX Utilities](https://github.com/tecosaur/LaTeX-Utilities): Providing fancy features that are less vital to the basic experience editing a LaTeX document

I just needed to configure the `settings.json` to have the behaviors that I wanted.
After that I was able to compile my LaTeX documents easily and the Math Preview Panel from LaTeX Workshop is really useful for writing math equations.
SyncTex is working great out of the box too.

I also use the [Vim extension](https://github.com/VSCodeVim/Vim) for VSCode in order to use Vim keybindings.

### Snippets

The only thing that was not working great was snippets.
VSCode provides a snippet engine but it was not exactly what I wanted as code interpolation was not possible and there was no way to trigger a snippet automatically.

This is when I found the [HyperSnips extension](https://github.com/draivin/hsnips).
I don't know why this extension doesn't have more downloads as it is a very powerful snippet engine for VSCode.
It is very similar to UltiSnips on Vim so it did not take me too long to transfer my snippets.

After creating and solving (creator was really active) some issues on the extension's GitHub repository, I was really happy with the result.

The extension even supports context matching which allows some snippets to work only when writing math for example.

## 📝 Conclusion

It was really hard to set up a LaTeX writing environment that suited all my needs and I had enough of switching technologies or IDE once a week.
Setting up environments and IDE are not things that I really enjoy doing, but now I am  happy about my writing environment.

I am able to take notes fast enough thanks to snippets.
The compilation is working well and I can preview the pdf to the side if needed.
SyncTex makes it easy to navigate from code to pdf and vice versa.

## 🖊️ 2023 / 09 - Edit

After more than 2 years editing and writing LaTeX (and code) using VSCode, I finally took the leap and switched (back) to (Neovim)[https://neovim.io].  
This decision was motivated by multiple factors:

- VSCode is proprietary. I know there is VSCodium out there but the whole application feels too proprietary to me.
- VSCode is awfully slow. I hate more and more Electron based applications. I want fast and delay free typing especially in my code editor.
- Bloated software. VSCode has way too many features and I don't use (or even know) half of them. When it is not builtin, adding plugins is made so easy that I too often found myself installing plugins that I really don't need.
- Configuration as code. Neovim uses lua for configuration and it is awesome. I can extend my editor exactly the way I want.
- Vim motions "emulation" in VSCode feels like a dirty workaround and not very much configurable.
- GUI is not the right kind of tool for text editing. When writing code I live in the terminal so I was finding myself switching back and forth between a GUI and the terminal which is not ideal. This goes without saying that the builtin VSCode terminal is basically unusable.

I replaced VSCode HyperSnips by Neovim (LuaSnips)[https://github.com/L3MON4D3/LuaSnip] and rewrote my snippets in lua (not too difficult to transition).  
Two months into my Neovim config and I haven't been happier writing code and LaTeX.  
Really the best improvement is **speed**, I am so much faster and proficient in Neovim. The startup time is below a 100ms and the snippets are triggering instantly.

Configuring Neovim was however pretty difficult to learn at first but there are good tutorials and documentations out there.

