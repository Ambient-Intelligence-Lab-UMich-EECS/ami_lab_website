---
title: Home
carousels:
  - images: 
    - image: /ami_lab_website/images/25UIST_ultraposer.gif
      title: "UltraPoser: IMU-based Full-Body Pose Estimation with Ultrasound Sensing on Consumer Wearables (UIST'25)"
    - image: /ami_lab_website/images/eveguard.png
      title: "EveGuard: Defeating Vibration-based Side-Channel Eavesdropping with Audio Adversarial Perturbations (S&P'25)"
---

## AmI (Ambient Intelligence) Lab
We are a research lab at in CSE of the EECS Department at the University of Michigan, Ann Arbor led by Prof. **[Ke Sun](https://samsonsjarkal.github.io/KeSun/)**. We envision a future where our environments intuitively adapt in real-time to augment human abilities through **Ambient Intelligence (AmI)**. In this future, devices, sensors, and processors are seamlessly embedded into everyday objects and spaces, creating intelligent systems that proactively adjust to individual needs. Guided by this vision, the AmI Lab focuses on developing **intelligent, cost-effective, deployable, human-centric, and trustworthy Mobile, Wearable, and IoT (MWIoT) systems**.

{% capture col1 %}

Our research goals include:

- **Enable novel applications** through advanced sensing technologies; 
- **Advance computational sensing techniques** to enhance the capabilities and performance of MWIoT systems; 
- **Address system bottlenecks** in MWIoT ecosystems, ensuring efficiency and reliability.

{% endcapture %}

{% capture col2 %}

## Research Highlight

{% include carousel.html height="60" unit="%" duration="5" number="1" %}

{% endcapture %}

{% include section.html %}

{% capture col1 %}
## {% include icon.html icon="fa-solid fa-newspaper" %}Lab News

  {% assign sorted_news = site.data.news | sort: "date" | reverse %}
    {% for post in sorted_news limit:4 %}
    
  <div class="news-card">
    <div class="news-header">
        <span class="news-title">{{ post.title }}</span>
        <span class="news-date">{% include icon.html icon="fa-regular fa-calendar" %} {{ post.date | date: "%B %d, %Y" }} </span>
    </div>
    <div class="news-description">
            {% if post.url %}
            <a href="{{ post.url }}" target="_blank">More...</a>
            {% endif %}
    </div>
  </div>

    {% endfor %}  
  
{%
  include button.html
  link="news"
  text="Read all news"
  icon="fa-solid fa-arrow-right"
  flip=true
  align=left

%}

{% endcapture %}

{% include cols.html col1=col1 col2=col2%}
