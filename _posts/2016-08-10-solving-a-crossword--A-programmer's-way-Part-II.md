---
layout: post
title:  "How to solve a crossword! - Part II"
date:   2016-09-02 21:30:46 -0700
---

There come's a point in everyone's life where they realize how spectacularly stupid they were. I had that epiphany while I started working on this project.

Any programmer worth his salt, knows how to Git. It is so common a skill, that I never thought for a second that I'd completely forget it. After initializing my repository, my remote push failed saying that I don't have the necessary privileges. My github username was set to something **_utterly random_**. Huh! I didn't even know how that happened.

Anyway, fixed the configs and tried again. Another Fail! It seems Git has changed since I last used it? [Git's push.default is unset](http://stackoverflow.com/questions/13148066/warning-push-default-is-unset-its-implicit-value-is-changing-in-git-2-0) and I had to go back and edit my configs. This one's on me for not following what's happening in the non-Google world.

Let's try again now. Spectacular Fail!!! I dont' have access to push to my own repo! Root of the problem: My fucking keychain was supplying outdated credentials when it shouldn't have. Thankfully, someone in the internet experienced the same and listed a solution in Stack Overflow. Thank god for 8 Mile and Eminem in the background, or I'd quit at this point.

Yeah, it failed again.

<div style="text-align:center"><img src ="../../../resources/hades_im_fine.jpg" /></div>
<br/><br/>
<div style="text-align:center"><b><i>"Files were to fricking large to use Git"</i></b></div>
The output had instructions to try _git lfs_ (Git's Large File System). Huh, I didn't know git had a cool functionality like this! I spent thirty minutes reading up on git's LFS before I realized how amazingly stupid I am. I could add those mundanely large files to .gitignore and be done with the whole thing in a matter of five seconds.