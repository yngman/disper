See [the Wiki](https://github.com/yngman/disper/wiki) for how-to fix it, or below for
[Patched and Pushed](#patched-and-pushed) as well as [Ubuntu Instructions](#ubuntu-instructions) for installing on Ubuntu.

# Disper

Disper is an on-the-fly display switch utility. It is intended to be used just
before giving a presentation with a laptop, when all one wants is that the
beamer, which has just been connected, is able to show whatever you prepared.

Disper gives you the option to either clone the all detected displays, or
extend the desktop to them. Resolutions are automatically detected. For
cloning, the highest resolution supported by all displays devices is chosen;
for extending every display device gets its highest supported resolution.
For special setups requiring more detailed control, one can still use the
standard display configuration utilites.

At the moment nVidia cards have the best support. XRandR is working, though
import/export is not complete. Contributions are welcome in this area.

Generally, one would bind 'disper -c' to a shortcut key (or if you rather
like to extend your desktop, use 'disper -e'). Without an external display
or beamer connected, you'll get your laptop's full resolution; when an external
display is present, it switches to clone mode after the keypress (or extend, if
you configured it that way).

In the future a graphical user interface may be added. For now I hope that it'll
save you some time at the beginning of presentations.

The initial development of this program was supported Frans and Linda
Reijnhoudt. A big thanks to them!

http://willem.engen.nl/projects/disper/

- Willem van Engen <dev-disper@willem.engen.nl>

# Orphan and Forked

As of 2018 (seems 2013), this poor package has seemed to lost an owner,
and an undefined return value for a ctypes function made all calls fail on most
current architectures.

But since otherwise it still works and is healthy, the package is patched and available
for all to enjoy.

- Alex Peyser <peyser.alex.public@gmail.com>

# Patched and Pushed

The source (Git version) of the Ubuntu package (Debian upstream) is here:

<https://salsa.debian.org/python-team/applications/disper>

That version segfaults, however. This is due to lack of maintenance (as noted above).

This repository is *just a merge* of the Debian upstream with the AUR packaged at:

<https://github.com/apeyser/disper>

See discussion on AUR, <https://aur.archlinux.org/packages/disper/>

- Gunnar Yngman <gunnar.yngman@farmbio.uu.se>

## Ubuntu Instructions

Uninstall the Ubuntu package (if you had that installed),

~~~bash
sudo apt purge disper
~~~

Clone this repo,

~~~bash
git clone https://github.com/yngman/disper.git
~~~

Make and install,

~~~bash
cd disper
make clean
make all
sudo make install
~~~

Yeah, that's all that is required. For me at least.
