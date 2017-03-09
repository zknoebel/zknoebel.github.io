---
layout: essay
type: essay
title: Meteor Gotchas
date: 2017-03-09
labels:
  - Meteor
  - JavaScript
  - ESLint
  - FlowRouter
---

First problem:


Second problem
One of the biggest problems I have had with Meteor might not be with Meteor itself, but with the combination of Meteor's expected project layout and IntelliJ 2016 while using ESLint. This problem occurred when I was accessing the directory of an image to be used for the background of my pages for a project. The project was to be made in stages. The first stage was to make a mock up of the first page and the second stage was to make mock ups of the subsequent pages in the project. The way that the Meteor project is set up lets the background of all web pages use the same block of code. The way the Meteor accesses the "images" directory, has you use "/images" as the path rather than the actual path "/public/images". Because we are using ESLint, and Intellij, just writing "/images" brings up an error saying that the directory does not exist. So to fix it I changed it to "/public/images" and the error went away, but when I brought it up in Meteor, Meteor could not find the directory. 

With all this confusion, I ended up changing it to just "images" and then it worked in Meteor and IntelliJ/ESLint did not complain either. I finished the first part of the project and everything was up in good working condition. Little did I know that in the second stage of development this change would come back to haunt me. 


