Mobile Icon Generating Tools
============================

These are some bash scripts to automate the generating of PNG and Vector
Drawable icons for mobile apps from an SVG source file.

Dependencies
------------

* macOS or Linux (untested on Windows Subsystem for Linux)
* [Inkscape](https://inkscape.org/)
* [ImageMagick](https://imagemagick.org/)
* [pngquant](https://pngquant.org/)
* [zopflipng](https://github.com/google/zopfli)
* [libxml2](https://gitlab.gnome.org/GNOME/libxml2)
* [npm](https://npmjs.org/)
* [Java](https://openjdk.org/)

Most of these packages can be installed using the system package manager on
Linux, or package managers such as Homebrew or MacPorts on macOS.

`iconize`
---------

Usage: `iconize [-d] [-b COLOR] [--force-bg] INPUTFILE [OUTPUTDIR]`

This tool generates app icons for iOS and Android apps from the SVG file given
in `INPUTFILE`. It is expected that the input file is an SVG with a canvas size
of 192×192 with a transparent background. A solid background colour can be
added to the output via the `--background`/`-b` option.

If `OUTPUTDIR` is not specified, it defaults to a folder named 'out' in the
current directory.

By default, it will generate a single 1024⨉1024 PNG icon for iOS, as supported
by recent versions of Xcode. The option `--ios-old` can be specified to
generate all the icon sizes needed for older versions.

Likewise, for Android it will attempt to convert the SVG into an Android Vector
Drawable. This behaviour can be disabled with `--no-vector`, and PNG images for
older versions can be generated using `--android-old`.

Generation of iOS or Android icons can be disabled with `--no-ios` and
`--no-android` respectively.

Partial support for web favicons can be enabled with the `--web` option.


`notify-iconize`
----------------

Usage: `notify-iconize [INPUTFILE]`

This tool generates Android notification icons from the SVG file given in
`INPUTFILE`. It is expected that the input file is an SVG with a square canvas
size and a transparent background.

In theory, this script works on both macOS and Linux. It is much less tested
than the `iconize` script.


Contributing
------------

Contributions of bug reports, feature requests, and pull requests are greatly
appreciated!

Please note that this project is released with a [Contributor Code of
Conduct](CODE_OF_CONDUCT.md). By participating in this project you agree to
abide by its terms.


Licence
-------

Released under the [MIT Licence](LICENCE).

Copyright © 2018 – 2023 Ayogo Health Inc.

