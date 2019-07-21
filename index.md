---
layout: index
title: Home
---
I am a PhD student in Economics at Harvard. My current research is the fields of public economics and labor economics. 

I received in AB in Economics from Harvard in 2015 and an MPhil in Economics from the University of Oxford in 2017. 

## Working Papers
{%- assign publications = site.data.publications -%}
{%- assign papers_dir = "/assets/papers/" -%}
{%- assign slides_dir = "/assets/slides/" -%}

{% for pub in publications %}
* **{{ pub.title }}**  
{{ pub.authors }}  
{% if pub.status %}*{{ pub.status }}*  {%- endif -%}
{% if pub.paper %}[[Paper -- July 2019]]({{ papers_dir | prepend: site.baseurl | append: pub.paper }}){% endif %}
{% if pub.slides %}[[Executive Summary]]({{ slides_dir | prepend: site.baseurl | append: pub.slides }}){% endif %}
{% if pub.website %}[[Interactive Website]]({{ pub.website }}){% endif %}
{% endfor %}

