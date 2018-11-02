Ayogo Image Tools
=================

<small>Copyright 2018 Ayogo Health Inc.</small>

Set Up
------

If you're on Mac, you will need to do the following:

1. Go to https://inkscape.org/en/~su_v/galleries/osxmenu-r12922/ and install the GTK2 version of Inkscape.
2. `brew install pngquant`
3. `brew install zopfli`

`iconize`
---------

Usage: `iconize [-d] [-b COLOR] INPUTFILE [OUTPUTDIR]`

This tool generates app icons for iOS and Android apps from the SVG file given in `INPUTFILE`. It is expected that the input file is an SVG with a canvas size of 192×192 with a transparent background. A solid background colour can be added to the output via the `--background`/`-b` option.

If `OUTPUTDIR` is not specified, it defaults to a folder named 'out' in the current directory.

In theory, this script works on both macOS and Linux.
