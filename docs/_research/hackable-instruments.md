---
layout: research
title:  "Hackable Instruments"
tagline: Exposing the scaffolding of digital musical instruments
tag: ["instrument-design", "research-projects"]
desc: Research tools
categories: research
thumb: hackable/d-box-thumb.jpg
authors: "Andrew McPherson, Victor Zappi"
main-image: /images/research/hackable/d-box_open_cover_photo.jpg
para: This project ran 2013-14, with support from the UK Engineering and Physical Sciences Research Council (grant EP/K032046/1).

---

{% include youtube.html youtube="JOAO-EUtrGQ" %}

This project ran 2013-14, with support from the UK Engineering and Physical Sciences Research Council (grant [EP/K032046/1](http://gow.epsrc.ac.uk/NGBOViewGrant.aspx?GrantRef=EP/K032046/1)).

Main researchers: **Victor Zappi**, **Andrew McPherson**

----

Throughout music history, performers have been playing instruments in ways the designer did not expect. For example, distortion and feedback on the electric guitar were engineering limitations before they became the sound of rock and roll, and the way hip-hop DJs use the turntable subverts its original purpose as a home playback device. Some performers even make physical modifications to their instruments to adapt them to their personal needs.

By contrast, the "black-box" design of many digital musical instruments (DMIs) can prevent musicians from making arbitrary modifications to the instrument, and may even restrict the performer to a limited set of playing techniques envisioned by the designer. The comparative difficulty of adapting new DMIs to purposes the designer did not anticipate may hold back the uptake of these instruments in the musical community.

The Hackable Instruments project undertook a series of studies, inspired by the practice of circuit bending and by the HCI literature on appropriation, examining how performers use and modify musical instruments.

### Constraints and Creativity: the Cube Instrument Study

{% include single-image-research.html fileName="hackable/cube_medely.jpg" %}

Many digital musical instrument designs seek to give the performer as much control as possible. But could giving them less control actually be a creative benefit?

That constraints can be a source of creative inspiration has long been known. Building on earlier work by [Gurevich et al.](http://www.nime.org/proceedings/2010/nime2010_106.pdf), we created a highly constrained, self-contained musical instrument with a touch sensor and speaker in a wooden cube. We made 10 copies of the instrument with identical hardware and two different versions of the software:

* Two degrees of freedom: pressure changes timbre, touch position changes pitch
* One degree of freedom: pressure changes timbre, but no pitch control

We gave the instruments to 10 musicians and asked them to prepare a performance, collecting observations on their usage of the instrument and interviews and questionnaires about their experience. We found that performers on the 2 degree-of-freedom instrument explored fewer playing techniques than the 1 degree-of-freedom group, who discovered a diverse and unusual set of ways to play the instrument. Moreover, the 1 degree-of-freedom group rated the instrument more highly than the 2 degree-of-freedom group.

Our finding, though limited in size, suggests that adding more degrees of freedom does not necessarily improve the creative value of an instrument, and that in certain cases the opposite may be true.

Read the paper:  V. Zappi and A. McPherson. [Dimensionality and appropriation in digital musical instrument design](http://www.eecs.qmul.ac.uk/~andrewm/zappi_nime2014.pdf). Proc. New Interfaces for Musical Expression, London, UK, 2014.

### Designing for Appropriation and Modification: the D-Box

{% include single-image-research.html fileName="hackable/d-box_closed.jpg" %}

The D-Box is a digital musical instrument designed to be modified and hacked by the performer. Like the earlier cube instrument, it is a self-contained instrument with touch sensors and a wooden cube, which initially presents a simple, limited interface to the performer (though not as tightly constrained as the original cube instrument). But uniquely, the side of the box can be opened, revealing an electronic breadboard:

{% include single-image-research.html fileName="hackable/dbox-interior.jpg" %}

By rewiring circuits on the breadboard, the performer can discover new and unusual sounds. Unlike more familiar modular synthesisers, the behaviour of the instrument is governed by feedback loops between hardware and software, so changes in the wiring can have chaotic and unpredictable (but still repeatable) effects.

The D-Box was used in a study with 10 performers examining how they played and modified the instrument. We found that performers discovered sounds and techniques that went beyond our original design, and that experienced circuit benders could deploy their skills on the instrument. 

Read about the D-Box design and performance here: V. Zappi and A. McPherson. [Design and use of a hackable digital instrument](https://www.eecs.qmul.ac.uk/~andrewm/zappi_icli14.pdf). Proc. Live Interfaces, Lisbon, Portugal, 2014.

Read about using feedback between hardware and software as a musical design tool: A. McPherson and V. Zappi. [Exposing the scaffolding of digital instruments with hardware-software feedback loops](https://nime2015.lsu.edu/proceedings/258/0258-paper.pdf). Proc. New Interfaces for Musical Expression, Baton Rouge, LA, USA, 2015. 

We also used the D-Box in hacking workshops with the general public, where we observed patterns of exploration and playful interaction which differ from how people interact with software tools or other musical instruments. We examine the outcomes in the context of Gaver’s work on ludic design, and offer suggestions for interactive system designers.

Read about the D-Box workshops and their implications for design: A. McPherson, A. Chamberlain, A. Hazzard, S. McGrath and S. Benford. Designing for exploratory play with a hackable digital musical instrument. Proc. DIS, Brisbane, Australia, 2016.

You can find code and design materials for the D-Box here: [https://github.com/BelaPlatform/d-box](https://github.com/BelaPlatform/d-box)

For further details on building your own D-Box, please contact us!

### Bela: an Embedded Platform for Ultra-Low-Latency Interactive Audio

The hardware and software behind the D-Box eventually developed into [Bela](bela.html), an open-source embedded platform for audio and sensor processing. Bela is designed for creating musical instruments and other interactive audio systems, and features extremely low (< 1ms) latency between action and sound, far faster than can be achieved on standard computers.

Bela successfully launched on [Kickstarter](https://www.kickstarter.com/projects/423153472/bela-an-embedded-platform-for-low-latency-interact) in April 2016, drawing support from more than 500 backers. It is now [available for general purchase](https://shop.bela.io) and has a growing user and developer community. Read more about Bela on the [Bela research page](bela.html) and at [http://bela.io](http://bela.io).

Read about the technical design and performance of Bela here: A. McPherson and V. Zappi. [An environment for submillisecond-latency audio and sensor processing on BeagleBone Black](http://www.eecs.qmul.ac.uk/~andrewm/mcpherson_aes2015.pdf). Proc. AES 138th Convention, Warsaw, Poland, 2015.


## References (collected)

A. McPherson, A. Chamberlain, A. Hazzard, S. McGrath and S. Benford. [Designing for exploratory play with a hackable digital musical instrument](http://eprints.nottingham.ac.uk/33165/1/dbox_rev.pdf). Proc. DIS, Brisbane, Australia, 2016.

A. McPherson and V. Zappi. [An environment for submillisecond-latency audio and sensor processing on BeagleBone Black](http://www.eecs.qmul.ac.uk/~andrewm/mcpherson_aes2015.pdf). Proc. AES 138th Convention, Warsaw, Poland, 2015.

V. Zappi and A. McPherson. [The D-Box: how to rethink a digital musical instrument](http://isea2015.org/proceeding/submissions/ISEA2015_submission_209.pdf). Proc. ISEA, Vancouver, BC, Canada, 2015.

A. McPherson and V. Zappi. [Exposing the scaffolding of digital instruments with hardware-software feedback loops](https://nime2015.lsu.edu/proceedings/258/0258-paper.pdf). Proc. New Interfaces for Musical Expression, Baton Rouge, LA, USA, 2015. 

V. Zappi and A. McPherson. [Design and use of a hackable digital instrument](https://www.eecs.qmul.ac.uk/~andrewm/zappi_icli14.pdf). Proc. Live Interfaces, Lisbon, Portugal, 2014.

V. Zappi and A. McPherson. [Dimensionality and appropriation in digital musical instrument design](http://www.eecs.qmul.ac.uk/~andrewm/zappi_nime2014.pdf). Proc. New Interfaces for Musical Expression, London, UK, 2014. 

J. Topliss, V. Zappi and A. McPherson. [Latency performance for real-time audio on BeagleBone Black](http://www.eecs.qmul.ac.uk/~andrewm/lac2014.pdf). Linux Audio Conference, Karlsruhe, Germany, 2014.
 
