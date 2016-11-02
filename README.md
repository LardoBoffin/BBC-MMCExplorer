# TurboMMC Explorer

TurboMMC explorer - this is a BBC Basic program which allows the selection of discs in a TurboMMC (and possibly others) system on a BBC Model B. Once selected you can then view the file list for the disc. In essence this program is designed to remove the need to use *DCAT, *DIN and *CAT so often to see what it on a disc.

The main reason for writing this is to give me something to work with to get to grips with assembly language. I will be re-writing the slow parts of this program in assembly as and when time permits. 

I don't have any other hardware (e.g. other MMC system or a BBC Master etc.) to test with but I suspect that it won't work on a Master due to the fact that it gets data directly from system memory to build the disc lists etc.

This also won't run across the Tube due to the direct memory access. 

Current issues: -

 . Slow
 . Doesn't have the ability to boot a disc once selected (although I am looking into this)
 . Doesn't have the ability to load / run a file once selected (as above)
 . Forgets which disc you were looking at when it is closed (I am thinking of getting it to store some settings in disc 510)
 . Won't work over the Tube as it directly accesses the main memory to get the disc info (not sure about this one)
 . Is a bit flaky when you press Escape - I have implemented JGHarstons excellent PROC / FN error handling code (viewtopic.php?f=2&t=11973#p151694), but not fully I suspect, so when you press Esc in the wrong place it freezes and needs a subtle application of the Break key to get it going again
 
Usage is pretty simple - run it and press a key to get past the help screen (press H at any time to toggle back to this).
Use the up and down arrows to select a disc - keep scrolling down to see more discs.
Press D and then type in a disc number - the discs from that number onwards will be listed.
Press tab to see the files on the selected disc and then use the arrow keys to scroll the files.
Press tab to go back to the disc list.

If there are gaps between the disc numbers this is hopefully down to the discs not being formatted!
