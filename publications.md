---
layout: single
author_profile: true
title: Publications
---

<!-- NOTE: The trailing spaces give newlines! Don't delete/format them -->

{% if site.data.publications.preprints %}
## Preprints

{% assign paperlist = site.data.publications.preprints %}
<table class="publications"><tbody>
  {% for paper in paperlist %}
    {% include publication_item.html %}
  {% endfor %}
</tbody></table>
{% endif %}

## Journal papers

{% assign paperlist = site.data.publications.journal_papers %}
<table class="publications"><tbody>
  {% for paper in paperlist %}
    {% include publication_item.html %}
  {% endfor %}
</tbody></table>

## Top-tier AI/ML Conference papers

{% assign paperlist = site.data.publications.top_tier_ml_papers %}
<table class="publications"><tbody>
  {% for paper in paperlist %}
    {% include publication_item.html %}
  {% endfor %}
</tbody></table>

## Conference papers

{% assign paperlist = site.data.publications.conference_papers %}
<table class="publications"><tbody>
  {% for paper in paperlist %}
    {% include publication_item.html %}
  {% endfor %}
</tbody></table>

## Top-tier Conferences & Workshops with Extended Abstracts

{% assign paperlist = site.data.publications.top_tier_abstracts %}
<table class="publications"><tbody>
  {% for paper in paperlist %}
    {% include publication_item.html %}
  {% endfor %}
</tbody></table>

## Workshops and Conference abstracts

{% assign paperlist = site.data.publications.conference_abstracts %}
<table class="publications"><tbody>
  {% for paper in paperlist %}
    {% include publication_item.html %}
  {% endfor %}
</tbody></table>
