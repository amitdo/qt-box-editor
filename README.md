QT Box Editor
=============

Project homepage: [https://github.com/zdenop/qt-box-editor](https://github.com/zdenop/qt-box-editor)

Project description: [https://zdenop.github.io/qt-box-editor/](https://zdenop.github.io/qt-box-editor/)

Screenshots: [wiki](https://github.com/zdenop/qt-box-editor/wiki)

Download current (devel) source: [tar.gz](https://github.com/zdenop/qt-box-editor/tarball/master) or [zip](https://github.com/zdenop/qt-box-editor/zipball/master).

The latest released source is [qt-box-editor-v1.13](https://github.com/zdenop/qt-box-editor/tarball/master/tree/v1.13).

Download [win32 binary build](http://sourceforge.net/projects/qtboxeditor/?source=dlp) from [sourceforge.net](http://sourceforge.net/projects/qtboxeditor/)

Licence: [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)


DESCRIPTION
-----------

QT Box Editor is tool for adjusting [tesseract-ocr](https://github.com/tesseract-ocr/tesseract) v3 (a.k.a Legacy engine) box files. Aim of this project is to provide easy and efficient way for editing regardless file size.
**It is useless for training tesseract v4 and above (LSTM engine).**

Release information can be found in CHANGELOG file. Code and artwork contribution is welcomed.

QT box editor is a successor of [tesseract-gui project](https://github.com/mk219533/tesseract-gui) that is not developed anymore. Name of application was changed due to name collision with project http://tesseract-gui.sourceforge.net.


LICENSE
-------

License was changed from "THE BEER-WARE LICENSE" to ["Apache License, Version 2.0"](http://www.apache.org/licenses/LICENSE-2.0) based on agreement with Marcel Kołodziejczyk ([original author](https://github.com/mk219533/tesseract-gui)). Anyway you are welcome to buy him a free beer if you meet him. He deserves it.

[Faenza Icons](http://tiheum.deviantart.com/art/Faenza-Icons-173323228) are under GNU/GPL license.
[Tango Icons](http://tango.freedesktop.org/) are Public Domain.

ARTWORK
-------

These icons are Faenza Icons:
    exit.png
    filesave.png
    fileopen.png
    gtk-jump-to-ltr.png
    help-about.png
    next.png
    previous.png
    text_bold.png
    text_italic.png
    text_under.png
    window-close.png
    zoom-in.png
    zoom-fit.png
    zoom-original.png
    zoom-out.png
    zoom-selection.png (is modified zoom-fit.png)

import.svg is modified icon of Faenza fileopen icon.

joinRow.svg and splitRow.svg are adapted icons of lmproulx icons [Convergent](http://www.openclipart.org/detail/convergent-by-lmproulx) and [Divergent](http://www.openclipart.org/detail/divergent-by-lmproulx)

gnome-edit-find.svg is from [Wikipedia](http://en.wikipedia.org/wiki/File:Gnome-edit-find.svg).

Other icons/artwork were created for Qt Box Editor and they are released under Apache License, Version 2.0.


Distribution
------------

See [release page](https://github.com/zdenop/qt-box-editor/releases)



Instalation
-----------

Requirements: QT5, tesseract & leptonica and (optionally) cmake.

For building you can use `qmake-qt5` or `cmake`

For cmake build you will need to compile&install tesseract by cmake otherwise cmake relevant files (e.g. ` tesseractConfig.cmake`) will not be created and installed.

## cmake windows build

`<your_QT5_path>` could be e.g. `f:/Qt/5.15.2/msvc2019_64`
`<your_tesseract_installation>` could be e.g. `f:/win64`

```sh
set QTDIR=<your_QT5_path>
set PATH=%QTDIR%/bin;%PATH%
cmake -G "Visual Studio 16 2019" -A x64 -S . -B build -DCMAKE_PREFIX_PATH="<your_QT5_path>;<your_tesseract_installation>"
cmake --build build --config Release --verbose
```

The Output will be at build\Release\qt-box-editor-1.13.0.exe

## cmake linux build

```sh
cmake -B build
make
```

## qmake linux build

```sh
qmake-qt5
make
```