Deepify
=======

Copyright (C) 2016  F. Brezo and Y. Rubio, i3visio

[![Version in PyPI](https://img.shields.io/pypi/v/deepify.svg)]()
[![Downloads/Month in PyPI](https://img.shields.io/pypi/dm/deepify.svg)]()
[![License](https://img.shields.io/badge/license-GNU%20General%20Public%20License%20Version%203%20or%20Later-blue.svg)]()

1 - Description
---------------

Deepify is a GPLv3+ set of libraries developed by i3visio to perform Open Source Intelligence tasks in some part of the internet that are not as easy to access as the conventional part of the web.

2 - License: GPLv3+
-------------------

This is free software, and you are welcome to redistribute it under certain conditions.

	This program is free software: you can redistribute it and/or modify
	it under the terms of the GNU General Public License as published by
	the Free Software Foundation, either version 3 of the License, or
	(at your option) any later version.

	This program is distributed in the hope that it will be useful,
	but WITHOUT ANY WARRANTY; without even the implied warranty of
	MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
	GNU General Public License for more details.

	You should have received a copy of the GNU General Public License
	along with this program.  If not, see <http://www.gnu.org/licenses/>.


For more details on this issue, check the [COPYING](COPYING) file.

3 - Installation
----------------

Fast way to do it on any system:
```
pip install deepify
```
Under MacOS or Linux systems, you may need to do this as superuser:
```
sudo pip install deepify
```
This will manage all the dependencies for you.

If you needed further information, check the [INSTALL.md](INSTALL.md) file.

4 - Basic usage
---------------

If everything went correctly (we hope so!), it's time for trying deepify. But first, you will need to start the Tor Bundle downloadable from `http://torproject.org`. Execution examples:
```
# Check that you have the Tor Browser running and that the options in ~/.config/Deepify folder are correct
onionGet.py -u "http://3g2upl4pq6kufc4m.onion/"
# Check that you have the Zeronet running and that the options in ~/.config/Deepify folder are correct
zeronetGet.py -u "1HeLLo4uzjaLetFx6NH3PMwFP3qbRbTf3D"
```

Type -h or --help to get more information about which are the parameters of the application.

You can use the functions as a library for collecting information from Tor:
```
# Check that you have the Tor Browser running and that the options in ~/.config/Deepify folder are correct
from deepify.tor import Tor
url = "http://3g2upl4pq6kufc4m.onion/"
# Creating the wrapper instance
torwrapper = Tor()
data = torwrapper.getResponse(url)
print data
```
You can also check it in Zeronet:
```
# Check that you have the Zeronet service running and that the options in ~/.config/Deepify folder are correct
from deepify.zeronet import Zeronet
url = "1HeLLo4uzjaLetFx6NH3PMwFP3qbRbTf3D"
# Creating the wrapper instance
zeronetwrapper = Zeronet()
data = zeronetwrapper.getResponse(url)
print data
```

5 - HACKING
-----------

If you want to extend the functionalities of Deepify and you do not know where to start from, check the [HACKING.md](HACKING.md) file.

6 - AUTHORS
-----------

More details about the authors in the [AUTHORS.md](AUTHORS.md) file.
