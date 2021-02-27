The Tk color picker a bit changed.


The changes to *tk_chooseColor* are the following:

1. The resizing of window is locked (supposedly the resizing makes no sense,
   at least in the current version of *tk_chooseColor*).

2. The sizes of Tk color picker are changed for more usability.

3. The 'Move all' checkbox is added allowing to move all (R, G, B) selectors
   simultaneously.

4. The 'Tone moves' checkbox is added allowing to implement the toning feature
   for a current color.

5. The RGBCMY and their tones are added, in separate color boxes.

6. The *-moveall* (0 by defauls) and *-tonemoves* (1 by default) options are added.

7. The chooser is themed now.

8. A stand-alone Tk color chooser *tkclr.tcl* is available.

9. A *aloupe* package may be called to pick a color from the screen loupe.

To use *clrpick.tcl*, copy it into the Tk directory (replacing the old version).

A stand-alone Tk color chooser is invoked as:

 `tclsh tkclr.tcl ?color?`

If the color argument is omitted, the chooser tries to take a color from the clipboard. Also, it provides two buttons allowing to get/put a color from/to the clipboard. Well fit when the chooser is 'topmost' above other windows.

Further details:
 https://aplsimple.github.io/en/tcl/tkcc
