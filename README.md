Wavydots
========

KansasFest 2016, HackFest entry

(Ranking: "Participant")

Paul Hagstrom, July 2016


This is kind of nothing as of v1.0 (though I got an incredibly good prize for my "participant" placing!),
but here's the story.  I kind of like the idea at least, even if I didn't get that far into it at KFest.

The basic idea is this: Apple II graphics are kind of... limited.
But I had come across a couple of particularly impressive "motion illusions" and I thought maybe it would
be interesting if I could leverage perceptual illusions to enhance the graphics beyond what the computer
itself could do.  The illusion that struck me most was this one here:

[blue dots on green, waving](https://en.wikipedia.org/wiki/File:Anomalous_motion_illusion1.png)

It is linked from [the Wikipedia article on illusory motion](https://en.wikipedia.org/wiki/Illusory_motion).

The effect was the strongest I'd ever seen, so I set about to see if it would work in Apple II graphics.

It took me a while of studying it to figure out how the illusion comes about, but it seems that what is
happening is that the blue dot has offset black and white dots under it, which rotate at a slight offset
as you progress across the image.

So, the first step was to try to generate the image.  And that's the main step I actually managed to take.
The program MAKEWAVES is an Applesoft program that will draw a series of circles that implement this.
It draws a white circle, a black circle, and a purple circle, all atop one another but offset slightly, to
get the "shadow" effect.  The program draws it all, then saves the result as WAVEYDOTS.PIC.  This is doing
a lot of trigonometry, running it at >1MHz is recommended.  It only needs to be run once, and, really, it's
just re-generating the WAVEYDOTS.PIC that's already on the disk image.

I think the image can probably be improved.  First of all, it could be made smoother, possibly by hand.
I tried a couple of different color combinations (red on blue, blue on red, green on purple) but the best
effect did seem to be blue on green.  Further experimentation might be interesting, though.

I had intended at this point to make some kind of ocean-based game, and even if possible dig a bit deeper
into what triggers the illusion so that I could kind of force the eye to track in a way that would
magnify the illusory motion.  But, I had pretty much run out of time.

So, as a proof of concept, I basically just lifted an example program from Penguin's The Graphics Magician,
which originally just allowed you to move a little person around on the screen with the keyboard, and I
stuffed in the background image, added some text notes and allowed for ESC to exit, and that's the program
you get when you run WAVEWALK, the main "demo" program.

So, this is very much an early proof-of-concept. I'd like to prove more impressive concepts in this direction.
One potential downside here is that it might look kind of cool, briefly, and then trigger migraines at minute
3 of gameplay.  Which would reduce the funness of game a bit.  But apart from that, this seems like an
interesting way around the graphics and processing limitations imposed by the Apple II.