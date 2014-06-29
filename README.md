EEGBliss
========

EEGBliss: Open source API for controlling computers with Blissymbolics and EEG (Python + Kivy)

Current version: 0.0.1 Alpha for Windows


Dependencies
========

* [Emotiv SDK](http://emotiv.com/)
* [Python 2.7.7 32bit](https://www.python.org/)
* [Kivy 1.8.0 32bit](https://www.python.org/)
* [PyEmotiv](https://github.com/dplass/PyEpoc)

Installation
============

After you have installed the Emotiv SDK, Python and Kivy, you need to place the 

First you need to download the wrapper PyEpoc from:
[https://raw.githubusercontent.com/dplass/PyEpoc/master/PyEpoc.py](https://raw.githubusercontent.com/dplass/PyEpoc/master/PyEpoc.py)

And place it in the /dll/32 bit folder of your Emotiv SDK installation.

Example:

![path to /dll/32 bit folder](http://turbolego.com/EEGBliss_github1.png)

Next, add the dll folder to your Environmental Variables by right-clicking “My computer”, select “properties”, then “advanced” and then “Enviroment variables”.

Select the “Path” variable under “system variables”, then click the “Edit…” button and add the path to your dll folder in the Emotiv SDK.

For example:

;C:/Program Files (x86)/Emotiv Research Edition SDK v2.0.0.20/dll

![adding dll folder to enviromental variables](http://turbolego.com/EEGBliss_github2.png)



Authors
=======
TurboDevs AS and Larsen Development.

Tobias Andersen, Sigve Larsen, Nine Bauge, Jan Ole Lysen Andersen, Emilie Thomassen, Raymond Holthe.
