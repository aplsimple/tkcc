The Tk color picker a bit changed.


The changes to *tk_chooseColor* are the following:

1. The resizing of window is locked (supposedly the resizing makes no sense,
   at least in the current version of *tk_chooseColor*).

2. The default sizes of Tcl/Tk color picker are changed a little for more usability.

3. The 'Move all' checkbox is added allowing to move all (R, G, B) selectors
   simultaneously.

4. At moving selectors, the current color is toned accordingly.

5. The RGBCMY and their tones are added, in separate color boxes.

6. The *-moveall* (0 by defauls) option is added, to move all picker's selectors.

7. The *-geometry* option is added, in two forms: +X+Y (coordinates) or pointer+X+Y (shift from the mouse pointer).

8. The chooser is themed now.

9. The *Loupe* button allows to pick a color from the screen loupe if *aloupe* package is loaded.

10. A reverse color is shown in the color display. After clicking the display, a new reverse color is displayed, just to select the best one.

11. ::tk::dialog::color::GetOptions is used to get main options ("bg", "-moveall", "fg") after calling tk_chooseColor.

12. A stand-alone Tk color chooser *tkclr.tcl* is available.

To use *clrpick.tcl*, copy it into the Tk directory (replacing the old version).

A stand-alone Tk color chooser is invoked as:

 `tclsh tkclr.tcl ?-moveall 1? ?-initialcolor color?`

If the color argument is omitted, the chooser tries to take a color from the clipboard. Also, it provides two buttons allowing to get/put a color from/to the clipboard. Well fit when the chooser is topmost above other windows.

Further details:
 https://aplsimple.github.io/en/tcl/tkcc
