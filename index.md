---
layout: index
title: Home
---
I am a PhD student in Economics at Harvard. My current research is in the fields of public economics and labor economics. I am a co-director at Policy Impacts. 

I received an AB in Economics from Harvard in 2015 and an MPhil in Economics from the University of Oxford in 2017. 

## Publications
{%- assign publications = site.data.publications -%}
{%- assign papers_dir = "/assets/papers/" -%}
{%- assign slides_dir = "/assets/slides/" -%}

{% for pub in publications %}
* **{{ pub.title }}**  
{{ pub.authors }}  
{% if pub.status %}*{{ pub.status }}*  {%- endif -%}
{% if pub.venue %}{{ pub.venue_prefix }}*{{ pub.venue }}*  {% endif %}
{% if pub.paper %}[[Paper]]({{ papers_dir | prepend: site.baseurl | append: pub.paper }}){% endif %}
{% if pub.slides %}[[Executive Summary]]({{ slides_dir | prepend: site.baseurl | append: pub.slides }}){% endif %}
{% if pub.website %}[[Interactive Website]]({{ pub.website }}){% endif %}
{% endfor %}

