Introduction
------------

This is the source tarball of Sakis3G script. While granted the
the "script" title, it actually cheats big time. Scope of Sakis3G
is to finally provide a single self-contained shell script to end
user, capable to connect him/her through 3G/UMTS/GPRS. Thus, the
"script" title.

Official site: http://www.sakis3g.org/


License
-------

This program is free software; you can redistribute it and/or 
modify it under the terms of the GNU General Public License as 
published by the Free Software Foundation; either version 2 of 
the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, 
but WITHOUT ANY WARRANTY; without even the implied warranty of 
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the 
GNU General Public License for more details:

    http://www.gnu.org/licenses/gpl.txt

Above statement includes additional charges you may receive from 
your operator by using this program, defects to your SIM card 
including but not limited to being PIN blocked, defects on your 
hardware, 3G service abuse ban etc. USE WITH CARE. Author of this
program or authors of any of its dependencies have no responsibi-
lity for what may happen to you.

Author is not related in any way with any of the companies, being 
operators or modem manufacturers, other than being a customer to 
some of them. Logos and trademarks mentioned by this package 
belong to their respective owners.

This program, in order to remain as self-contained as possible,
includes original source packages of some of its dependencies. 
You should consult their respective COPYING and README files to 
identify terms under which they are redistributed by Sakis3G.


Scope
-----

Scope of this work is to provide an as small as possible single
file which could enable a user to use his 3G USB modem. It does
not, in anyway, attempt to be a complete replacement to fully
featured solutions or distribution specific methodologies, used
for utilizing such devices. Instead, it is supposed to provide:

  - An as small as possible solution to those unlucky enough
    to have no internet connection, other than their 3G USB
    modem. They can use this script to initially bring their
    connection up, and then install all required software.
  - An alternative solution when anything else has failed.
  - A small footprint solution for environments and distri-
    butions that need to keep their profile low.


Package Contents
----------------

This package contains Sakis3G sources, along with:
  - Unmodified Usb-ModeSwitch sources.
  - Modified Usb-ModeSwitch device database.

You can replace contents of their respective directories with
more recent -suitable- versions, as long as you mention version
and origin of your own supplied versions wherever/whenever you
redistribute Sakis3G, either "compiled" or in "source" form and
as long as you respect license requirements of Sakis3G and any
one of its dependencies mentioned above.


Compile
-------

Required dependencies: libusb-dev, ppp

Ubuntu requires additional steps:
1. Install libusb-1.0-0-dev
2a. Change `#include <libusb.h>` in dependencies/usb-modeswitch.h 
to `#include <libusb-1.0/libusb.h>` 
or
2b. `cp /usr/include/libusb-1.0/libusb.h /usr/include`

Now clone the repo using git

`git clone https://github.com/Trixarian/sakis3g-source.git`

Then change to directory when the repo downloaded

`cd sakis3g-source`

Then compile Sakis3G

`./compile`

Then copy the compiled file to your bin folder

`sudo cp build/sakis3gz /usr/bin/sakis3g`
