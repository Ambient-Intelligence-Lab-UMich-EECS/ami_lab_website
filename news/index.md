---
title: News
nav:
  order: 5
  tooltip: Lab news and updates
---


{% capture col1 %}
###  {% include icon.html icon="fa-solid fa-newspaper" %} News and updates

{% assign sorted_news = site.data.news | sort: "date" | reverse %}
    {% for post in sorted_news %}
    
  <div class="news-card">
    <div class="news-header">
        <span class="news-title">{{ post.title | markdownify | remove: "<p>" | remove: "</p>" }}</span>
        <span class="news-date">{% include icon.html icon="fa-regular fa-calendar" %} {{ post.date | date: "%b %Y" }} </span>
    </div>
    <div class="news-description">
        {{ post.description }} 
            {% if post.links %}
              {% for item in post.links %}
                {% assign news_link_icon = "fa-solid fa-globe" %}
                {% if item.label == "Video demo" or item.url contains "youtube.com" or item.url contains "youtu.be" %}
                  {% assign news_link_icon = "fa-brands fa-youtube" %}
                {% endif %}
                <a href="{{ item.url }}" target="_blank">{% include icon.html icon=news_link_icon %} {{ item.label }}</a>
              {% endfor %}
            {% elsif post.url %}
              {% assign news_link_label = "Website" %}
              {% assign news_link_icon = "fa-solid fa-globe" %}
              {% if post.url contains "youtube.com" or post.url contains "youtu.be" %}
                {% assign news_link_label = "Video demo" %}
                {% assign news_link_icon = "fa-brands fa-youtube" %}
              {% endif %}
              <a href="{{ post.url }}" target="_blank">{% include icon.html icon=news_link_icon %} {{ news_link_label }}</a>
            {% endif %}
    </div>
  </div>

    {% endfor %}  

{% endcapture %}

{% include cols.html col1=col1 %}
