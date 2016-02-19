---
layout: post
title:  "Github Pages and Jekyll for Easy-Peasy Static Sites"
date:   2016-01-28 12:10:00
categories: coding business development hacking
permalink: /blog/github-pages-and-jekyll-static-sites
---

Hey everyone, welcome to the re-launch of my personal site! As an obligatory exercise, here’s a write-up on how this site was made with Jekyll and Github Pages. Also in use are HAML and Bootstrap. This guide assumes basic knowledge of using your terminal and navigating to a folder. Special thanks to these previous posts:

Step 1: Creating a github repo

Requirements:
-a github account [create one now if you don’t have one](https://github.com/join?source=mglobel)

This site is developed using [Github Pages](https://pages.github.com/). Github is a wonderful tool for hosting and sharing your source code, and more importantly, collaborating with others. Coding is a communal effort, and Github is the easiest way to join. Github also provides a very useful tool for quickly creating a static website called Github Pages. Github pages is free, easy, and most importantly is super fast to get started. I strongly believe in a positive feedback loop when starting a project or learning something new. Get it up and running and iterate from there. It makes the process far more tangible and enjoyable.

The first thing you’ll need to do is make a Github Repo. A repo is where you store your source code and manage versions. You have two options when using Github Pages for your static site, you can either use username.github.io (or organization.github.io) and use `master` as your deploy branch, or you can simply name the repo whatever you’d like, and use a `gh-pages` branch as your deploy branch. I prefer to use the `gh-pages` as my deploy branch, so that master can be preserved for my primary development branch. This way every push to master doesn’t automatically deploy your site, which could certainly lead to some unforeseen pushes. But make your choice and [make your repo](https://github.com/new). The repo for this site is named [mglobel](https://github.com/mglobel/mglobel).

Once you have your repo on Github, the next part is to create a local repo on your computer. If you have git installed on your terminal, you can `git clone your-https-git-url`. If you have no idea what that means, I’d suggest downloading [Github Desktop](https://desktop.github.com/) and then pressing the giant green button on your github.com repo, ’Set up in Desktop’. Even if you know how to use git from the command line, I’d highly recommend Github Desktop, as it’s a great tool for managing multiple git projects and visually committing, which usually leads to cleaner commits.

When you’ve completed that process, you should have a (mostly) empty folder wherever you downloaded the repo. Open up your terminal and cd into your project directory. Now we’re ready to make things happen!

Step 2: Install jekyll

Requirements:
-a code-friendly text editor (try out (atom)[https://atom.io/] if you don’t currently have one)

Now that you have a repo, you can start setting up your site! My preference for getting started with a project is Jekyll. Jekyll is originally designed as blogging platform, but works great for deploying simple static sites. Static sites are great because they’re incredibly fast (html is generated once and then served to the user through a CDN). Plus, a static site can be far more than just static. Jekyll can compile and serve javascript as well, allowing you to add a lot of functionality and interaction to your ‘static’ site. But, on with the evangelizing, how to actually get your site up..

First things first, let’s install jekyll by running `gem install jekyll` in your repo. Then to create a new site, simply run `jekyll new .`. This’ll generate a few files for you. Now you can run ‘jekyll serve’ and your site should be up and running. Go to your browser and enter `localhost:4000` in the url bar to visit your new web page.

With that you’re ready to start making some changes!

Step 3: Hello world commit

Before we dive in, let’s understand the jekyll project structure. You can check out jekyll’s documentation on the [default directories](http://jekyllrb.com/docs/structure/). For this tutorial we’ll be looking at _config.yml and index.html. From the command line enter `atom .` to open up the project, or open the project in your favorite text editor.

If you’ll just be using this as a static site, feel free to delete the _posts directory. Next open up the index.html file.

Step 4: Create deploy step (Optional, but highly recommended)
This step taken from this post. However I’ve revised it to use the gh-pages branch, so that master can be reserved for development.

**Here’s an interesting thing..you can’t really use github as your cms if you use the deploy step. I may no longer be the biggest fan of it..Or just make that as a note, stick with master branch, and then link to an advanced configuration.

Step 5: Use a custom domain (Optional, but usually desired)

To use a custom domain you’ll need to take a few extra steps. First in your project make a new file in the root CNAME and add your custom domain. Here’s the [directions from Github](https://help.github.com/articles/adding-a-cname-file-to-your-repository/). You can do this from the terminal with two easy commands.

```
touch CNAME
echo ‘your-custom-domain.com’  > CNAME
```
Commit your changes and push up to the repo. Next you’ll need to add two A records through your domain registrar or DNS provider. These will change periodically (though your old ones will always work), but it’s best to grab the latest from [Github directly](https://help.github.com/articles/tips-for-configuring-an-a-record-with-your-dns-provider/).

Step 6: Make a meatloaf (Also optional, but usually even more desired)

Congratulations, hopefully you’ve made this far and are now proudly staring at a pretty basic site with some words on it. Your words. The good news is that making changes is pretty straight forward from here. So why not reward yourself and go make a meatloaf! It’ll last for days while you hold yourself away in a coding black hole frenzy. To get you started, here’s my mom’s recipe, which was her father's recipe.


Great, now you've got a meatloaf!
