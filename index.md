---
layout: index
title: Home
---
I am an assistant professor in the Business Economics and Public Policy (BEPP) group at the Wharton School at the University of Pennsylvania. My research is in the fields of public economics and labor economics. I am a co-director at <a href="https://policyimpacts.org">Policy Impacts</a>. I received a PhD in Economics from Harvard. 

My CV is <a href="https://bsprungkeyser.com/Sprung-Keyser_CV.pdf">here</a>.

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

## Working Papers
{%- assign publications = site.data.working-%}
{%- assign papers_dir = "/assets/papers/" -%}
{%- assign slides_dir = "/assets/slides/" -%}
{%- assign appendix_dir = "/assets/appendix/" -%}

{% for pub in publications %}
* **{{ pub.title }}**  
{{ pub.authors }}  
{% if pub.venue %}{{ pub.venue_prefix }}*{{ pub.venue }}*  {% endif %}
{% if pub.paper %}[[Paper]]({{ papers_dir | prepend: site.baseurl | append: pub.paper }}){% endif %}
{% if pub.slides %}[[Executive Summary]]({{ slides_dir | prepend: site.baseurl | append: pub.slides }}){% endif %}
{% if pub.website %}[[Interactive Data Tool]]({{ pub.website }}){% endif %}
{% if pub.appendix %}[[Online Appendix]]({{ appendix_dir | prepend: site.baseurl | append: pub.appendix }}){% endif %}
{% endfor %}

## Notes
{%- assign publications = site.data.notes-%}
{%- assign papers_dir = "/assets/papers/" -%}
{%- assign slides_dir = "/assets/slides/" -%}

{% for pub in publications %}
* **{{ pub.title }}**  
{{ pub.authors }}  
{% if pub.paper %}[[Paper]]({{ papers_dir | prepend: site.baseurl | append: pub.paper }}){% endif %}
{% if pub.slides %}[[Previous Version]]({{ slides_dir | prepend: site.baseurl | append: pub.slides }}){% endif %}
{% endfor %}

