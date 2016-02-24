---
layout: post
title:  "Flow with Github and Waffle.io"
date:   2016-02-23 12:10:00
categories: coding business development hacking
permalink: /blog/flow-with-github-and-waffle-io
---

I try to have a process where something comes off a trello board and goes onto waffle (via an issue) when it's decided that it REALLY should be added to the codebase. Helps keep the constant growing idea backlog a little separate from the 'this should actually get done' backlog.

1) Create an issue in Github

2) Create a branch with the issue number e.x. 123-new-feature

3) When you push up that branch, waffle will add the label 'in progress' and move the issue over

4) When you open a PR for the branch, include 'closes #123' in the description and it'll associate it on th wafflee board, and close the issue when you merge the pr.

And that's it! Easy-peasy visual tracking of progress on github projects.  Now here's a great recipe for waffles: http://www.tasteofhome.com/recipes/family-favorite-oatmeal-waffles
