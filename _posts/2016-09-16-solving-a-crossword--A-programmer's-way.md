---
layout: post
title:  "How to solve a crossword!"
date:   2016-09-02 21:30:46 -0700
---

## **Inspiration:**
### I have nothing better to do in life. So, I might as well!

Truer words have never been ~~spoken~~ typed. I've always loved solving puzzles. They're a fun way to pass the time. But crosswords are always something that I steered away from. **Why?**

**1 Across: "Fried Green Tomatoes" scripwriter Fannie** - What the actual shit.

**14 Across: "Great!"** Seriously. That's it. The word _Great_ is the clue. It has an exclamation point and quotes around it.

**17 Down: Half a rack.** Wait, half a what??? Oh... racks... Internet has taken away my innocense.

**24 Down: Gladiator's weapon.** 5 letters? Haha, I got one. Sword. Wait, it could be a Spear. Meh, Spear is unlikely. Have you ever seen a gladiator with a spear? Wait, could this be a word in Latin? I'll pissed as hell if the answer was in Latin. Fuck this shit, I'm out.

I suck at it, **_that's why_**. English (or in some cases Latin) is not my native language. There's no way I can understand the underlying subtle nuances in a crossword clue and figure out the damn word. Hell, I'd bet that I wouldn't even know more than half the words in the solution. So, I decided to stick to my strengths, PROGRAMMING.

![Batman Facepalm](../../../resources/batman_facepalm.jpg)![Gandalf Facepalm](../../../resources/gandalf_facepalm.jpg)![Picard Facepalm](../../../resources/picard_facepalm.jpg)![Joker WTF](../../../resources/joker_wtf.jpg)
<br/>
<br/>
YEP, that's what I'm gonna do. I'm gonna build myself an iPhone app that can take a picture of a crossword and solve it for me.
<br/>
<br/>

First let's break this down into smaller problems. From the image, I have to get all the information about the crossword:
- The grid. Number of rows and coloumns.
- Identify the blank vs black grids and the numbers hiding in the corner.
- The clues. What's across and what's down. Most crosswords don't give out the number of letters in the word. [You Bastards!](../../../resources/south_park_you_bastards.jpg)

After constructing the problem, now comes the solving part. Now, coming to my skills in NLP (Natural Language Processing)... Oh, who am I kidding, I know nothing about it. Absolutely nothing, let alone designing my own word-solving machine. So what I'm gonna do is to simply work on top of the existing dictionary.com website. They have a cool thing where you can type the clue, and it gives you a list of possible solutions.

Firstly, I'd have to get the grid from the puzzle. I know from a friend of mine back in my university who once did something with OpenCV, a library for image processing. Yeah, I could use that to get the grid info.

Next, I would need to get a hold of the clues from the picture. A simple Google Search gave me a C++ library Tesseract that does image-to-text translation. I don't know how they do it, but damn its impressive. I just saw a demo of it and I'm convinced that it should do the trick. With these two in place, I'm well on my way to start solving the damn crossword.

Lastly, I'd have to curl against dictionary.com for EVERY single clue. There's no avoiding that. I'm hope there won't be any issue with this. I don't think this website gets much traffic to worry about a DDoS attacks. Hell, they might even notice a spike because of what I'm about to do! I'll come back to this later, if the website does start shouting at me.

Effectively for each clue, I'll be getting a solution with an associated confidence interval. That's all I need to start solving this thing. Start from a candidate answer with the highest confidence and go back from there and make sure any new word that I insert into the grid plays along nicely with the existing ones!

I'm not sure if there is something like this already online, but I don't care.

<div style="text-align:center"><img src ="../../../resources/bender_makemyown.jpg" /></div>
<br/>
<br/>