---
title: Publications
nav:
  order: 2
  tooltip: Papers and highlighted publications
---

# {% include icon.html icon="fa-solid fa-scroll" %}Publications

<style>
.publication-filters h3 {
  font-size: 1rem;
  margin: 16px 0 8px;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.publication-filters .tags {
  justify-content: flex-start;
  gap: 8px;
  margin: 8px 0 14px;
}

.publication-filters .tag {
  padding: 4px 9px;
  font-size: 0.84rem;
}
</style>

<div class="publication-filters" markdown="1">

### Sensing Modalities
<div class="tags" data-group="sensing">
  <a href="{{ page.dir | relative_url }}" class="tag" data-query="">all</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20acoustics%22" class="tag" data-query='"tag: acoustics"'>acoustics</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20light%22" class="tag" data-query='"tag: light"'>light</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20rf%22" class="tag" data-query='"tag: rf"'>rf</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20vibration%22" class="tag" data-query='"tag: vibration"'>vibration</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20motion-sensors%22" class="tag" data-query='"tag: motion-sensors"'>motion sensors</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20biosensors%22" class="tag" data-query='"tag: biosensors"'>biosensors</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20multi-modal%22" class="tag" data-query='"tag: multi-modal"'>multi-modal</a>
</div>

### System Challenges
<div class="tags" data-group="system">
  <a href="{{ page.dir | relative_url }}" class="tag" data-query="">all</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20extended-sensing-capabilities%22" class="tag" data-query='"tag: extended-sensing-capabilities"'>extended sensing capabilities</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20privacy%22" class="tag" data-query='"tag: privacy"'>privacy</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20security%22" class="tag" data-query='"tag: security"'>security</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20communication%22" class="tag" data-query='"tag: communication"'>communication</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20computation-%26-storage%22" class="tag" data-query='"tag: computation-&-storage"'>computation &amp; storage</a>
</div>

### Applications
<div class="tags" data-group="applications">
  <a href="{{ page.dir | relative_url }}" class="tag" data-query="">all</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20hci%22" class="tag" data-query='"tag: hci"'>hci</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20speech-processing%22" class="tag" data-query='"tag: speech-processing"'>speech processing</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20health-sensing%22" class="tag" data-query='"tag: health-sensing"'>health sensing</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20environmental-sensing%22" class="tag" data-query='"tag: environmental-sensing"'>environmental sensing</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20robotic-sensing%22" class="tag" data-query='"tag: robotic-sensing"'>robotic sensing</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20sensor-security%22" class="tag" data-query='"tag: sensor-security"'>sensor security</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20sensor-privacy-attack-and-defense%22" class="tag" data-query='"tag: sensor-privacy-attack-and-defense"'>sensor privacy attack and defense</a>
</div>

### Venue Areas
<div class="tags" data-group="venue">
  <a href="{{ page.dir | relative_url }}" class="tag" data-query="">all</a>
  <a href="{{ page.dir | relative_url }}?search=%22MobiCom%22%20%22IMWUT%22%20%22MobiSys%22%20%22TMC%22" class="tag" data-query='"MobiCom" "IMWUT" "MobiSys" "TMC"'>mobile computing</a>
  <a href="{{ page.dir | relative_url }}?search=%22UIST%22%20%22IMWUT%22%20%22MobiSys%22" class="tag" data-query='"UIST" "IMWUT" "MobiSys"'>human computer interaction</a>
  <a href="{{ page.dir | relative_url }}?search=%22S%26P%22%20%22NDSS%22" class="tag" data-query='"S&P" "NDSS"'>security and privacy</a>
  <a href="{{ page.dir | relative_url }}?search=%22NSDI%22%20%22INFOCOM%22%20%22SenSys%22" class="tag" data-query='"NSDI" "INFOCOM" "SenSys"'>computer networks</a>
  <a href="{{ page.dir | relative_url }}?search=%22AAAI%22" class="tag" data-query='"AAAI"'>ml/ai</a>
</div>
</div>

{% include list.html data="citations" component="citation" style="rich" %}

{% include search-info.html %}
