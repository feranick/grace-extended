This repository provides patches for the  popular 2D plotting program xmgrace. 
While upstream development appears to have slowed or stopped, many improvements are still marked in 
upstream bug reports.

These builds provide the following improvements over the stock version in Linux/MacPorts 
repos:

1. Default print resolution for all printing devices have been bumped to 300 dpi (from 
72dpi).

2. The vertical toolbar has been extended to include buttons for common operations such as: 
ASCII import and export, Print settings, Objects, and other data manipulation functions.

3. Pointer coordinates: under the Window menu, the new function allows the user to click 
over the plot to get the coordinates of the points in the external console.

4. Resized the default width of the xmgrace window (HighRes: 1200; LowRes: 1000).

5. New Library of non-linear fitting functions is now included in Debian unstable/testing 
and in the official version of grace in Maverick.

In addition:

1.    Instantaneous Updating 

This patch adds instantaneous updating to the major widgets. Only the feature changed gets updated. This means that, for example, the line colour of a set is changed when you select the colour, NOT when you press apply.

    Why is this so great?
        Well, say I have a bunch of sets for which I selected all the line styles, symbols and colours. Now I want to change the width of all of them Traditionally, this would have meant that I would have to go through and do every set individually. Now, I can select all the sets and ONLY the line width wll get changed when I select a new line width. Imagine this with graphs, axes, etc.
        I can see the result right away. I do not have to leave the widget and hit the apply button.
        every modern program works like this

    There is a new X resource to control this. By default it is on, but if you want the old behavior, put the following line in your ~/.Xresources or ~/.Xdefaults file:

    XMgrace*InstantUpdate: false

2. Independent major and minor tic directions

3. A Set Locator Fixed Point button has been added to the locater menu.

4. PDFs, JPGs and PNGs can be cropped to the minimum bounding box: use the "Tight BBox" device option from the GUI. The 3 devices now also have the options to control this, like EPS: bbox:tight bbox:page

5. Set comments can be read from a file, one per line, from Edit/Data sets.../Edit/Read set comments

6. Offsets can be applied to Titles and Subtitles to finely control vertical placement

7. Project description added to the Plot window

8. autoscale added to the set menu

9. file with legend captions can now be added on command line 

Additional system-level patches (available in a single patch or as individual patches):

1. grace-opt-flags_5.1.25-3: Added compiling optimization flags for better performance

2. grace-allow-Xresource Allow display overrides via ~/.Xresources

3. grace-font-extension-t1 Search for .t1 as a font file extension, in addition to .pfa/.pfb
 .t1 is now seen as a file extension, in addition to the classic .pfa and
 .pfb extensions, particularly in fonts-urw-base35; search for .t1 as well.


Comments, suggestions for future additions: Nicola Ferralis <feranick@hotmail.com>
