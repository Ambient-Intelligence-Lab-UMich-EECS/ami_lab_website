---
title: Team
nav:
  order: 3
  tooltip: About our team
---

<style>
.team-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(118px, 118px));
  gap: 12px;
  align-items: start;
  margin: 0.45rem 0 1rem;
  justify-content: start;
}

.team-grid .portrait {
  margin: 0;
  width: 118px;
  max-width: 118px;
  padding: 8px;
}

.team-grid .portrait-image {
  margin-bottom: 10px;
}

.team-grid .portrait-name {
  font-size: 0.9rem;
}

.team-grid .portrait-description {
  font-size: 0.8rem;
}

h2 {
  margin-top: 1.2rem;
  margin-bottom: 0.45rem;
}

main > section p {
  margin-bottom: 0.7rem;
}
</style>

# {% include icon.html icon="fa-solid fa-users" %}Team

Meet the people building Ambient Intelligence systems across sensing, machine learning, systems, and human-centered applications.

{% include section.html %}

<div class="team-grid">
{% include list.html data="members" component="portrait" filter="role == 'principal-investigator'" suppress_affiliation=true style="small" %}
</div>

## PhD Students

<div class="team-grid">
{% include list.html data="members" component="portrait" filter="name == 'Linzhen Zhu'" suppress_affiliation=true style="small" %}
{% include list.html data="members" component="portrait" filter="name == 'Hyunmin Park'" suppress_affiliation=true style="small" %}
{% include list.html data="members" component="portrait" filter="name == 'Kailai Cui'" suppress_affiliation=true style="small" %}
{% include list.html data="members" component="portrait" filter="name == 'Leonard Zhang'" suppress_affiliation=true style="small" %}
</div>

## Master Students

<div class="team-grid">
{% include list.html data="members" component="portrait" filter="role == 'master'" suppress_affiliation=true style="small" %}
</div>

## Undergraduate Students

<div class="team-grid">
{% include list.html data="members" component="portrait" filter="role == 'undergrad'" suppress_affiliation=true style="small" %}
</div>

## Alumni
