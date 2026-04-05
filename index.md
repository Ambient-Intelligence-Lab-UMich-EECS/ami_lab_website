---
title: Home
carousels:
  - images: 
    - image: images/moirelens.gif
      title: "MoiréLens: Bringing Schlieren Imaging into Real-World Environments Using Moiré Patterns (SenSys'26)"
      link: https://ambient-intelligence-lab-umich-eecs.github.io/MoireLens-Page/
    - image: images/earcardio.gif
      title: "EarCardio: Unlocking Practical Cardiac Monitoring Capabilities on True Wireless Stereo Earbuds (MobiCom'26)"
      link: https://www.youtube.com/watch?v=FrSbxhM5yII
    - image: images/magicpatch.gif
      title: "MagicPatch: Attacking mmWave Imaging Using Metasurfaces Based on Intensity and Time-of-Flight Manipulation (MobiCom'26)"
      link: https://www.youtube.com/watch?v=Vgy-u9HlQOo
    - image: images/25UIST_ultraposer.gif
      title: "UltraPoser: IMU-based Full-Body Pose Estimation with Ultrasound Sensing on Consumer Wearables (UIST'25)"
      link: https://github.com/leeyadong/UltraPoser
---

<style>
.home-main-grid,
.home-sub-grid {
  display: grid;
  gap: 1.5rem;
  align-items: start;
  margin: 1.25rem 0;
}

.home-main-grid {
  grid-template-columns: minmax(0, 1.7fr) minmax(280px, 0.8fr);
}

.home-side-list {
  display: flex;
  flex-direction: column;
  gap: 0.65rem;
  align-self: start;
}

.home-left-column {
  min-width: 0;
}

.home-main-grid > div > :first-child,
.home-sub-grid > div > :first-child,
.home-side-list > :first-child {
  margin-top: 0 !important;
}

.home-side-list .news-card {
  margin-bottom: 0;
  padding: 0.65rem 0.8rem;
  border-radius: 8px;
}

.home-side-list .news-header {
  flex-direction: column;
  align-items: flex-start;
  gap: 0.2rem;
}

.home-side-list .news-title {
  font-size: 0.94rem;
  line-height: 1.25;
  font-weight: 400;
}

.home-side-list .news-title strong {
  font-weight: 700;
}

.home-side-list .news-date,
.home-side-list .news-description {
  font-size: 0.84rem;
}

.home-compact-list p,
.home-compact-list ul {
  margin-bottom: 0.35rem;
}

.home-compact-list ul {
  padding-left: 1.1rem;
}

.home-compact-list li {
  margin-bottom: 0.2rem;
}

.home-left-column > p {
  margin-bottom: 0.5rem;
  line-height: 1.45;
}

.home-left-column .home-sub-grid {
  margin-top: 0.75rem;
}

.home-left-column .home-compact-list p {
  margin-top: 0.1rem;
  margin-bottom: 0.1rem;
  line-height: 1.5;
}

.home-left-column .home-compact-list ul {
  margin-top: 0.05rem;
  margin-bottom: 0.05rem;
}

.home-left-column .home-compact-list li {
  margin-bottom: 0.15rem;
  line-height: 1.3;
}

.home-main-grid .carousel__holder,
.home-sub-grid .carousel__holder {
  margin: 0.35rem 0 0.5rem;
}

.home-side-list h2,
.home-side-list h3,
.home-left-column h2,
.home-left-column h3,
.home-main-grid h2,
.home-main-grid h3,
.home-sub-grid h2,
.home-sub-grid h3 {
  margin-top: 0;
  margin-bottom: 0.6rem;
}

.home-left-column > h2 {
  padding-left: 0;
}

@media (max-width: 900px) {
  .home-main-grid,
  .home-sub-grid {
    grid-template-columns: 1fr;
  }
}
</style>

<div class="home-main-grid">
  <div class="home-left-column" markdown="1">

## AmI (Ambient Intelligence) Lab
AmI Lab is in CSE at the University of Michigan led by Prof. **[Ke Sun](https://samsonsjarkal.github.io/KeSun/)**. We build AI-native computational sensing systems for mobile, wearable, IoT, and robotic platforms. Our research centers on three questions:

{% capture col1 %}

- **How can off-the-shelf sensors be repurposed to achieve extended sensing capabilities?**
- **How can we address the systems challenges of emerging AI-native sensing systems?**
- **How can sensing systems be designed to better support everyday life?**

{% endcapture %}

{% capture col2 %}

{% endcapture %}

<div class="home-sub-grid">
  <div class="home-compact-list">{{ col1 | markdownify }}</div>
  <div class="home-compact-list">{{ col2 | markdownify }}</div>
</div>

## Recent Research Highlight

{% include carousel.html height="58" unit="%" duration="5" number="1" %}

If you are interested in the AmI Lab's ongoing research projects, please visit the [Research page]({{ "/research/" | relative_url }}).
  </div>
  <div class="home-side-list" markdown="1">

## {% include icon.html icon="fa-solid fa-newspaper" %}Lab News

{% assign sorted_news = site.data.news | sort: "date" | reverse %}
{% for post in sorted_news limit:6 %}

<div class="news-card">
  <div class="news-header">
    <span class="news-title">{{ post.title | markdownify | remove: "<p>" | remove: "</p>" }}</span>
    <span class="news-date">{% include icon.html icon="fa-regular fa-calendar" %} {{ post.date | date: "%b %Y" }}</span>
  </div>
  {% if post.url %}
    <div class="news-description">
      {% if post.links %}
        {% for item in post.links %}
          {% assign news_link_icon = "fa-solid fa-globe" %}
          {% if item.label == "Video demo" or item.url contains "youtube.com" or item.url contains "youtu.be" %}
            {% assign news_link_icon = "fa-brands fa-youtube" %}
          {% endif %}
          <a href="{{ item.url }}" target="_blank">{% include icon.html icon=news_link_icon %} {{ item.label }}</a>
        {% endfor %}
      {% else %}
        {% assign news_link_label = "Website" %}
        {% assign news_link_icon = "fa-solid fa-globe" %}
        {% if post.url contains "youtube.com" or post.url contains "youtu.be" %}
          {% assign news_link_label = "Video demo" %}
          {% assign news_link_icon = "fa-brands fa-youtube" %}
        {% endif %}
        <a href="{{ post.url }}" target="_blank">{% include icon.html icon=news_link_icon %} {{ news_link_label }}</a>
      {% endif %}
    </div>
  {% endif %}
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

</div>
</div>
