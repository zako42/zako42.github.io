---
layout: post
title:  "Stenoboard arrived"
date:   2016-01-06
categories: plover opensteno stenography stenoboard
---
Today the stenoboard I ordered finally arrived in the mail. [Stenoboard][stenoboard] is an open hardware NKRO 
(n-key rollover) keyboard used for [stenography][wikipediasteno]. It can be used with software like [Plover][githubplover], which is
an open source stenography engine.

Ok, backing up a bit, what the hell is "stenography"?  Stenography (not to be confused with 
Steganography) is a kind of typing shorthand.  You see an example of it in the courtroom, 
when the judge asks the typist sitting on the side of the room to read something back from the 
record. I was always skeptical of those typists, because I didn't think anyone could type fast 
enough to capture everything being said, and figured they were just capturing the gist of what 
was going on. But apparently, they TOTALLY CAN type that fast, because of stenography. According
to the [Open Steno Project][openstenoproject], professional stenographers can hit 225-300 words per minute
(in contrast to good QWERTY typists, who hit 120 wpm), while average human speech is in the neighborhood of 200!
They do this with special keyboards and a more efficient system of typing.

I found out about the Open Steno Project from the Giant Robots podcast by Thoughtbot. Ben Ornstein
interviewed its founder, Mirabai Knight in [episode 164][giantrobots164]. It's a really interesting episode, highly
recommend listening. I had no idea that such a thing existed -- I mean vimmers are always going
around trying to optimize their keystrokes, but this was mind blowing to me. 
If typing were martial arts, these stenographers would be the Bruce Lee kung fu masters.
On top of the speed advantages, there's the added benefit of ergonomics.
It makes sense that to achieve higher possible speeds, economy of motion must be considered.
This efficiency leads to less RSI, which is anathema to anyone typing for a living, like programmers.
I have been experiencing forearm/writst twinges at times, so this is an added attraction for me personally.

Anyway, you can play with Plover using any keyboard, but it helps to have an NKRO keyboard because
stenography uses key "chords" (think of piano where a chord is played by hitting multiple keys at the
same time). Because of this, regular keyboards may choke when combinations of keys are pressed
simultaneously. When playing with it, certain chords were not possible on my laptop keyboard. You
can play with a live demo on the Open Steno Project homepage [here][stenodemo]. I decided to take the plunge and
buy a [Stenoboard][stenoboard], which is "open hardware" designed by Emanuele Caruso. You can download the plans
and build one yourself with Arduino and resistors and diodes and whatnot (3d printing files for the casing are
available as well) or you can purchase the parts from his website [here][utopen].

Which brings me back full circle to the topic of this post.

The Stenoboard I ordered came today as unassembled parts.  Here are some of the photos I took as I
put it together. I opted to purchase the pre-assembled PC boards, which costs a bit more but
you don't need to solder components together.

The parts:<br/>
![the parts]({{ site.url }}/assets/steno_kit_parts.JPG)
<br/>
Putting the right hand portion of the Stenoboard together:<br/>
![right hand guts]({{ site.url }}/assets/steno_right_side.JPG)
<br/>
Both halves of the Stenoboard, showing the innards:<br/>
![both sides]({{ site.url }}/assets/steno_both_sides.JPG)
<br/>
Finished!<br/>
![completed]({{ site.url }}/assets/steno_complete.JPG)
<br/>
It was easy to do, and there are detailed instructions available on github [here][stenoboardinstructions]. One thing to note
for people like me who don't read carefully and can't intuitively gauge sizes of things in the
metric system -- There are 3 different screw sizes, so pay attention when screwing the boards down.
The Arduino board screws down with the 4 smallest size screws (6mm), the vowel keys (the smaller
2 circuit boards) screw down with the 9mm screws, and the rest use the 13mm large ones. With the kit I
purchased, all that was needed was a phillips (+) screwdriver.

Installation is easy -- the Stenoboard is recognized as a keyboard, so it should show up when plugged
in with a usb cable. In my case, I got stuck for a while because I was unwittingly using a charging
cable which fits micro usb, but apparently doesn't have all the pins/wires needed for actual data
transfer. On my mac it did give me that "keyboard not recognized" thing where you
have to press different keys on the keyboard to help identify it. I just skipped all that and it worked
without a hitch. Installing the Plover software is also a snap. When run, Plover opens a small window, with a red 'P'
button to toggle it on/off. When active, the P beomes green. There are some configurable knobs and
buttons, but I haven't used those yet.

Once everything has been set up, I've started going through some [Plover tutorials][plovertutorial].
It's been fun so far and it seems like this will be a neat side hobby. 
It will remain to be seen if I can use stenography to code, especially using vim, etc.
When I mentioned this to my co-worker, he was skeptical that being able to type
faster would do provide any benefits to coding, to which I agree -- typing is the easy part. 
Typing more fluently however, can reduce friction between what your brain is thinking and the final code entered into the
text editor, as any vim user will tell you. But the appealing thing about all this (besides
curiosity and wanting to try something new) is 
the philosophy of a tool which has been carefully engineered to provide power and 
efficiency in an elegant and customizable way. This is the same reason vim appeals to me. 
Whatever the case, I'm not making an argument for or against steno for coding. Undoubtedly my
productivity would suffer throughout the steno learning curve and I couldn't conscientiously allow 
it to affect my work and employer. Maybe when I reach roughly equal proficiency with QWERTY, I
can bring it up with my boss.

Anyway, I'm looking forward to learning and hopefully I will be able to stick 
with it and improve both my typing speed and ergonomics. Right now my steno wpm is like 5. So
I can only improve from here!

[wikipediasteno]:          https://en.wikipedia.org/wiki/Shorthand
[openstenoproject]:        http://www.openstenoproject.org
[giantrobots164]:          http://giantrobots.fm/164
[githubplover]:            https://github.com/openstenoproject/plover
[ploverwiki]:              http://stenoknight.com/wiki/Main_Page
[stenodemo]:               http://stenoknight.com/kws.html
[stenoboardinstructions]:  https://github.com/caru/Stenoboard/wiki
[stenoboard]:              http://stenoboard.com
[utopen]:                  http://utopen.com
[plovertutorial]:          https://sites.google.com/site/ploverdoc/
