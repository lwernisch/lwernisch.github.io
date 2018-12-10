---
layout: page
title: Publications
#description: "Peer-reviewed publications"
header-img: images/20180506-_MG_0228.jpg
comments: false
modified: 2018-10-01
---

More publications can be found on [Google Scholar](https://scholar.google.com/citations?user=1Ed4ZMYAAAAJ)

## Selected publications
-----

<div class='panel-pub'>
<ol>
{% for article in site.data.selected_publications_short.references %}
    <li>
    <div class="title">
    <span class="title">{{ article.title }}</span>
    {% if article.fulltext %}
        <a title="fulltext" href="{{ site.url }}/downloads/journal/{{ thesis.fulltext }}"><i class="fa fa-file-pdf-o"></i></a>
    {% endif %}
    </div>
    <div class='author'>
    {% for author in article.author %}
        <span class='{{ author.role }}'>{{ author.family }}, {{ author.given }}{% if author.role contains 'corr' %}*{% endif %}; </span>
    {% endfor %}
    </div>
    <div class="pubinfo">
    <span class="source">{{ article.container-title }} </span>
    <span class="year">{{ article.issued[0].year }},</span>
    {% if article.volume %}
    <span class="volume">{{ article.volume }}, </span>
    {% endif %}
    {% if article.page %}
    <span class="page">{{ article.page }}.</span>
    {% endif %}
    {% if article.DOI %}
        <a href="http://dx.doi.org/{{ article.DOI }}">{{  article.DOI }}</a>
    {% endif %}
    {% if article.URL %}
        <a href="{{ article.URL }}">{{  article.URL }}</a>
    {% endif %}
    </div>
    </li>
{% endfor %}
</ol>
</div>

