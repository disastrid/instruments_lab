---
layout: research
title:  "Magpick"
tag: "augmented-instruments"
tagline: An Augmented Guitar Pick for Nuanced Control
thumb: magpick/magpick-thumb.jpg
authors: "Fabio Morreale, Andrea Guidi, Andrew McPherson"
main-image: /images/research/magpick/magpick-cover___.jpg
production-date: 2018 - present
para: Magpick brings nuanced sound shaping to the electric guitar.
---

The Magpick is an augmented pick for electric guitar capable of eliciting new sounds using magnetic pickups normally installed in electric guitars.

Magpick uses electromagnetic induction to sense the motion of the guitar pick while Bela analyses, processes and translates this motion into nuanced, low-latency sonic interactions. It can be used with most electrified string instruments using magnetic transducers. 

{% include youtube.html youtube="MZIKEEDMzDQ" %}

## Motivation

### Extending the Guitar Plectrum

The Magpick is designed to extend the plectrum, allowing the player to continuously shape each note in dynamics, pitch and timbre while retaining the playing techniques available on the electric guitar.

{% include single-image-research.html fileName="magpick/magpick-front.png" %}

It introduces novel playing techniques that extend beyond traditional electric guitar performance. It is possible to use the plectrum to air-play above the strings, as well as control the pick angular position to subtly evolving tones which may or may not have the timbral qualities of the electric guitar.

## Playing the Pickups

The pick is equipped with a copper wire coil and functions by detecting the movements of guitarists through interaction with the magnetic field produced by any guitar pickups. This interaction generates voltage, which corresponds to the pick's motion concerning the magnets in the guitar pickup. Consequently, it provides insights into the actions of the plucking hand. Thanks to Bela, this data is captured with particular precision and minimal delay, enabling it to be used for modifying the guitar's sound in ways that align with established guitar techniques.

{% include single-image-research.html fileName="magpick/magpick-pickups.jpg" %}

This technology is non-intrusive, as it doesn't necessitate additional hardware installations on the guitar. Characteristics of the pick signals include that they are only generated when the guitarist strums in the pickup area (as opposed to, for example, over the fretboard); they react to pick movement above the strings, not necessarily making contact with them; and they are sensitive to the degree of motion with a wide dynamic range.

## Amplifier System

To ensure a favourable signal-to-noise ratio for the small signal detected by the system, two specialized amplifier circuits were developed (they detailed in the publication titled "Magpick: an Augmented Guitar Pick for Nuanced Control." These amplifiers each generate distinct types of signals, which we'll identify as "integrator" and "proportional," each with unique characteristics. The integrator signal, depicted in blue in the image below, is well-suited for detecting slower motions, such as waving the Magpick above the magnets. In contrast, the proportional signal, illustrated in orange in the image, is designed to identify high-frequency transient events, such as the snap of the pick following the plucking of a string.

{% include single-image-research.html fileName="magpick/magpick-signals.png" %}

These amplified signals were then linked to two analog inputs on a Bela Mini device. Simultaneously, the signal from the electric guitar itself (referred to as the "guitar signal") was connected to a third input. Within the Bela board, these three signals were merged using a Pure Data patch that processes the sound before transmitting it to the guitar amplifier.

{% include single-image-research.html fileName="magpick/magpick-diagram.gif" %}

## Data Mapping and Sound Design
Up to this point, we have created three distinct sound designs that combine the guitar signal with the control signals produced by the Magpick.

### Volume Swell
The most straightforward way to combine the pick signal with the guitar signal is through a basic multiplication of the two. This setup enables guitarists to manipulate the sound's envelope by moving the pick above the strings after plucking them. For instance, to achieve a gradual attack, a guitarist might pluck the string(s) on the fretboard and then slowly glide the plucking hand, holding the Magpick, over the neck pickup. Subsequently, they can engage in air-strumming above the strings to control the sustain. 

{% include youtube.html youtube="09sDsUIVr2Y" %}

In this scenario, air-strumming above the strings within the pickup area produces a nuanced tremolo effect with a higher level of control and expressiveness than tremolo pedals. Standard tremolo effects employ low-frequency oscillators to modulate the guitar signal's amplitude.

### Harmonised Delay
Under these circumstances, the output comprises the unaltered guitar signal that is sent directly to the output, along with a modified rendition of the guitar signal. The modification is carried out using one or more parameters that are controlled by the pick signal. As an illustration, we've created an audio effect using Bela and Pure Data, which we've aptly named "harmonized delay." This effect takes the guitar signal, conducts an FFT analysis, and then introduces delays to each resulting harmonic partial, resulting in a spectral harmonic arpeggio that is combined with the original guitar sound.

{% include youtube.html youtube="v0wWBLeoJJw" %}

The effect activates when the pick signal surpasses a predefined threshold. Subsequently, the pick-signal's intensity exerts control over both the number of generated partials and the interval of delay between them. This setup empowers guitarists to influence the speed of spectral arpeggios using their pick directly: strumming with greater intensity leads to higher frequencies and shorter delay intervals (ranging from 0 to 255 ms). Consequently, a strong pick signal reaches elevated frequencies, yielding brighter harmonic tones. The proportional preamp was chosen for its swift response to transients. This effect relies on Bela's low-latency capability, as the entire process depends on rapid peak detection of the input signal to determine the resulting sonic output.

### Scrambled Delay
Essentially, this effect functions as a basic granulator. It preserves the most recent 5 seconds of the guitar signal in a buffer. Subsequently, a segment of the recorded audio is chosen at random and played back at its original speed. The duration of this selection varies each time, randomly ranging from 1 to 2 seconds. Additionally, a fade-in and fade-out envelope is applied to each playback, enhancing the consistency of the output. Simultaneously, two of these playback buffers are active. 

{% include youtube.html youtube="6NU81paEbis" %}

The effect's volume is regulated through the integrator preamp, responding to the pick-signal. This sound can function similarly to a reverse delay layered over the guitarist's performance. It can also act as a tool for "recording" a brief musical phrase during regular play and replaying it randomised by moving the Magpick over the pickup region. The pseudocode below illustrates the minimal signal processing required for a rewarding interaction, provided the sensor and physical design align harmoniously.

{% include single-image-research.html fileName="magpick/magpick-puredata.png" %}

## References
F. Morreale, A. Guidi, and A. McPherson. [Magpick: an augmented guitar pick for nuanced control](https://www.nime.org/proceedings/2019/nime2019_paper013.pdf). Proc. New Interfaces for Musical Expression, Porto Alegre, Brazil, June 3-6, 2019.
A. McPherson, F. Morreale and A. Guidi. [Designing Creative Tensions between Concept and Embodied Practice](https://thingsofdesign.info/2019/mcpherson.pdf). CHI Workshop "Doing Things with Research through Design: With What, with Whom, and Towards What Ends?" Glasgow, UK, 2019.
