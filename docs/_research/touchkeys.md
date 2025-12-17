---
layout: research
title:  "TouchKeys"
tag: "augmented-instruments"
tagline: Expressive multi-touch sensing on the piano keyboard.
thumb: touchkeys/tk-thumb.jpg
authors: "Andrew McPherson"
main-image: /images/research/touchkeys/tk-cover.jpg
production-date: 2011 - 2022
para: TouchKeys adds capacitive multi-touch sensing to the surface of the piano keys.  
links: ["https://www.kickstarter.com/projects/instrumentslab/touchkeys-multi-touch-musical-keyboard", "http://youtube.com/user/apm414/videos"]
link-names: ["Kickstarter campaign", "YouTube channel"]
---

{% include youtube.html youtube="fNxacJZXPic" %}

TouchKeys is a new musical instrument transforming the piano-style keyboard into an expressive multi-touch control surface. The TouchKeys sensors can be added to the surface of any keyboard, using capacitive touch sensing to measure the location of the musician's fingers on the keys during performance.

The project was launched on the crowd-funding website [Kickstarter](https://www.kickstarter.com/projects/instrumentslab/touchkeys-multi-touch-musical-keyboard) on 29 July 2013 and successfully finished its campaign on 2 September 2013. The campaign raised funding to build sets of TouchKeys that any musician can install on their own keyboard. They shipped by the end of January 2014, and a second production run completed in 2015. In 2016, the project spun out into an independent company, TouchKeys Instruments Ltd, which sold kits and keyboards until 2022.

**TouchKeys is no longer available for sale, but if you are an existing TouchKeys user you can find support for your kit here:**

* TouchKeys software downloads: [binary releases](https://github.com/apmcpherson/touchkeys/releases/tag/release) (Mac/Windows/Linux), [source code](https://github.com/apmcpherson/touchkeys/), [software manual](https://instrumentslab.org/data/andrew/touchkeys_manual_0.2.pdf)
* Installation instructions: [written guide](https://instrumentslab.org/data/andrew/touchkeys_installation.pdf), [tutorial video](https://vimeo.com/82399344)

## How it Works

{% include youtube.html youtube="BmRYuDOzTqU" %}

TouchKeys adds capacitive multi-touch sensing to the surface of any piano-style keyboard. Sensor overlays measure the location and contact area of the player's fingers on the key surfaces, and the data can be used to create a wide range of expressive effects including vibrato, pitch bends, timbre changes and improved emulations of non-keyboard instruments. The keyboard is traditionally a discrete interface, measuring notes by onset and release. The TouchKeys let the player continuously shape each note through the subtle expressive details of their finger motion.

{% include two-image-include.html left_image="touchkeys_finger_simulation.png" right_image="touchkeys_graph_simulation.png" image_subfolder="research/touchkeys" caption="Simulation of touch location calculation in a single axis" %}

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

## Playing Techniques

TouchKeys connects to your computer by USB. The included software transforms the data from the touch sensors and your keyboard into control messages for any synth. The mappings are fully customisable, and can be different for different parts of the keyboard. Here are some of the things you can do with TouchKeys:

### Vibrato

Rock the finger back and forth on the key to add a vibrato. The speed and width of the vibrato follows the motion of your finger, just like it would on a violin. But unlike a violin, the pitch always stays centred around the note you’re playing, so it never goes out of tune. You can adjust the sensitivity of the mapping, to make it engage on the slightest motion or to require a bigger movement before the vibrato begins.

### Pitch Bends

Slide the finger up and down a key to bend the pitch. The amount of pitch bend is adjustable, and no matter where you strike the key, the note begins at its normal pitch, so it’s there when you want it and stays out of the way the rest of the time. With a compatible synth setup, every note can have its own pitch bend, letting you retune melody and harmonies on the fly.

### Filter / Timbre Effects

In addition to pitch bend, sliding the finger up and down the key can control any MIDI parameter on your synth. For example, it could be used to control a filter cutoff, where sliding the finger upwards makes the note get brighter. The mappings are completely flexible: use horizontal or vertical position, absolute location or relative motion, or finger-key contact area, all with adjustable ranges.

### Rapid Retriggering

Add or remove a second finger from a single key to retrigger the note. Normally on the keyboard, striking the same key repeatedly is hard to do quickly, but this way you can rapidly retrigger notes. You can use it for tremolo effects like on a violin, or you can also use it to trigger custom key switches for your synth.

### Special Instrumental Effects

Many software instruments have key switches that create special effects. For example, on a software emulation of a brass instrument, you might add falls or buzzes to the end of a note. With TouchKeys, you can intuitively trigger these effects by pulling the finger along the key just as you release the note.

### Microtonal Playing

Divide the key into 2 or 3 sections with a different tuning on each section. By pressing the key in different places, it is like having 24 or 36 keys in every octave! The tunings are adjustable, and you can combine it with vibrato and pitch bend mappings to further adjust the pitch after the note begins.
 
## Videos

During the [Kickstarter campaign](https://www.kickstarter.com/projects/instrumentslab/touchkeys-multi-touch-musical-keyboard), we created over 10 videos demonstrating different applications of TouchKeys which are available on the [YouTube channel](http://youtube.com/user/apm414/videos). Here is a selection of those videos:

{% include youtube.html youtube="bIkKMHwXcko" %}
{% include youtube.html youtube="InNZkNz4NMc" %}
{% include youtube.html youtube="jt8Eb0ZalWQ" %}

A further gallery of TouchKeys videos can be found on this [TouchKeys YouTube playlist](https://www.youtube.com/playlist?list=PL7J-E0lEQw8xrmPxg9kRVDi5gGRiOCgLz).

## TouchKeys in the Press

During the Kickstarter campaign and its subsequent commercial launch, TouchKeys was the subject of over 25 press articles. Here is a selection:

* Synthtopia: [TouchKeys creator Andrew McPherson on bringing new expression to musical keyboards](http://www.synthtopia.com/content/2016/12/09/touchkeys-creator-andrew-mcpherson-on-bringing-new-expression-to-musical-keyboards/)
* Synthtopia: [TouchKeys promises to add multi-touch expression to your existing keyboard](https://www.synthtopia.com/content/2013/07/29/touchkeys-promises-to-add-multi-touch-expression-to-your-existing-keyboard/)
* Sound on Sound: [Touch Sensitive: the TouchKeys Project](http://www.soundonsound.com/people/touchkeys-project)
* Create Digital Music: [Multi-touch with your current keyboard, and how expressive, crowd-funded keys stack up](http://cdm.link/2013/08/the-latest-multitouch-expressive-idea-use-your-current-keyboard/)
* Time: [What if your piano’s keys supported multitouch and gesture control?](http://techland.time.com/2013/08/07/what-if-your-pianos-keys-supported-multitouch-and-gesture-control/)
* New Scientist: [Sensitive piano keys let pianists create new sounds](https://www.newscientist.com/article/dn23819-sensitive-piano-keys-let-pianists-create-new-sounds.html)
* Hackaday: [Touch control for every key on the keyboard](http://hackaday.com/2013/07/30/touch-control-for-every-key-on-the-keyboard/)
* Popular Science: [Why hasn’t there been a multitouch piano before now?](http://www.popsci.com/technology/article/2013-07/why-hasnt-there-been-multitouch-piano-now?src=SOC&dom=tw)
* Electronics Weekly: [TouchKeys electronic piano plays by sensors](https://www.electronicsweekly.com/blogs/gadget-master/sensors/touchkeys-electronic-piano-plays-by-sensors-2013-07/)
* Engadget: [TouchKeys overlay brings whole new meaning to ‘tickling the ivories’](https://www.engadget.com/2013-07-29-insert-coin-touchkeys.html)
* Kitmonsters: [TouchKeys interview with Andrew McPherson](http://www.kitmonsters.com/blog/touchkeys)