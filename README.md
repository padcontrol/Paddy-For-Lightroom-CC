## Paddy for Lightroom CC 

### note: specifically Lightroom 6 CC 2015, not LR6 standalone, not LR CC Classic (v7)

A friend asked for help with making Paddy work with Lightroom CC (v6, 2015.x).  I wanted to try out LRCC (had been staying with LR5), so why not.

Went spaghetti code diving and patched up the last Paddy 5.x  beta release to make it work sufficiently for his and my test purposes. 

Paddy was an admirable effort. Author "dorfl" had stated he was not a programmer. And the code echoed the statement. Inconsistent naming, mixture of repeated functions and inline, adding strings of text with numbers expecting numbers, all globals, etcetera. And unnecessarily complicated indirection layers.  It's easy to be distracted with new features, and it shows in the code. New features over bug fixes.  But it sorta worked. Author "dorfl" has moved on per the Paddy site. But it was CC BSD licensed, so we're going to have a crack at making it work.

Use at your own risk.  Attempt only for Lightroom CC 2015.13 (latest update as of October 2017)

You should already have Paddy working in LR5. And it should only be complaining and exiting on LR CC startup.

This should be looked as a hack, on a hack (Paddy LR5 beta), on a runaway complication (Paddy LR4), on a well intended plan (Paddy LR3). That is, no, I did not try to refactor or tidy it up. Not worth the time. Not releasing an installer, or an easy binary. 

Putting this out because it may help others. Making it difficult because you must really want it.

So if you want changes and features made, by all means, attempt it, go code spelunking yourself.  But looks like no one had the mettle to do so the last two+ years. Understandably. It's easier to contribute a meatball than to understand the spaghetti.  If you want to have a crack at this yourself, hit up the sourceforge archive sources, decompile the last lr5 beta paddy, go through the old forum, find users who might have touched the sources, etc. Lots of legwork.

This will not be supported further. I tried but did not upgrade to use this LR CC 2015.x version. I have used LR4, then LR5. Stayed with LR5. Used some home brewed solutions alongside Paddy. Maybe LR Classic CC. TBD.

I might full rewrite chunks, focusing only on keyboard support. So it can be used alongside solutions like MIDI2LR. Or when traveling light. And target only LR Classic CC. Maybe. TBD. 

 
