---
title: Home
carousels:
  - images: 
    - image: /images/background.jpg
      # title: "First Slide Title"
    - image: /images/logo.jpg
    - image: /images/photo.jpg
---

## AmI (Ambient Intelligence) Lab Vision
Led by Prof. **[Ke Sun](https://samsonsjarkal.github.io/KeSun/)**, the AmI Lab was established in CSE of the EECS Department at the University of Michigan, Ann Arbor in January 2025.

We envision a future where our environments intuitively adapt in real-time to augment human abilities through **Ambient Intelligence (AmI)**. In this future, devices, sensors, and processors are seamlessly embedded into everyday objects and spaces, creating intelligent systems that proactively adjust to individual needs. 

Guided by this vision, the AmI Lab at UMich CSE focuses on developing **intelligent, cost-effective, deployable, human-centric, and trustworthy Mobile, Wearable, and IoT (MWIoT) systems**. Our research goals include:

- **Enable novel applications** through advanced sensing technologies; 
- **Advance computational sensing techniques** to enhance the capabilities and performance of MWIoT systems; 
- **Address system bottlenecks** in MWIoT ecosystems, ensuring efficiency and reliability.

{% include carousel.html height="40" unit="%" duration="5" number="1" %}

{% include section.html %}

{% capture col1 %}
## {% include icon.html icon="fa-solid fa-newspaper" %}Lab News

  {% assign sorted_news = site.data.news | sort: "date" | reverse %}
    {% for post in sorted_news limit:5 %}
    
  <div class="news-card">
    <div class="news-header">
        <span class="news-title">{{ post.title }}</span>
        <span class="news-date">{% include icon.html icon="fa-regular fa-calendar" %} {{ post.date | date: "%B %d, %Y" }} </span>
    </div>
    <div class="news-description">
        {{ post.description }} 
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

{% include cols.html col1=col1 %}
