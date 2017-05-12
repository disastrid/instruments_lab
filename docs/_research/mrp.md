---
layout: research
title:  "Magnetic Resonator Piano"
tag: "augmented instruments"
tagline: Electromagnetically-augmented acoustic piano
thumb: mrp/mrp-thumb.jpg
authors: "Andrew McPherson"
main-image: /images/research/mrp/mrp-cover.jpg
production-date: 2009 - present
para: The magnetic resonator piano brings continuous note shaping to the acoustic piano.
---

The magnetic resonator piano (MRP) is an electronically-augmented acoustic piano capable of eliciting new sounds *acoustically* from the piano strings, without speakers. Electromagnets induce vibrations in the strings independently of the hammers, creating infinite sustain, crescendos, harmonics, pitch beends and new timbres, all controlled from the piano keyboard.

The MRP installs in any grand piano and has been used in compositions, performances and recordings internationally.

{% include youtube.html youtube="f79d_oVqv4Y" %}

## Motivation

### Extending the Piano

The piano is a percussion instrument whose design has remained essentially unchanged over a century. Sound is produced by hammers striking strings, and once a note is struck, the performer has no means to alter its sound before it is released. For example, the following gesture is impossible on the acoustic piano:

{% include single-image-research.html fileName="mrp/mrp-crescendo.png" %}

The MRP was initially designed as an extension of the piano, allowing the player to continuously shape each note in dynamics, pitch and timbre, while retaining the richness and nuance of the acoustic grand piano.

### New Acoustic Sounds

The MRP also unlocks a sound world far removed from the traditional piano. When the keys are played lightly and no hammers strike the strings, the electromagnets elicit sustained, subtly evolving tones which have many of the acoustic qualities of the piano, including the sympathetic resonance between strings, but without the familiar percussion. It is also possible to explore the space "between the notes" by bending notes away from where the strings are tuned and exploring the harmonics of each string. The results of this mode of playing have been explored in compositions and gallery installations.

## Electromagnetic Actuation

{% include single-image-research.html fileName="mrp/mrp-magnets1.jpg" %}
{% include single-image-research.html fileName="mrp/mrp-magnets2.jpg" caption = "Electromagnets are placed just above the piano strings on adjustable brackets." %}

### Principle of Operation

{% include single-image-research.html fileName="mrp/mrp-magnet-principle.png" %}

Piano strings are made of steel, which is a ferromagnetic material, meaning it can be attracted by a magnetic field. The MRP uses 88 electromagnetic actuators to cover the complete range of the piano (one actuator per note, though a note may include 2 or 3 identically-tuned strings). When current is passed through an actuator, the string is pulled upward; when the current is turned off, the string returns to its original position. By modulating the current at the frequency of the string or one of its harmonics, the string is made to vibrate sympathetically without ever having been struck by the hammer.

### Amplifier System

{% include single-image-research.html fileName="mrp/mrp-amplifier.jpg" caption="Amplifier board for 18 notes. 5 boards cover the complete range of the piano." %}

Audio signals for the electromagnets ultimately come from a computer, controlled by the performer's actions at the keyboard. One amplifier per actuator is used to achieve the necessary power level. The current instrument is capable of up to 20W per string for short time, limited by the heating of the magnets. The tones produced can be quite loud, especially in the middle and treble registers, comparable in sound pressure level to forte playing on the traditional piano. A wide dynamic range is possible which also includes tones barely above silence.

The instrument covers 88 strings, but requiring 88 audio channels would be prohibitive. The amplifier circuitry therefore includes a signal routing system where audio channels are dynamically allocated to each string as needed. A standard audio interface can be used, with the number of audio channels (up to 16) determining the maximum polyphony of the instrument. In practice, the instrument is often run with 6-to-10-note polyphony.

### Accounting for Tuning

The tuning of each piano varies slightly, and the best performance is obtained when the actuator frequencies exactly match the tuning of the strings, with the bass notes being particularly sensitive to tuning accuracy. To adjust to the tuning of the specific piano, a pickup can be placed on the soundboard and a phased-locked loop (PLL) system used to lock the actuators into the existing vibrations of the strings. More detail on this process can be found in [this paper](http://www.tandfonline.com/doi/abs/10.1080/09298211003695587).

**References for Electromagnetic Actuation**

A. McPherson. [The magnetic resonator piano: electronic augmentation of an acoustic grand piano](http://www.tandfonline.com/doi/abs/10.1080/09298211003695587). Journal of New Music Research 2010, 39 (3), 189-202.

A. McPherson. [Techniques and circuits for electromagnetic instrument actuation](http://www.eecs.umich.edu/nime2012/Proceedings/papers/117_Final_Manuscript.pdf). Proc. New Interfaces for Musical Expression, Ann Arbor, MI, USA, 2012. [Design Materials](http://c4dm.eecs.qmul.ac.uk/rdr/handle/123456789/25)

## Continuous Key Position

{% include single-image-research.html fileName="mrp/mrp-aberystwyth.jpg" caption="The MRP in an art gallery in Aberystwyth as part of the show Beyond the Moon by printmaker Wuon-Gean Ho. The scanner bar with multicoloured LED feedback can be seen on the keyboard." %}

### Scanner Hardware

Continuous control of every note is a primary goal of the MRP, whether it is used to subtly extend the sounds of the traditional piano or to create novel and unusual effects. MIDI keyboards represent notes solely by onset and release, and even where aftertouch is used, the degree of control is insufficient for the continuously-evolving MRP sounds. Instead, a custom optical scanner bar is placed on the piano keyboard which records the continuous angle of each key.

Originally, a modified Moog Piano Bar was used for this purpose but a new dedicated solution has been developed, detailed in this [NIME 2013 paper](http://www.eecs.qmul.ac.uk/~andrewm/mcpherson_nime2013.pdf). The scanner uses optical reflectance sensing on each key:

{% include single-image-research.html fileName="mrp/mrp-scanner.jpg" caption="Close-up of scanner on keyboard. Optical reflectance sensors use LED and phototransistor in a single package." %}

### Data Mapping and Performance

Continuous key data can be used to capture the subtle details of how a key has been pressed, including dimensions beyond velocity. More information on these measurements can be found in [this paper](http://dl.acm.org/authorize?406423). Continuous key angle also allows new techniques including partial key presses, light taps on the surface, vibrato and aFtertouch on the acoustic piano (since the keybed is lined in felt, which compresses under pressure).

A computer maps key angle to actuator behaviour in a manner designed to be intuitive for the performer. The pianist does not interact with the computer during the normal performance process, though it is possible for certain aspects of the mappings to be dynamically changed by the pianist or another person. The standard mapping uses key angle to affect the volume of a note, such that a slow key press will produce a crescendo from silence. Pressure on a key will change the timbre of a note, and rhythmic oscillation in key pressure will produce a vibrato effect. Lightly, repeatedly tapping the surface of the key produces a glissando up the harmonic series of the note, creating a shimmering effect. When one key is held and a neighbouring key is lightly pressed, the pitch can be bent up or down. Each of these effects is demonstrated in the video at the top of this page.

**References for Continuous Key Position**

A. McPherson and Y. Kim. [Augmenting the acoustic piano with electromagnetic string actuation and continuous key position sensing](http://www.nime.org/proceedings/2010/nime2010_217.pdf). Proc. New Interfaces for Musical Expression, Sydney, Australia, 2010.

A. McPherson and Y. Kim. [Multidimensional gesture sensing at the piano keyboard](http://www.eecs.qmul.ac.uk/~andrewm/mcpherson-cmj2012.pdf). Proc. ACM Conference on Human Factors in Computing Systems (CHI), Vancouver, BC, Canada, 2011.

A. McPherson and Y. Kim. [The problem of the second performer: building a community around an augmented piano](http://www.eecs.qmul.ac.uk/~andrewm/mcpherson-cmj2012.pdf). Computer Music Journal 2012, 36 (4), 10-27. (PDF &copy; 2013 Massachusetts Institute of Technology; archived with permission from [Computer Music Journal](http://www.mitpressjournals.org/cmj))

A. McPherson. [Portable measurement and mapping of continuous piano gesture](http://www.eecs.qmul.ac.uk/~andrewm/mcpherson_nime2013.pdf). Proc. New Interfaces for Musical Expression, Seoul, South Korea, 2013.

A. McPherson. [Buttons, handles, and keys: advances in continuous-control keyboard instruments](http://www.mitpressjournals.org/doi/pdf/10.1162/COMJ_a_00297). Computer Music Journal 29(2), 2015.


## Repertoire

The MRP has been used in new pieces and recordings by a growing number of composers and performers. Since it can be set up in any grand piano and fits in travel-sized cases, new pieces can be performed anywhere. Scores and recordings are available from the composers in most cases; [contact Andrew McPherson](mailto:a.mcpherson@qmul.ac.uk) if you are interested.

Two major projects have expanded the repertoire for MRP. A 2011 collaboration with Philadelphia composers and performers is described in [this article](http://www.eecs.qmul.ac.uk/~andrewm/mcpherson-cmj2012.pdf) in Computer Music Journal. In 2013, the MRP has been featured by the [London Chamber Orchestra](http://www.lco.co.uk) as part of the project "LCO New: Inspired by Digital".

{% include youtube.html youtube="WDTaH_d8s8c" %}

### Classical Compositions

* [Andrew McPherson](http://andrewmcpherson.org/), *Secrets of Antiykthera* (2009), 35'. Performances by Steve Beck, Sandra Gu and Ryan MacEvoy McCullough. Commercially released on [Innova Recordings](https://www.innova.mu/albums/andrew-mcpherson/secrets-antikythera). [Video](https://vimeo.com/34848595)
* [Andrew McPherson](http://andrewmcpherson.org/), *d'Amore* (2009), 11', for viola and MRP. Performances by Nadia Sirota, Bridget Carey and Rachel Ku. Commercially released on [Innova Recordings](https://www.innova.mu/albums/andrew-mcpherson/secrets-antikythera).
* [Andrew McPherson](http://andrewmcpherson.org/), *Layers Deep Below* (2011), 8'. Premiere by Andrew McPherson.
* [David Carpenter](http://davidowencarpenter.com/), *Job* (2011), 13', for baritone voice and MRP. Premiere by Lawrence Indik and Feifei Zhang.
* [William Derganc](https://soundcloud.com/wderganc), *Play* (2011), 6', for violin and MRP. Premiere by Noco Kawamura and Matt Bengtson.
* [Daniel Fox](https://thoughtstoodefinite.com), *Intermezzo* (2011), 5'. Performances by Feifei Zhang and Hunter Noack. [Video](https://www.youtube.com/watch?v=9yU1Aa8DeU8)
* [Daniel Shapiro](https://www.atlanticmusicfestival.org/artists/daniel-shapiro/), *The Masons of Heidelberg* (2011), 14'. Performances by Katya Popova, Elaine Chew and Nic Gerpe. Video: [Mvt. I](https://www.youtube.com/watch?v=xhkQ8ammO-c); [Mvt. II](https://www.youtube.com/watch?v=p1Rtfbk9lLY); [Mvt. III](https://www.youtube.com/watch?v=bk-A5C17SVo)
* [Jeff Snyder](http://www.scattershot.org/news.htm), *Fantasy* (2011), 10'. Performances by Eric Wubbels and Lola Perrin.
* [Tony Solitro](http://www.tonysolitro.com), *Spectra of Morning* (2011), 10'. Premiere by Feifei Zhang. [Video](https://www.youtube.com/watch?v=IAnPN7busYE)
* [William Dougherty](http://www.williamdougherty.org), *Emanations* (2013), for violin, viola, cello, bass and MRP. To be premiered by members of London Chamber Orchestra.
* [Pedro Faria Gomes](http://www.pedrofariagomes.com), *tereza's dreams* (2013), for 8-piece ensemble including MRP. To be premiered by members of London Chamber Orchestra.
* [James Moriarty](http://jamesmoriarty.net), *Untempered by the Hand of Man* (2013), for 5-piece ensemble including MRP. To be premiered by members of London Chamber Orchestra.
* [Nick Morrish Rarity](https://soundcloud.com/nicholasmorrishrarity) and [Tim Morrish](https://soundcloud.com/timothy-morrish), *Impulse.Pulse.Parted* (2013), for 8-piece ensemble including MRP. To be premiered by members of London Chamber Orchestra.
* [Andrew Thomas](https://soundcloud.com/at385), *Till Human Voices Wake Us* (2013), for 6-piece ensemble including MRP. To be premiered by members of London Chamber Orchestra.
* [Richard Peat](http://www.richardpeat.com), *You leave it with me* (2014), for magnetic resonator piano. Premiered by Neil Georgeson, QMUL, 25 October 2014.
* [Ben Parker](http://www.benparkercomposer.com/biography), *Time Stopped and Snow Fell* (2015). for magnetic resonator piano. Premiered by Ben Powell, Royal Northern College of Music (UK), 22 March 2015.
* [Sergio Cote](http://www.sergiocote.com), piece for magnetic resonator piano (2015). Premiered by Leanne Cody, Royal Northern College of Music (UK), 22 March 2015.
* [Julia Adolphe](http://juliaadolphe.com), *Magnetic etudes* (2015), for magnetic resonator piano. Premiered by Aron Kallay ([People Inside Electronics](http://peopleinsideelectronics.com)), Neighborhood Unitarian Universalist Church of Pasadena, CA, 18 April 2015. Video: [Mvt. I](https://www.youtube.com/watch?v=bFnKX1sWA6Y); [Mvt. II](https://www.youtube.com/watch?v=kIY5wOIbx88); [Mvt. III](https://www.youtube.com/watch?v=yIuzieGE8BA)
* Jeremy Cavaterra, *Gegenschein* (2015), for magnetic resonator piano. Premiered by Steven Vanhauwaert ([People Inside Electronics](http://peopleinsideelectronics.com)), Neighborhood Unitarian Universalist Church of Pasadena, CA, 18 April 2015. [Video](https://www.youtube.com/watch?v=w310tzATQGo)
* [Alexander Elliot Miller](http://www.alexanderemiller.com), *88 MPH* (2015), for magnetic resonator piano. Premiered by Nic Gerpe ([People Inside Electronics](http://peopleinsideelectronics.com)), Neighborhood Unitarian Universalist Church of Pasadena, CA, 18 April 2015. [Video](https://www.youtube.com/watch?v=D3MMg_cF66o)
* [Elise Roy](http://www.eliseroy.com), *Sonatine* (2015), for magnetic resonator piano. Premiered by Richard Valitutto ([People Inside Electronics](http://peopleinsideelectronics.com)), Neighborhood Unitarian Universalist Church of Pasadena, CA, 18 April 2015. [Video](https://www.youtube.com/watch?v=LkCP615cB-Q)
* [Oded Ben-Tal](http://obental.wixsite.com/main), *Sonata (Scarlatti, Schubert, Scriabin)* (2016), for magnetic resonator piano and live electronics. [Premiered by Elaine Chew](http://elainechew-piano.blogspot.com/2016/06/withwithout-excerpts.html), Schott Music London, 24 June 2016.

### Other Recordings

The magnetic resonator piano is featured in the new album "Field of Reeds" by [These New Puritans](http://thesenewpuritans.com/), released April 2013. The recording took place December 2012 on a Boesendorfer 225 piano at [Snap Studios](http://snapstudios.co.uk/) in north London.

**References for Musician Collaboration**

A. McPherson and Y. Kim. [The problem of the second performer: building a community around an augmented piano](http://www.eecs.qmul.ac.uk/~andrewm/mcpherson-cmj2012.pdf). Computer Music Journal 2012, 36 (4), 10-27. (PDF &copy; 2013 Massachusetts Institute of Technology; archived with permission from [Computer Music Journal](http://www.mitpressjournals.org/cmj))

## References (collected)

A. McPherson. [The magnetic resonator piano: electronic augmentation of an acoustic grand piano](http://www.tandfonline.com/doi/abs/10.1080/09298211003695587). Journal of New Music Research 2010, 39 (3), 189-202.

A. McPherson and Y. Kim. [Augmenting the acoustic piano with electromagnetic string actuation and continuous key position sensing](http://www.nime.org/proceedings/2010/nime2010_217.pdf). Proc. New Interfaces for Musical Expression, Sydney, Australia, 2010.

A. McPherson and Y. Kim. [Multidimensional gesture sensing at the piano keyboard](http://www.eecs.qmul.ac.uk/~andrewm/mcpherson-cmj2012.pdf). Proc. ACM Conference on Human Factors in Computing Systems (CHI), Vancouver, BC, Canada, 2011.

A. McPherson. [Techniques and circuits for electromagnetic instrument actuation](http://www.eecs.umich.edu/nime2012/Proceedings/papers/117_Final_Manuscript.pdf). Proc. New Interfaces for Musical Expression, Ann Arbor, MI, USA, 2012. [Design Materials](http://c4dm.eecs.qmul.ac.uk/rdr/handle/123456789/25)

A. McPherson and Y. Kim. [The problem of the second performer: building a community around an augmented piano](http://www.eecs.qmul.ac.uk/~andrewm/mcpherson-cmj2012.pdf). Computer Music Journal 2012, 36 (4), 10-27. (PDF &copy; 2013 Massachusetts Institute of Technology; archived with permission from [Computer Music Journal](http://www.mitpressjournals.org/cmj))

A. McPherson. [Portable measurement and mapping of continuous piano gesture](http://www.eecs.qmul.ac.uk/~andrewm/mcpherson_nime2013.pdf). Proc. New Interfaces for Musical Expression, Seoul, South Korea, 2013.

A. McPherson. [Buttons, handles, and keys: advances in continuous-control keyboard instruments](http://www.mitpressjournals.org/doi/pdf/10.1162/COMJ_a_00297). Computer Music Journal 29(2), 2015.

