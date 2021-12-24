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

6. Add buttons in Eval data for quick evaluation of basic formula.

Additional system-level patches (available in a single patch or as individual patches):

1. grace-opt-flags_5.1.25-3: Added compiling optimization flags for better performance

2. grace-allow-Xresource Allow display overrides via ~/.Xresources

3. grace-font-extension-t1 Search for .t1 as a font file extension, in addition to .pfa/.pfb
 .t1 is now seen as a file extension, in addition to the classic .pfa and
 .pfb extensions, particularly in fonts-urw-base35; search for .t1 as well.


Comments, suggestions for future additions: Nicola Ferralis <feranick@hotmail.com>
