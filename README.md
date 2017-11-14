## Paddy for Lightroom CC 

Putting this patch out there because it may help others. Especially those with workflows containing a lot of photos. Providing it without an easy install because you must really want it.

### note: specifically Lightroom CC 2015.x (v6.x such as 2015.13), not LR6 standalone, not LR Classic CC (v7.0.x)

A friend asked for help with making Paddy work with Lightroom CC (v6, 2015.x). There are things he did via Paddy with keyboards and a G13 keypad that the newer MIDI2LR does not do. I wanted to try out LRCC (had been staying with LR5), and have used Paddy, so why not. 

Went spaghetti code diving and patched up the last Paddy 5.x  beta release to make it work sufficiently for his and my test purposes. Works in Develop mode. Adjustments in Library are not fixed.

Paddy was an admirable effort. Author "dorfl" had stated he was not a programmer. And the code echoed the statement. Inconsistent naming, mixture of functions and code blocks reused inline, adding strings of text with numbers expecting numbers, all globals, etcetera. And an unnecessarily complicated design with indirection layers, probably a second-system effect of sorts. Something that evolved from doing a task well to a distraction of new features, and it shows in the code. New features over bugs.  But it sorta worked, with good intentions. Author "dorfl" has moved on per the Paddy site. But it was CC BSD licensed, so we're going to have a crack at making it work.

So, use this patch at your own risk. Fixed to make run, target correct sliders, a few obvious bugs, that's it. Attempt only for Lightroom CC 2015.13 (latest update as of October 2017).

Added as a test: selecting (not moving) the Dehaze slider as one of the Paddy commands.
Fixed: some quirks that already existing with Paddy-LR5.
Removed: quit on >LR5 check, registration.

You should already have Paddy working in LR5. And it should only be complaining and exiting on LR CC startup. If this is your first encounter with "trying out Paddy", you should consider taking a look at the MIDI2LR project.

Will not work if you have a Surface like product that enables LR6CC touch workspace option.

This should be looked as a hack, on a hack (Paddy LR5 beta), on a runaway complication (Paddy LR4), on a well intended plan (Paddy LR3). That is, no, I did not try to refactor or tidy it up. Not worth the time. Not releasing an installer, or an easy binary. 

So if you want changes and features made, by all means, attempt it, go code spelunking yourself.  But looks like no one had the mettle to do so the last two+ years. Understandably. It's easier to contribute a meatball than to understand the spaghetti.  If you want to have a go at this yourself, hit up the sourceforge archive sources, decompile the last lr5 beta paddy, go through the old forum, find users who might have touched the sources, etc. Lots of legwork.

There will be no more fixes for this. I tried but did not upgrade to use this LR CC 2015.x version. I have used LR4, then LR5. Stayed with LR5. Used some home brewed solutions alongside Paddy. Maybe LR Classic CC. TBD.

I might do a full rewrite, focusing only on keyboard support. So it can be used alongside solutions like MIDI2LR. Or when traveling light without a midi device. And target only LR Classic CC. Maybe. TBD. 

 
