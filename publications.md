---
layout: single
author_profile: true
title: Publications
---

<!-- NOTE: The trailing spaces give newlines! Don't delete/format them -->

## Journal papers

{% assign paperlist = site.data.publications.journal_papers %}
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

## Conference abstracts

{% assign paperlist = site.data.publications.conference_abstracts %}
<table class="publications"><tbody>
  {% for paper in paperlist %}
    {% include publication_item.html %}
  {% endfor %}
</tbody></table>