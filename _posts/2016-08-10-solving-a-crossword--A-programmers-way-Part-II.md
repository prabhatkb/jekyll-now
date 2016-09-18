---
layout: post
title:  "How to solve a crossword! - Part II"
date:   2016-09-02 21:30:46 -0700
---

## The first commit to Git.

<div style="text-align:center"><h4><b>Yep, this post is entirely about pushing a commit to Git.</b></h4></div>

There come's a point in everyone's life where they realize how spectacularly stupid they were. I had that epiphany at the very step of working with this project.

Any programmer worth his salt, knows how to Git. It is so common a skill, that I never thought for a second that I'd completely forget it. After initializing my repository, my remote push failed saying that I don't have the necessary privileges. My github username was set to something **_utterly random_**. What? Time-out!

<br/>
<div style="text-align:center"><img src ="../../../resources/hades_timeout.jpg" /></div>
<br/>

Turns out I already have another github account already initlialized in my Mac. I don't even remember when I did that! Anyway, I fixed the configs and tried again. 

It failed again! It seems Git has changed since I last used it. Git's default push configurations are [different from before](http://stackoverflow.com/questions/13148066/warning-push-default-is-unset-its-implicit-value-is-changing-in-git-2-0) and I had to go back and edit my configs. This one's on me for completely slacking off and not following up on what's happening in the outside world.

<br/>
<div style="text-align:center"><img src ="../../../resources/hades_slacking.jpg" /></div>
<br/>

Anyway, edited the push configurations appropriately and tried again.

A spectacular Fail!!! *I dont' have access to push to my own repo*. Wait, what?

<br/>
<div style="text-align:center"><img src ="../../../resources/hades_i_own_you.jpg" /></div>
<br/>

Root of the problem: My keychain was supplying outdated credentials. Thankfully, someone in the internet experienced the same and listed a solution in Stack Overflow. Thank god for 8 Mile and Eminem in the background, or I'd quit at this point. So after purging everything in my keychain, I tried again.

Yep, it failed.

<br/>
<div style="text-align:center"><img src ="../../../resources/hades_im_fine.jpg" /></div>
<br/>
<div style="text-align:center"><b><i>"Files were to fricking large to use Git"</i></b></div>
<br/>
The output had instructions to try _git lfs_ (Git's Large File System). Huh, I didn't know git had a cool functionality like this! I spent thirty minutes reading up on git's LFS before I realized how amazingly stupid I am. I could add those mundanely large files to .gitignore and be done with the whole thing in a matter of five seconds.

Finally the push succeeded and my first commit is submitted to Git.

<br/>
<div style="text-align:center"><img src ="../../../resources/hades_approves.jpg" /></div>
<br/>