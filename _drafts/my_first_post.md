---
title: Solving a crossword - A programmer's way
---

Anyway, I went on a dating app, welcome to the 21st century. There was a girl who boasted a shit load about crosswords and shit. And that got me thinking, how hard can it be to solve a crossword. English is not my native language, and there is no fucking way I can master it to the level of this, I'm assuming an English Literature major.


Solving a crossword

Alright, there is no fucking way that I am going to beat her at Crosswords, who probably majored in English and being a native speaker. I could stick to my strengths though. Programming.

Yep, that's what I'm going to do for fun right now. I'm going to build myself an iPhone app that can simply take a picture of a crossword puzzle and solves it.

I'm not sure if there is one online, but hey, let's give this a shot. First things first, let's break this down into smaller problems.

1. From the image, I have to get all the information about the crossword.
	a) The grid size
	b) The places where they are black thingies.
	c) The clues. What's across and what's down.

2. After constructing the problem, now comes the solving part. Now, my skills in NLP are not nearly as skillful enough to design my own word-solving machine. So what I'm gonna do is to simply work on top of the existing dictionary.com website which helps people solve problems by reporting what's the possible phrase given the number of letters that's required.

Basically, I'd have to curl against that website for EVERY single clue. There's no avoiding that. I'm not sure if there are gonna be any issues that might happen because of me using the dictionary.com solver. I'll come back to this later if the website starts shouting at me.

Effectively for each clue, I'll be getting a solution with an associated confidence interval. That's all I need to start solving this thing. Let's start with the word that has the highest confidence and start from there. Fill that little fella and from then on out its a walk in the park.

Let's get cracking then.

Firstly, I'd have to get the fucking grid from the puzzle. I know from a friend of mine back in my university who once did something with OpenCV a library for image processing. Yeah, I could use that to get the grid info. Take a picture I can get the grid, the black spots and the numbers in them.

Next, I would need to get a hold of the clues. Again going to be super lazy and just work on top of the Tesseract library. I don't know how they do it, but damn its impressive to convert image to text like that library. I just saw a demo of it and I'm convinced that it should do the trick. With these two in place, I'm well on my way to start solving the damn crossword.

I really hope there is a way to batch my request to the dictionary.com website (how do people call this, an endpoint??? I don't know...). But, I'm getting ahead of myself. First things first, create a project in XCODE!!!!

Github fiasco!!!

Now, on to engineering. First off, I need a picture of a crossword for testing. Done.
