---
layout: communal-elections
title: Komunální volby v Plzni
campaignCategoryUid: plzen2018
candidateListUid: radnice # uid z `_candidates/radnice.md`
---

<section class="o-section o-section--spaceBot">
  <div class="o-section-inner">
    <div class="o-section-block">
      <div class="c-BasicPage">
        <div class="c-BasicPage-content">
          <h2>Kandidátky do městských částí:</h2>
{% assign regions = site.data.regions | sort: 'rank' %}
{% for region in regions %}
    {% if region.kontakt_id %}
        {% assign candidates = site.candidatelists | where: "uid", region.uid | first  %}
        <a href="/mestske-casti/{{region.uid}}.html">
            {{ region.full_name }} 
        </a>
        &ensp;
    {% endif %}
{% endfor %}
        </div>
      </div>
    </div>
  </div>
</section>
