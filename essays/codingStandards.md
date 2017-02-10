---
layout: essay
type: essay
title: Coding Standards
date: 2017-02-09
labels:
  - JavaScript
  - Software Engineering
  - Coding Standards
  - Coding Style
---

Coding standards are a very important part of writing code that is easily readable and understandable by others. Having standards in the way code is written is essential to writing large projects in a group environment. It also helps quicken the pace of development of open source projects, and makes it easier to share ideas. 

Linting software is used to check for inconsistencies in coding style. This is helpful, because then the software can be set up to enforce whatever coding style rules that have been decided on for the project. It is easy to think that giving the group of programmers some guidelines on how to style their code would be enough to keep the code easily readable and understandable, and for smaller projects, this can be the case. However, when the projects starts getting bigger, it is much harder to proofread all of the code yourself. You can think of this like the difference between writing a paragraph without Spell Check on your computer, which you can probably proofread and fix in a matter of minutes if not seconds, and writing a book without Spell Check. You could take the time to look through it and fix it yourself, but honestly, why would you want to? Don't you have better things to do? 

For the last week, we have been using a tool called ESLint. It is easy to install and use, especially if you already have Node and Node Package Manager. ESLint does a good job catching coding style errors and also makes them very easy to fix. I can't speak for other IDEs, but if you are using IntelliJ, you can simply right click on your file and select "fix ESLint problems" and it will fix the vast majority of the coding style issues for you. Since we are using the Air B&B style guide for this class, sometimes the style issues are annoying, like having to say "x += 1" instead of "x ++", but the best part is, it is fully customizable with whatever style guide you want to use, or you can even make your own.

With everything that has been said so far, you might be thinking that fixing stuff like "x ++" or changing double quotes to single quotes doesn't really seem that important. Well, you are probably right, and honestly, if that was all ESLint did, I probably wouldn't spend the time to ever use it after this class. My favorite thing about it is that if someone else writes code like this

	while(x = true)
		y = x * 2;
		x ++;

it will give an error and make the code change to this.

	while(x = true){
		y = x * 2; 
	}
	x ++; 

When that while loop is in the middle of 1000 or more lines of code, it can be quite easy to overlook it while trying to figure out where the bug is in the program. 

All in all, if you take the 10 to 30 minutes to set up some sort of Linting software in your development environment, it will most likely be more of a help than a hindrance, because in the long run, it will probably save you far more time when looking through your own or someone else's code. 
