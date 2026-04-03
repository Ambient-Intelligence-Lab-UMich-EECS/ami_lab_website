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
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20ultrasound%22%20%22tag%3A%20speech%22" class="tag" data-query='"tag: ultrasound" "tag: speech"'>acoustics</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20vision%22" class="tag" data-query='"tag: vision"'>light</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20radio-frequency%22" class="tag" data-query='"tag: radio-frequency"'>rf</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20vibration%22" class="tag" data-query='"tag: vibration"'>vibration</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20motion-sensor%22" class="tag" data-query='"tag: motion-sensor"'>motion sensors</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20biosignals%22" class="tag" data-query='"tag: biosignals"'>biosensors</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20multimodal%22" class="tag" data-query='"tag: multimodal"'>multi-modal</a>
</div>

### System Challenges
<div class="tags" data-group="system">
  <a href="{{ page.dir | relative_url }}" class="tag" data-query="">all</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20ultrasound%22%20%22tag%3A%20vision%22%20%22tag%3A%20radio-frequency%22%20%22tag%3A%20vibration%22%20%22tag%3A%20motion-sensor%22%20%22tag%3A%20biosignals%22%20%22tag%3A%20multimodal%22" class="tag" data-query='"tag: ultrasound" "tag: vision" "tag: radio-frequency" "tag: vibration" "tag: motion-sensor" "tag: biosignals" "tag: multimodal"'>extended sensing capabilities</a>
  <a href="{{ page.dir | relative_url }}?search=privacy" class="tag" data-query='privacy'>privacy</a>
  <a href="{{ page.dir | relative_url }}?search=security" class="tag" data-query='security'>security</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20wireless-communication%22" class="tag" data-query='"tag: wireless-communication"'>communication</a>
  <a href="{{ page.dir | relative_url }}?search=computation%20storage" class="tag" data-query='computation storage'>computation &amp; storage</a>
</div>

### Applications
<div class="tags" data-group="applications">
  <a href="{{ page.dir | relative_url }}" class="tag" data-query="">all</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20human-computer-interaction%22" class="tag" data-query='"tag: human-computer-interaction"'>hci</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20speech%22" class="tag" data-query='"tag: speech"'>speech processing</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20mobile-health%22" class="tag" data-query='"tag: mobile-health"'>health sensing</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20environmental-sensing%22" class="tag" data-query='"tag: environmental-sensing"'>environmental sensing</a>
  <a href="{{ page.dir | relative_url }}?search=%22tag%3A%20mobile-robotics%22" class="tag" data-query='"tag: mobile-robotics"'>robotic sensing</a>
  <a href="{{ page.dir | relative_url }}?search=sensor%20security" class="tag" data-query='sensor security'>sensor security</a>
  <a href="{{ page.dir | relative_url }}?search=privacy%20defense" class="tag" data-query='privacy defense'>sensor privacy attack and defense</a>
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
