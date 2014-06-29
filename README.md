EEGBliss
========

EEGBliss: Open source API for controlling computers with Blissymbolics and EEG (Python + Kivy)

Current version: Prototype 0.0.1 Alpha for Windows


Dependencies
========

* [Emotiv SDK](http://emotiv.com/)
* [Python 2.7.7 32bit](https://www.python.org/)
* [Kivy 1.8.0 32bit](https://www.python.org/)
* [PyEmotiv](https://github.com/dplass/PyEpoc)

Installation
============

After you have installed the Emotiv SDK, Python and Kivy, download the wrapper PyEpoc from:
[https://raw.githubusercontent.com/dplass/PyEpoc/master/PyEpoc.py](https://raw.githubusercontent.com/dplass/PyEpoc/master/PyEpoc.py)

And place it in the /dll/32 bit folder of your Emotiv SDK installation.

Place the files "EGGBliss_prototype.py", "pluss.png" and "minus.png" in this folder too.

Example:

![path to /dll/32 bit folder](http://turbolego.com/EEGBliss_github1.png)

Next, add the dll folder to your Environmental Variables by right-clicking “My computer”, select “properties”, then “advanced” and then “Enviroment variables”.

Select the “Path” variable under “system variables”, then click the “Edit…” button and add the path to your dll folder in the Emotiv SDK.

For example:

```;C:/Program Files (x86)/Emotiv Research Edition SDK v2.0.0.20/dll```

![adding dll folder to enviromental variables](http://turbolego.com/EEGBliss_github2.png)

Next, you need to do one edit to the prototype sourcecode to select if you want to use the EmoComposer program or the EPOC Control Panel with the EPOC EEG headset.
EmoComposer uses the port 1726 while EPOC Control Panel uses port 3008.

To use EmoComposer, comment line 39 like so:

```EmotivEngine.EE_EngineRemoteConnect ( '127.0.0.1', 1726 )```

```#EmotivEngine.EE_EngineRemoteConnect ( '127.0.0.1', 3008 )```

To use EPOC control panel, comment line 39 like so:

```EmotivEngine.EE_EngineRemoteConnect ( '127.0.0.1', 1726 )```

```#EmotivEngine.EE_EngineRemoteConnect ( '127.0.0.1', 3008 )```

That's it!


Using the prototype
============

Because we have used the cognitive states for "lift" and "drop" in the Emotiv SDK while testing our concept, these slots are the ones you should use when you train the blissymbols for "yes" and "no" prior to using this prototype.
You can add more states or replace the states we have used in the source.

To use the prototype with EPOC Control Panel, you need to start the control panel first, and then run EGGBliss_prototype.py.

If you have already trained cognitive thoughts for the blissymbol "yes" and saved them to the state "lift" in EPOC Control Panel, the prototype should activate the "+" Blissymbol whenever you think about it.

![Thinking about the blissymbol for yes](http://turbolego.com/EEGBliss_github3.png)

If you have already trained cognitive thoughts for the blissymbol "no" and saved them to the state "drop" in EPOC Control Panel, the prototype should activate the "-" Blissymbol whenever you think about it.

![Thinking about the blissymbol for yes](http://turbolego.com/EEGBliss_github3.png)


Authors
=======
TurboDevs AS and Larsen Development.

Tobias Andersen, Sigve Larsen, Nine Bauge, Jan Ole Lysen Andersen, Emilie Thomassen, Raymond Holthe.
