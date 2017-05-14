---
layout: research
title:  "Bela"
tagline: Open source embedded platform for ultra-low latency interactive audio
tag: "instrument-design"
desc: Research tools
categories: research
thumb: bela/bela-thumb.jpg
authors: ""
main-image: /images/research/bela/belaboard.jpg
links: ["http://bela.io", "https://www.kickstarter.com/projects/423153472/bela-an-embedded-platform-for-low-latency-interact", "http://twitter.com/belaPlatform"]
link-names: ["Bela website", "Kickstarter page", "Bela twitter account"]
para: 

---

### Bela: an Embedded Platform for Ultra-Low-Latency Interactive Audio

Bela is an open-source embedded computing platform developed for high quality, ultra-low latency interactive audio. Bela was initially funded on [Kickstarter](https://www.kickstarter.com/projects/423153472/bela-an-embedded-platform-for-low-latency-interact) in April 2016, and has been growing ever since. Bela provides stereo audio, analogue and digital I/O in a single self-contained package. It combines the processing power of the [BeagleBone Black](https://beagleboard.org/black) embedded computer with the timing precision and connectivity of a microcontroller.

{% include single-image-research.html fileName="bela/sideview.jpg" %}


Bela features an on-board, browser-based IDE, making it easy to get up and running without requiring any additional software. The end result: digital instruments and interactive objects that are faster to develop and more responsive to use.

### Built for speed

A dedicated hardware and software environment provides hard real-time performance with 1ms latency while retaining the capabilities and power of a 1GHz embedded computer running Linux.

### Connected everything

Use Bela's stereo audio input and output to create musical instruments and audio effects. Connect to the physical world with Bela's 8 analogue inputs, 8 analogue outputs and 16 digital I/O pins. You can also use ethernet, USB (including MIDI), SD card storage and other features of the BeagleBone Black.

### Embedded

Bela's compact form factor means that it easily integrates into portable interactive objects. It's a self-contained processing platform that eliminates the need for a laptop. It's also easily battery powered so completely mobile.

### Code your way

Code in C/C++, PureData, or Faust. Bela features a browser-based IDE, with full C/C++ and PureData development capabilities. Includes powerful features at your fingertips, such as an in-browser oscilloscope, code examples, and much more. You develop it, Bela runs it.

### Open source

Bela’s hardware and software are both open source, and Bela benefits from the innovation and support of its worldwide community of musicians, designers, makers and tinkerers.

## Who is Bela for?

Bela is for anyone who wishes to develop powerful and responsive embedded interactive audio applications. It is particularly suited to electronic musicians and instrument designers, but is also useful for artists, makers and other embedded hardware programmers who want to take advantage of its ultra-low latency audio and sensor processing capabilities.

## Performance

Bela is designed with audio in mind. It uses the BeagleBone Black single-board computer which features a 1GHz ARM Cortex-A8 processor and 512MB of RAM. It runs a custom Linux audio environment that gives you buffer sizes as small as 2 samples, producing latency as low as 1 millisecond from audio in to audio out, or even down to 100 microseconds from analogue in to analogue out. What's more, every analog and digital pin is automatically sampled at audio rate, providing precise, jitter-free alignment between audio and sensors.

What this means for you is that your digital musical instruments and interactive hardware just got a lot more responsive and expressive: Bela's speed and timing precision allow for natural, intuitive and immediate gestural control. Digital instrument design has never been this elegant.

## Using Bela

{% include single-image-research.html fileName="bela/connect_replaceme.png" %}


Connect Bela to your laptop via USB, bring up the dedicated on-board IDE in your browser and you can start coding right away in C++. Custom developer toolchains are also supported through a set of build scripts. Bela supports a lightweight and simple Arduino-like API that allows you to focus on the core functionality of your code. The IDE also includes a browser-based oscilloscope to visualise and debug your sensor and audio data in real time.


Alternatively, build patches for Bela in the powerful computer music programming environment Pure Data. We use Heavy Audio Tools from Enzien Audio to convert your Pd patch into optimised C code which is compiled to run natively on Bela.


When you are done developing you can unplug Bela from your laptop, power it with a battery, and embed it in your project, be it a musical instrument, interactive installation or kinetic sculpture. No laptop required.

## The Hardware 

{% include single-image-research.html fileName="bela/INTRO_hardware.png" %}


* Audio: 16-bit stereo audio I/O at 44.1kHz
* Audio power output: 2x 1W 8ohm speaker amplifiers (available when powered from DC jack)
* Analogue In: 8x 16-bit analogue inputs at 22.05kHz
* Analogue Out: 8x 16-bit analogue outputs at 22.05kHz
* Digital channels: 16x digital GPIO at 44.1kHz or 88.2kHz
* Analogue I/O is also software configurable to give 4 channels at 44.1kHz or 2 channels at 88.1kHz

## The Software 

{% include single-image-research.html fileName="bela/INTRO_software.png" %}

Bela runs a custom audio processing environment based on the Xenomai real-time Linux extensions. Your audio code runs in hard real-time, bypassing the entire operating system to go straight to the hardware. We have written a custom audio driver using the Programmable Realtime Unit (PRU), a microcontroller on the same chip as the BeagleBone Black CPU. This driver is capable of buffer sizes as small as 2 audio samples for very low latency, and its performance is not affected by other system load. No other embedded Linux platform can match this performance.

The Bela C++ API gives you a clean and lightweight way to write audio code. Fill in three functions: `setup()` runs at the beginning; `render()` runs once for each new audio buffer; `cleanup()` runs once at the end. All the analogue and digital pins are sampled automatically at audio rate, so sensor signals can be treated the same way as audio in your code. You can write your code using the browser-based IDE, or alternatively a set of build scripts let you use an editor of your choice and then compile the code on the board.

## Comparison to other tools 

{% include single-image-research.html fileName="bela/INTRO_comparison.png" %}

Bela combines the low-latency real-time performance of microcontrollers with the power and connectivity of embedded Linux computers. Through Bela's dedicated design we can achieve audio latency lower than even a high-end laptop.

