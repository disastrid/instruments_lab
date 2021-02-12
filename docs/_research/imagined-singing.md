---
layout: research
title:  "Imagined Singing: Sensing Musical Imagery and Intention in Vocalists"
tag: "new-interfaces"
tagline:  PhD Research, Courtney N. Reed
thumb: electrodes-thumb.png
authors: "Courtney Reed"
main-image: /images/research/imagined-singing/debussyvoxscore.png
para:  Sensing Intention, Imagery, and Bodily Relationships with sEMG
links: ["https://courtneynreed.wordpress.com/"]
link-names: ["Personal Website"]
---

The voice as an instrument is highly personal and exists wholly within the body. As such, vocalists must rely heavily on detailed metaphors, bodily sensations, and abstract representations of the physiological processes of singing. This research aims to better understand how these internal representations are used by vocalists and to develop sensory tools to detect such useage. Mainly, we focus on measuring the application of musical imagery in low-level muscular movement. This research will explore how body-based relationships vocalists have with their instrument and aspects of technical and expressive performance can be observed in the body. As well, we explore how the body responds when a vocalist’s imagination, intention, and interaction goals change. Additionally, the tools we develop and use to measure aspects of imagery in vocal performance will become studies in their own right, as interfaces for musical expression through which we can observe how vocalists use imagery to not only adapt to but also control various aspects of expressive musical performance.

___

## The Role of Musical Imagery in Vocal Performance

Musical imagery - that is, the ability to imagine the multimodal aspects of a musical activity without or prior to actually perceiving it - helps to shape our interaction and performance. In addition to improving coordination and timing and communication of emotional and musical expression, imagery allows for the mental rehearsal and audiation needed in musical practice. Imagining and executing an action result in similar neural activation; musical imagery and the imagination of musical events both utilise and strengthen neural links.

An initial study exploring the impact of auditory imagery in singers' ability to maintain tonal and temporal accuracy, while both singing aloud and audiating, revealed the importance of imagery and sensorimotor systems in performance. 16 singers were invited to sing an unaccompanied piece of their own choosing against altered auditory feedback (AAF), including delays and pitch shifts. Results suggest auditory imagery ability has a significant effect on singers' ability to avoid tonal drift while singing with pitch-shifted AAF. However, auditory imagery was not found to have a significant effect on temporal accuracy; rather, singers appear to cope with timing distractions using body sway, foot tapping, and other tactile adaptations. This highlights the importance of bodily sensations, in addition to imagery, in performance. This study informed how vocalists are able to use mind and body-based representations in performance, to be used in examination of vocal practice.

Because of the difficulty in physically examining the vocal apparatus, much of vocal pedagogy relies on abstract language and metaphor to teach fundamental vocal technique. We are currently exploring the role of metaphor and underlying behavior in vocal technqiue through an interview-based study with vocal coaches and private teachers. We hope to use the experience of these teachers to determine how sensory-based interaction through the body can be translated through linguistic metaphor. 

More information on this ongoing study can be found HERE. If you are a vocal educator and are interested in participating in our study, please contact Courtney at . <a href="mailto:c.n.reed@qmul.ac.uk">c.n.reed@qmul.ac.uk</a> 

{% include single-image-research.html fileName="imagined-singing/electrode-place-2.JPG" caption="Electrodes placed on the suprayhoid muscles, which activate frequently while singing" %}

___

## Designing a Controller for Direct Vocal Interfacing

Although highly personal to the vocalist and situated within the body, the voice is removed for others. Sensations and the relationship between body and mind drive the vocal interaction; but, how do we relate to something which we normally interact with only through sensation? A vocalist can feel through their technique, but this is largely hidden within the body and obscured from view. As a result, vocal analysis and interpretation, even in vocal pedagogy, is largely audio-based - we react to what is heard. While techniques for audio feature exctraction in vocal interaction have improved greatly over recent years, many elements of vocal technique and the sensory information driving the vocalist's own behaviour and interaction with their voice are lost in translation. Expression and embellishment are difficult to detect; even more dangerous, harmful vocal practices may go unnoticed or even be encouraged through this kind of analysis, which could lead to physiological damage. Therefore, the focus of this research is to turn away from audio-only analysis and focus on the vocal source and embodied sensations vocalists rely on. 

For this, we propose the use of surface electromyography (sEMG) as a way of interfacing with vocal musculature. sEMG detects the activation of muscles by measuring the electrical neural impulse which causes muscles to contract. We have developed a system for extraction of sEMG signals from the extrinsic (externally-located) laryngeal muscles. sEMG is useful in that, not only can it provide information about performance without need for audio analysis, but also that it can detect subvocalised (unvoiced) movement, such as is present in audiation. This allows for an inquiry into the use of musical imagery during both executed and imagined practice. Furthermore, the electrical neural impulses are a precursor to detectable movement. This means sEMG provides a way to look at the intention of a performer and reduce system latency.

The design was driven through autobiographical design for both third- and first-person interaction perspectives. From a third-person point of view, we have found that sEMG is able to detect both vocalised and subvocalised singing during sung and imagined exercises, respectively. Third-person views of the vocal musculature allow for data to be collected about the activation patterns and tension during different exercises. We are currently exploring different filtering methods for the sEMG signal and working on detection of imagined versus executed action.

- link to Git repo
- photos from NIME paper

-  Courtney N. Reed and Andrew P. McPherson. 2020. Surface Electromyography for Direct Vocal Control. Proc. New Interfaces for Musical Expression (NIME), Royal Birmingham Conservatoire, Birmingham, UK. <br><a href="http://instrumentslab.org/data/courtney/NIME2020_final.pdf">Download PDF</a>

{% include single-image-research.html fileName="imagined-singing/v2.2-sch.png" caption="Circuit for sEMG signal acquisition and amplification." %}
___

## First-Person Interaction and Autobiographical Design

In addition to the traditional third-person view point of the sensor, sEMG provides a unique resource for third-person interaction. Because the interaction comes from the body, this sensing is ideal for the study of embodied technique and designing for sensation-based systems. Through autobiographical design by Courtney, with 10+ years of semi-professional vocal performance experience to apply in use of the system, we can design in ways which are not disruptive to singing practice but allow the vocalist to explore the system in first-person interaction.

From a first-person interaction perspective, the user is made aware of their own movement. In the case of sEMG, this is often movement which is not completely conscious or has become automated through years of experience. Posture, alignment, breathing, and other internalised techniques which have become natural and automatic over time suddenly are brought to attention through sonification. This allows vocalists to explore their own technique and provides a way to observe movement in real-time. Vocalists are able to modify and challenge their internalised behavior; through interaction with the system over long time periods (1+ years), we have found that some old habits do not die hard - old techniques which have been drilled into performance over time are subverted and adapted in the context of this new interaction.

The use of sEMG thus provdes a foundation for creative interaction, where vocalists can use their pre-existing technique to control various aspects of performance. We use this signal in computer-music languages such as SuperCollider to map muscular activations to parameters of vocal processing. As well, because sEMG provides feedback for covert movements, we are keen to explore the applications of using sEMG as a teaching resource in vocal pedagogy and music education. Biofeedback in this sense can provide a better way for teachers and students to understand each other and help to reinforce healthy vocal practice.

- Courtney N. Reed and Andrew P. McPherson. 2021. Surface Electromyography for Sensing Performance Intention and Musical Imagery in Vocalists. In Fifteenth International Conference on Tangible, Embedded, and Embodied Interaction (TEI ’21), February 14–17, 2021, Salzburg, Austria. ACM, New York, NY, USA, 11 pages. https://doi.org/10.1145/3430524.3440641 <br><a href="https://doi.org/10.1145/3430524.3440641">Download PDF</a> 

- 