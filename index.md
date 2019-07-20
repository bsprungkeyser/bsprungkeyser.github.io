---
layout: index
title: Home
---
I am a PhD student in Computer Science at Harvard. 

## Working Papers
{%- assign publications = site.data.publications -%}
{%- assign papers_dir = "/assets/papers/" -%}
{%- assign slides_dir = "/assets/slides/" -%}

{% for pub in publications %}
{{ forloop.index }}. **{{ pub.title }}**  
{{ pub.authors }}  
{% if pub.status %}*{{ pub.status }}*  {%- endif -%}
{% if pub.venue %}{{ pub.venue_prefix }} [{{ pub.venue }}, {{ pub.year }}]({{ pub.venue_link }})  {% endif %}
{% if pub.paper %}[[paper]]({{ papers_dir | prepend: site.baseurl | append: pub.paper }}){% endif %}
{% if pub.slides %}[[slides]]({{ slides_dir | prepend: site.baseurl | append: pub.slides }}){% endif %}
{% endfor %}

