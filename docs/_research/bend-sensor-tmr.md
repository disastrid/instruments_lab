---
layout: research
title:  "String Bend Acquisition using TMR Angle Sensors"
tag: "augmented-instruments"
tagline: Audio Mostly '21, Adan L. Benito Temprano
thumb: /images/research/bend_sensor_tmr/bend_sensor_thumb.png
authors: ["Adan L. Benito Temprano", "Andrew P. McPherson"]
main-image: /images/research/bend_sensor_tmr/fretboard_string_bend.jpg
para: "A TMR Angle Sensor for Gesture Acquisition and Disambiguation on the Electric Guitar"
links: ["https://github.com/adanlbenito/bend_sensor_breakout"]
link-names: ["Design files"]
---

{% include youtube.html youtube="ANnCJgCdUx4" %}


The electric guitar might be one of the most ubiquitous instruments from the 20th century. The instrument has been embraced and adapted by a wide range of musical traditions, leading to idiomatic playing styles that carry both stylistic elements and expressive techniques. As a result, a gestural palette has been developed that contributes to shaping the identity of the instrument by conveying not only musical meaning and articulation, but a signature that allows us to recognise genre and even particular personal styles.

Capturing these expressive gestures, however, poses a series of difficult challenges. The flexibility of left- and right-hand techniques, the instrument's inherent polyphony and the different nuances associated with the combination of *excitation* gestures (e.g. plucking) and *modification* gestures  (e.g. fretting, string bending, vibrato, etc) make the extraction of musical parameters from the audio signal produced by the instrument a complex task. Moreover, some of these gestures, despite being associated with different physical interactions and perhaps presenting different significance to the performer, might have similar, even identical, sonic results and therefore be virtually indistinguishable from this perspective.

One potential solution that might provide the kind of nuanced analysis required for the study of expressive gestures is the use of complementary direct sensing methods that provide measures related to the physical features of the performer's actions. This has been a staple of certain Digital Musical Instrument design trends in recent years and has allowed researchers to create interfaces which repurpose existing user expertise in order to retain access to virtuosity.

In this work, we present a novel application of Tunneling Magnetoresistance (TMR) sensors for tracking the horizontal displacement of a ferromagnetic string, which can be used to capture different dimensions of playing and disambiguate gestures that have similar sound signatures. We analyse how this sensor can be easily calibrated based on pitch contour estimation and show potential applications for music transcription and instrument augmentation where the performer's expertise is repurposed for expanding the gestural possibilities of the instruments.

---

- Adan L. Benito Temprano and Andrew P. McPherson. _A TMR Angle Sensor for Gesture Acquisition and Disambiguation on the Electric Guitar_. In Proceedings of the International Audio Mostly Conference on Sonic experiences in the era of the Internet of Sounds, September 1–3, 2021, Trento, Italy.
