Electrum-raven - Lightweight Ravencoin client
=====================================

::

  Licence: MIT Licence
  Author: Thomas Voegtlin
  Port Maintainer: traysi@github (Electrum-raven)
  Language: Python (>= 3.6)
  Homepage: https://ravencoin.org/


.. image:: https://minermore.com/images/ravencoin.svg
    :width: 100px
    :target: https://github.com/traysi/electrum-raven
    :alt: Build Status


Getting started
===============

Electrum-raven is a pure python application. If you want to use the Qt interface, install the Qt dependencies::

    sudo apt-get install python3-pyqt5

If you downloaded the official package (tar.gz), you can run Electrum-raven from its root directory, without installing it on your system; all the python dependencies are included in the 'packages' directory. To run Electrum-raven from its root directory, just do::

    ./run_electrum

You can also install Electrum-raven on your system, by running these commands::

```cd ~
virtualenv -p /usr/local/bin/python3.7 pve
source ~/pve/bin/activate
git clone https://github.com/traysi/electrum-raven
cd electrum-raven
pip3 install https://github.com/traysi/x16r_hash/releases/download/1.0/1.0.zip
python3 -m pip install .[fast]
pyrcc5 icons.qrc -o electrum/gui/qt/icons_rc.py
pip3 install pyqt5
./run_electrum
```

Creating Binaries
=================

To create binaries, create the 'packages' directory::

    ./contrib/make_packages

This directory contains the python dependencies used by Electrum-raven.

Mac OS X / macOS
--------

See `contrib/build-osx/`.

Windows
-------

See `contrib/build-wine/`.


Android
-------

See `electrum/gui/kivy/Readme.md` file.
