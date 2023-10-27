---
layout: index
title: Home
---
I am a postdoctoral research fellow at Opportunity Insights at Harvard. My current research is in the fields of public economics and labor economics. I am a co-director at <a href="https://policyimpacts.org">Policy Impacts</a>.

I received a Ph.D. in Economics from Harvard in 2023, an MPhil in Economics from the University of Oxford in 2017, and an AB in Economics from Harvard in 2015.

**I am on the job market during the 2023-2024 academic year.** 

Job Market Paper to be posted soon! My CV is <a href="https://bsprungkeyser.com/Sprung-Keyser_CV.pdf">here</a>.

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

{% for pub in publications %}
* **{{ pub.title }}**  
{{ pub.authors }}  
{% if pub.venue %}{{ pub.venue_prefix }}*{{ pub.venue }}*  {% endif %}
{% if pub.paper %}[[Paper]]({{ papers_dir | prepend: site.baseurl | append: pub.paper }}){% endif %}
{% if pub.website %}[[Interactive Data Tool]]({{ pub.website }}){% endif %}
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

