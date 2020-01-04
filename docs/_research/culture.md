---
layout: research
title:  "Instrument Design as Cultural Negotiation"
tag: "Musician Studies"
tagline: PhD research Giacomo Lepri
thumb: culture/music-instruments02.png
authors: "Giacomo Lepri"
main-image: /images/research/culture/straw.jpg
production-date: 2017 - present
para: On the multiple origins of new musical instruments
links: ["http://www.giacomolepri.com"]
link-names: ["Personal website"]
---
<!--{% include single-image-research.html fileName="culture/music_research.jpg" %}-->

##### Remediation

The notion of Remediation has been sketched by McLuhan in his theory of Media and further developed by Bolter & Grusin. Remediation can be defined as the formal logic by which new media refashion prior media forms. This implies that characteristics typical of an existing media are translated into the new designs. For instance, modular synths often remediate prior radio technology which remediate early electromagnetic measurement technology. The process of remediation does not only related to physical and material features but it also concern the transfer of more abstract knowledge and cultural notions. Within the context of music technology, Wester tuning is probably one of the most remediated musical notions. It indeed provided the basis for the development of the MIDI communication protocol.

Considering the genesis of new musical instruments through the perspective of mediation it is possible to argue that new design often remediate physical properties and cultural paradigms already associated to existing devices. Magnusson argues that "what new instruments translate from earlier technologies are not simply the simulation of an interface, but a whole constellation of embodied contexts". Within this constellation we include the values, imaginaries and concerns inherited from communities of practice.

___
___

##### On the influences of communities and musical backgrounds

{% include single-image-research.html fileName="culture/WorkshopLab01.jpg" caption="Musicians making fictional musical instruments - As if by Magic workshop, Genoa, Italy, March 2018" %}

To explore how diverse musical backgrounds might influence the understanding of music technology we ran a value discovery exercise exploring the breadth of perspectives different communities might have in relation to the values inscribed in fictional technologies for musical interaction. We conducted a hands-on activity in which musicians active in different contexts were invited to envision not-yet-existent musical instruments. The outcomes revealed several sources of influence on participants’ artefacts, including cultural background, instrumental training, and prior experience with music technology. Overall the research highlighted the importance of cultural awareness and value rationality for the design of interactive systems within and beyond the musical domain.

___

***As If By Magic workshop***

Our work builds on Kristina Andersen’s Magic Machines workshops in which the notion of Magical Unknown is exploited to free a participant’s imagination
and generate manifestations of unknown technologies. Our workshop is therefore based on the idea that “embodied making processes facilitate a different form of thinking”. Through the act of building, narratives entailing the maker’s intentions, motivations and feelings can emerge. However, compared to the work of Andersen, our approach is more focused in the emergence of existing musical values and instrumental concerns rather then provoking new disruptive ideas and designs.

- **Write down a relevant aspect of your instrumental musical practice**
- **Draw one sonic element of a music you particularly enjoy playing or listening to**
- **Build the machine that addresses the sound you drew or the words you wrote**

{% include two-image-include.html left_image="Machine01.png" right_image="Machine03.png" image_subfolder="research/culture" caption=" From left to right: (1) AntennaLele - an ukulele like instrument with a bendable neck. The designer focused on the alteration of a specific element (guitar neck) in order to accurately “shape harmonies and melodies”. (2) SonicAlarm - a wire based instrument with attachments to be loosely hooked to both upper and lower limbs. The artefacts emphasises the notions of low control and stochastic behaviour. (3) No name - A string instrument that can only play notes with prime number frequencies, to produced “optimally dissonant” sounds. (4) Space Vibrator - a “plinky sort of instrument” (i.e. a funny string instrument) that turned out to be a really badly made spaceship."%}

{% include single-image-research.html fileName="culture/Machine02.png" caption="From left to right: (1) Orchestra - the conductor interacting with a musician of the orchestra. In this artefact the instrument disappears (transparent mediation technology) and the ideas of communication and interplay are privileged. (2) CorpoSuono - An organ like instrument with tubes filtering the air and a stopper to close them. The artefact focuses on the notion of timbre manipulation."%}

- G. Lepri and A. P. McPherson. [Making Up Instruments: Design Fiction for Value Discovery in Communities of Musical Practice.](http://instrumentslab.org/data/giacomo/2019DISFinal.pdf) Proc. ACM Designing Interactive Systems (DIS), San Diego, Californis, USA. 2019.

___

***Fictional artefacts - real values***

We then ran an online survey targeting musicians and technologists with experience in musical interface design. We recruited the participants using academic mailing lists (NIME and SMC) and social networks. We aimed to see if respondents could discover musical values through the artefacts created during the various As If by Magic workshops and link them to specific aesthetics and communities. Survey participants reviewed an image of eachfictional instrument and a short description of it provided by its creator. The survey asked the following open questions:

>What kind of musical style/genre do you think the musician plays? Why do you think that?
>What instrument(s) do you think this musician plays? Why?

Overall, our participants were rather successful in guessing the genre/style of the artefacts' creators: 44% of answers were correct, and a further 27% partly correct. In particular we were impressed by the overall ability of the survey respondents to discover the multiplicity of cultural sources and musical practices in the designer's background. Besides technical expertise, the design of a music technology entails the materialisation of purposes, assumptions and values. These are situated factors, emerging from specific communities, contexts and cultures. This research provides us the possibility to engage with this type of knowledge: context-dependent values emerging from situated practices.

- G. Lepri and A. P. McPherson. [Fictional Instruments, Real Values: Discovering Musical Backgrounds with Non-Functional Prototypes.](http://www.nime.org/proceedings/2019/nime2019_024.pdf) Proc. New Interfaces for Musical Expression, Porto Alegre, Rio Grande do Sul, Brazil. 2019.

___
___

##### A practice based account

***Chowndolo***

The Chowndolo is an Interactive Sonic Sculpture based on a magnetic pendulum whose trajectories are altered by magnets placed underneath the device. This creates unstable patterns of oscillation which are translated into synthesis parameters and sound. The Chowndolo was conceived as an interactive experience: the scuplture can be played like an instrument and audience participation is crucial. The magnets below the pendulum can be arranged to compose new shapes: different configurations will modify the pendulum oscillations and the generated sonorities. The unstable patterns produced by the pendulum oscillations are transformed into sound, articulating a music that evolves based on the pendulum’s motion.

The magnetic fields and their interactions are revealed through nuanced tones, acting as counterpoint to the pendulum’s dance. The installation aims to make visible the invisible, letting us feel forces that we are not able to perceive. The sounds generated are entirely based on FM synthesis whose sound parameters are controlled by sensing the variations in the magnetic field. According to Faraday’s law of induction, a variation in the magnetic field generates an induced electromagnetic force. This force is then amplified by a custom-designed preamp and the resulting signal is sent to a Bela board where it is processed before the audio being sent to the output.

The Chowndolo is a tribute to John Chowning, a pioneer in the field of Computer Music mostly known for his electroacoustic compositions, the discovery of FM synthesis and research on voice and instrument synthesis. During the development of the Chowndolo, we were lucky enough to welcome John Chowning to our lab and show him the project. He provided precious comments for the improvement of both the sensing technique and the FM synthesis implementation.

{% include vimeo.html vimeo="325707625" %}

___

***Cembalo Scrivano***

Cembalo Scrivano: an interactive audio-visual installation based on an augmented typewriter. By detecting the user's typing activity, the CS1 generates in realtime audio and visual materials. The project is inspired by the writing machine created in 1855 by the Italian inventor Giuseppe Ravizza. Ravizza called his invention Cembalo Scrivano (Scribe Harpsichord) due to the usage of piano-keys. This invention reworks the harpsichord interface: an existing musical instrument was used as source of inspiration for the development of a new machine (from art technology to typewriting).

The piece aims to mirror this process: a typewriter is converted into an interactive art installation (from typewriting to art technology). Oscillating between two domains (musical and literary), the same technology travels across history, carrying knowledge, behaviours and meanings. In media theory, the practice to understand new and emerging technologies by taking into account the history and evolution of past new media often relate to media archaeology studies. These cultural studies focus on the critical scrutiny of forgotten technologies, observing that new media often renovate old interactive paradigms and communication techniques. Media Archaeology is also a methodology for contemporary artistic practice introducing the concept of 'zombie media': a media that is not only out of use, but resurrected to new uses, contexts and adaptations.

{% include youtube.html youtube="o9BE7N6ER5w" %}

-  G. Lepri and A. P. McPherson. [First-person Research in the Arts: Exploring the Values Behind New Music Technology.](http://instrumentslab.org/data/giacomo/lepri_updated2.pdf) Proc. ACM Designing Interactive Systems (DIS), San Diego, Californis, USA. 2019.

- G. Lepri, A. P. McPherson. [Mirroring the past, from typewriting to interactive art: an approach to the re-design of a vintage technology.](http://www.nime.org/proceedings/2018/nime2018_paper0069.pdf). Proc. New Interfaces for Musical Expression, Blacksburg, Virginia, USA. 2018.

<!--

##### On our own influences: a first person account

> ***Workshop Structure***

{% include single-image-research.html fileName="culture/Machine03.png" %}

### Background

It is possible to argue that any musical technology embodied a set of pre-existing knowledge (e.g. technical expertise, musical notions and performative intentions). A luthier (instrument makers), while designing an instrument, transfers into the object specific cultural knowledges and musical meanings.

Likewise, musicians can be considered influential vectors through witch musical values are conveyed within communities. The involvement into specific musical communities implies ways of learning - of both absorbing and being absorbed in - the culture of practice. The roles played by music practitioners active in particular contexts seems therefore crucial for the generation and reproduction of cultural values that influence the understanding and use of music technologies.

### Aims

This research aims to explore how diverse musical backgrounds related to communities of musical practice influence the foresee of music technology. Drawing on HCI approaches and methodologies such as Design Fiction, Value Sensitive Design and Participatory Design, we aim to develop a body of knowledge for the discovery of musical values related to specific musical communities.

The exploration of the communities engaged with the invention and mediation of new musical instruments are also considered. We therefore aim to identify tacit assumptions on the ways designers use the available technologies while building new musical instruments. Furthermore, our goal is to elaborate on the question "Who controls who?". Thus, discussing the relations between tools, musical intentions and technical expertise within the instrument design tendencies situated in the NIME communities.

The body of knowledge and skill acquired will hopefully converge in the design of instruments conceived for specific musical values. Thus addressing specific musicians active in diverse communities of musical practice.

### Key concepts

Notions such as corporeal intentionality and embodied interaction are considered as core aspects of musical expressiveness. From this viewpoint, designers of New Interface for Musical Expression inherit a centuries-old body of knowledges and practices. New instruments are often discussed in relation to traditional instruments. This suggests that historical and cultural practices are easily projected into the design of the new instruments.

This research is grounded on the idea that new media re-mediates old media. The design of a novel instrument can be approached as a migration process in which features associated with existing musical technologies are integrated and negotiated into a new context. Thus we envision instrumented design cultures as sedimented and layered, a fold of time and materiality where the past might be suddenly discovered anew.

#### Media Archaeology

In media theory, the attempts to understand new and emerging technologies by taking into account the history and evolution of past new media is dened as media archaeology These cultural studies focus on the critical scrutiny of forgotten technologies, observing that new media often renovate old interactive paradigms and communication techniques. Media Archaeology is also a methodology for contemporary artistic practice introducing the concept of 'zombie media': a media that is not only out of use, but resurrected to new uses, contexts and adaptations.

-->
