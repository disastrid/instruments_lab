---
layout: research
title:  "Tactility in the Design of Digital Musical Instruments"
tagline: PhD research: Robert Jack
tag: "instrument-design"
desc: Research tools
categories: research
thumb: tactility/tactile-thumb.jpg
authors: "Robert Jack"
main-image: /images/research/tactility/tiles-2.jpg
para: Maintaining and Constraining Performer Touch.

---

## Touch in musical performance

Expression in musical performance is deeply connected to the particular touch of a performer, that is the nuances of their control of an instrument. Alongside hearing, the haptic sense is the primary modality through which we engage with musical instruments. In fact learning a musical instrument can be understood as one of the most developed haptic cultural practices, where years of practical and theoretical training reinforce sensorimotor pathways allowing us to perform complex music. Robert Jack, a PhD candidate at the augmented instruments lab, is researching the mechanisms of touch and how they relate to the design of new digital musical instruments. When playing an acoustic instrument we get a great deal of rich sensory information from the part of our body which makes contact with the instrument (hands, fingertips, lips, shoulders). This haptic experience is integrated with the sound that the instrument produces, summing together to give the perception of playing a note. For most digital musical instruments, although touch-mediated interaction is still the primary means of control, there is no comparably rich physical experience from the instrument and little relationship between the sound of an instrument and its feel. This research focuses on the contact that a performer makes with an instrument. This shifts the focus to the combination of auditory and haptic feedback that we get from an instrument and how they integrate with one another in the moment of excitation. This informs both the feel of the instrument, that is it's immediate feedback to our haptic and auditory sense, and the mental model we have of that instrument, shaping the gestures that we use to control it and our internal representation of its mechanism. This research project aims to provide guidelines for designers on how to cater for the sense of touch in the process of designing digital musical instruments. As part of this project new musical instruments have been designed specifically to investigate different aspects of touch in digital musical instrument performance.

{% include single-image-research.html fileName="tactility/hands-tactile.jpg" %}


## Tactile exploration and instrument navigation

This first study of this research project investigated how a digital musical instrument can respond dynamically to performer control through vibrations in the body of the instrument, and how this feedback can provide the performer with additional performance information. The aim was to create vibro-tactile feedback conditions that could guide the hand of the performer whilst remaining harmonically linked to the sound output of the instrument. An embedded DMI with various vibro-tactile feedback conditions was created using Bela to test this out. It was designed to assist performer intonation (accuracy of tuning) on an instrument with continuous pitch control (like a cello, trombone, theremin). The instrument was tested with ten musicians who played the instrument while it was hidden from sight, encouraging concentration on the relationship between touch and hearing. Findings from the user study were present at TEI 2016 in Eindhoven and can be read in the paper below.

We found an increased tuning accuracy with each of the tactile feedback conditions, but noted that certain vibration patterns imposed temporal constraints that disrupted musical performance. We also witnessed a series of emergent gestures that used the interplay of audio and haptic feedback in unexpected ways. Where previous studies used force feedback to push the performer to the right pitch, this interface required an active correction by the performer. It is interesting that both methods are successful in improving accuracy which suggests that there is great potential for integrating audio-related vibrotactile feedback for guidance tasks in interfaces although the temporal demands of performance can limit the complexity of this feedback.

R. Jack, T. Stockman and A. McPherson. Navigation of pitch space on a digital musical instrument with dynamic tactile feedback. Proc. TEI, Eindhoven, Netherlands, 2016.

{% include single-image-research.html fileName="tactility/box-study-1.jpg" %}

{% include single-image-research.html fileName="tactility/box-study-2.jpg" %}

## Auditory-haptic latency and instrument quality

In the second study the focus shifted to the temporal behaviour of a DMI. A study was designed to test the impact of audio-haptic asynchrony (latency) on the perceived quality of a DMI. This work built on a previously study that we conducted which found that common techniques employed in DMI design exhibit action-sound latency above a threshold of 10ms set by Wessel in 2002. We wanted to test out whether this threshold is valid in the most demanding of musical situations, with rhythmic performance on a percussion instrument. We were also interested in finding out how low levels of latency (mostly below the threshold of perception) are reported by musicians in terms of instrument quality. Alongside this we also measured the impact of latency on the temporal accuracy of their performance. For the study we built a novel percussion instrument constructed of eight ceramic tiles and built with using Bela. The instrument is capable of sub-millisecond latency and negligible jitter (variation in latency).

The first iteration of this study was conducted with general musicians who freely improvised on the instrument evaluating different the latency conditions (0ms, 10ms, 20ms, 10ms±3ms) in terms of instrument quality. We found that even if the level of latency is below the degree of accuracy that can be achieved by the performer on an instrument, it can still impact on how the quality of that instrument is judged. None of the participants were able to perform with a degree of accuracy that was better than the jitter condition (± 3ms) yet this condition alongisde the 20ms latency condition showed significantly lower ratings of quality compared to the zero or 10ms latency conditions. There were also multi-sensory by-products of some of the latency conditions, where participants put more force into their strikes as the latency increased. The details of this study can be found in the below paper presented at Audio Mostly 2016.

R. H. Jack, A. McPherson and T. Stockman. Effect of latency on performer interaction and subjective quality assessment of a digital musical instrument Proc. Audio Mostly,Norrköping, Sweden, 2016.

A. McPherson, R. Jack and G. Moro. Action-Sound Latency: Are Our Tools Fast Enough?Proc. NIME, Brisbane, Australia, 2016.

{% include single-image-research.html fileName="tactility/tiles-1.jpg" %}

{% include single-image-research.html fileName="tactility/tiles-2.jpg" %}



