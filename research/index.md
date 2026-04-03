---
title: Research
nav:
  order: 1
  tooltip: Published works
---

# {% include icon.html icon="fa-solid fa-microscope" %}Research

AmI Lab studies AI-native computational sensing systems that are intelligent, deployable, and human-centric across mobile, wearable, IoT, and robotic platforms.

{% capture col1 %}

**Core research questions**
- How can off-the-shelf sensors be repurposed to unlock extended sensing capabilities?
- How can emerging sensing systems remain accurate, robust, and practical in real deployments?
- How can sensing systems better support everyday life across health, interaction, and environment?

**Application domains**
- Human-computer interaction and ubiquitous computing
- Mobile health and wellbeing
- Environmental sensing
- Mobile robotics, autonomy, and wireless systems

{% endcapture %}

{% capture col2 %} 

**Technical layers**
- Novel sensing with RF, ultrasound, acoustic, biopotential, vibration, and multimodal systems
- Computational models that are accurate, robust, intelligent, and personalized
- Systems support for efficiency, deployability, trustworthiness, and privacy preservation

**Recent directions**
- New sensing technologies: MoiréLens, EarCardio, UWB-Prac, SoilNutri, UltraPoser
- AI-native systems challenges: KDC, RFCanvas, EveGuard, MagicPatch, LCCT, Magmaw

{% endcapture %}

{% include cols.html col1=col1 col2=col2 %} {% include section.html %}

## Highlighted

{% include citation.html lookup="MoiréLens" style="rich" %}

{% include citation.html lookup="EarCardio" style="rich" %}

{% include citation.html lookup="UltraPoser" style="rich" %}

{% include citation.html lookup="EveGuard" style="rich" %}

{% include section.html %}

## All

{% include search-box.html %}

{% include search-info.html %}

{% include list.html data="citations" component="citation" style="rich" %}
