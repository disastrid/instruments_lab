---
layout: research
title:  "TouchKeys"
tag: "augmented-	instruments"
tagline: Expressive multi-touch sensing on the piano keyboard.
thumb: touchkeys/tk-thumb.jpg
authors: "Andrew McPherson"
main-image: /images/research/touchkeys/tk-cover.jpg
production-date: 2011 - present
para: TouchKeys adds capacitive multi-touch sensing to the surface of the piano keys.  
links: ["http://touchkeys.co.uk", "https://www.kickstarter.com/projects/instrumentslab/touchkeys-multi-touch-musical-keyboard", "http://youtube.com/user/apm414/videos"]
link-names: ["TouchKeys.co.uk", "Kickstarter campaign", "YouTube channel"]
---

{% include youtube.html youtube="fNxacJZXPic" %}

TouchKeys is a new musical instrument transforming the piano-style keyboard into an expressive multi-touch control surface. The TouchKeys sensors can be added to the surface of any keyboard, using capacitive touch sensing to measure the location of the musician's fingers on the keys during performance.

The project was launched on the crowd-funding website [Kickstarter](https://www.kickstarter.com/projects/instrumentslab/touchkeys-multi-touch-musical-keyboard) on 29 July 2013 and successfully finished its campaign on 2 September 2013. The campaign raised funding to build sets of TouchKeys that any musician can install on their own keyboard. They shipped by the end of January 2014, and a second production run completed in 2015. In 2016, the project spun out into an independent company, [TouchKeys Instruments Ltd](http://touchkeys.co.uk), which sells kits and instruments to musicians worldwide.

## How it Works

{% include youtube.html youtube="BmRYuDOzTqU" %}

TouchKeys adds capacitive multi-touch sensing to the surface of any piano-style keyboard. Sensor overlays measure the location and contact area of the player's fingers on the key surfaces, and the data can be used to create a wide range of expressive effects including vibrato, pitch bends, timbre changes and improved emulations of non-keyboard instruments. The keyboard is traditionally a discrete interface, measuring notes by onset and release. The TouchKeys let the player continuously shape each note through the subtle expressive details of their finger motion.

{% include single-image-research.html fileName="touchkeys/touchkeys_finger_simulation.png" %}
{% include single-image-research.html fileName="touchkeys/touchkeys_graph_simulation.png" caption="Simulation of touch location calculation in a single axis" %}

The sensors work by measuring the capacitance of a collection of small conductive pads on the surface. Touching the key causes several adjacent pads to increase in capacitance. A microcontroller on the key interpolates between the values to arrive at a precise estimate of the contact location. Contact area can be sensed by observing the overall magnitude of change in capacitance.

Once each key has calculated its touch information, another microcontroller collects the data from every key and transmits it to a computer by USB. Software on the computer side generates OSC and MIDI messages that can be used by a wide variety of synthesis software. The software also uses the MIDI data from the underlying keyboard to produce a complete picture of the performer's actions.

More information on the design and operation of the TouchKeys can be found in the papers below:

A. McPherson and Y. Kim. [Design and applications of a multi-touch musical keyboard](http://smcnetwork.org/system/files/smc2011_submission_80.pdf). Proc. Sound and Music Computing, Padova, Italy, 2011.

A. McPherson. [TouchKeys: capacitive multi-touch sensing on a physical keyboard](http://www.eecs.umich.edu/nime2012/Proceedings/papers/195_Final_Manuscript.pdf). Proc. New Interfaces for Musical Expression, Ann Arbor, MI, USA, 2012.

C. Heinrichs and A. McPherson. [A hybrid keyboard-guitar interface using capacitive touch sensing and physical modeling](http://www.smcnetwork.org/system/files/smc2012-176.pdf). Proc. Sound and Music Computing, Copenhagen, Denmark, 2012.

A. McPherson, A. Gierakowski and A. Stark. [The space between the notes: adding expressive pitch control to the piano keyboard](http://dl.acm.org/authorize?6813830). Proc. ACM Conference on Human Factors in Computing Systems (CHI), Paris, France, 2013.

A. McPherson. [Buttons, handles, and keys: advances in continuous-control keyboard instruments](http://www.mitpressjournals.org/doi/pdf/10.1162/COMJ_a_00297). Computer Music Journal 29(2), 2015.

## Features

{% include single-image-research.html fileName="touchkeys/touchkeys_classic_with_logo.jpg" %}

The TouchKeys are sensor overlays that attach to any standard-size keyboard, acoustic or electronic. Each key uses capacitive touch sensing to precisely locate one or more fingers on the key surface. Here are a few of the main features:

* High-resolution position measurement with over 1500 points of resolution in the long axis, 256 points in the narrow axis. That's sub-millimeter accuracy!
* XY position on every key, including the black keys. (The narrow part of the white keys senses on the long axis only.)
* Contact area measurement distinguishes the tip and the pad of the finger, and can indicate finger pressure in some circumstances.
* Up to 3 touches per key allows new multi-finger techniques on the keyboard.
* 200Hz sample rate makes for a natural, low-latency interaction.
* Configurable keyboard size: the sensors can install on anything from a 2-octave portable keyboard to a 97-key Boesendorfer Imperial Grand piano.
* OSC and MIDI support for a wide range of mappings from touch data to sound.

## Videos

During the [Kickstarter campaign](https://www.kickstarter.com/projects/instrumentslab/touchkeys-multi-touch-musical-keyboard), we created over 10 videos demonstrating different applications of TouchKeys which are available on the [YouTube channel](http://youtube.com/user/apm414/videos). Here is a selection of those videos:

{% include youtube.html youtube="bIkKMHwXcko" %}
{% include youtube.html youtube="InNZkNz4NMc" %}
{% include youtube.html youtube="jt8Eb0ZalWQ" %}

## TouchKeys in the Press

During the Kickstarter campaign and its subsequent [commercial launch](http://touchkeys.co.uk), TouchKeys was the subject of over 25 press articles. A full list can be found [here](http://touchkeys.co.uk/press/); a selection is below:

* Synthtopia: [TouchKeys creator Andrew McPherson on bringing new expression To musical keyboards](http://www.synthtopia.com/content/2016/12/09/touchkeys-creator-andrew-mcpherson-on-bringing-new-expression-to-musical-keyboards/)
* Sound on Sound: [Touch Sensitive: the TouchKeys Project](http://www.soundonsound.com/people/touchkeys-project)
* Create Digital Music: [Multi-touch with your current keyboard, and how expressive, crowd-funded keys stack up](http://cdm.link/2013/08/the-latest-multitouch-expressive-idea-use-your-current-keyboard/)
* Time: What if your piano’s keys supported multitouch and gesture control?
* New Scientist: [Sensitive piano keys let pianists create new sounds](https://www.newscientist.com/article/dn23819-sensitive-piano-keys-let-pianists-create-new-sounds.html)
* Hackaday: [Touch control for every key on the keyboard](http://hackaday.com/2013/07/30/touch-control-for-every-key-on-the-keyboard/)
* Popular Science: [Why hasn’t there been a multitouch piano before now?](http://www.popsci.com/technology/article/2013-07/why-hasnt-there-been-multitouch-piano-now?src=SOC&dom=tw)
