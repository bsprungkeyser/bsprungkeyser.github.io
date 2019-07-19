---
layout: index
title: Home
---
I am a first-year PhD student in Computer Science at [Princeton University](https://www.cs.princeton.edu/). Professor [Wyatt Lloyd](https://www.cs.princeton.edu/~wlloyd/) and I are tackling interesting research problems spanning distributed systems, databases, and computer networks.

Prior to attending Princeton, I earned a Master's in Computer Science at [Carnegie Mellon University](https://www.cs.cmu.edu/), where I was fortunate to be co-advised by [Srini Seshan](https://www.cs.cmu.edu/~srini/) and [Vyas Sekar](https://users.ece.cmu.edu/~vsekar/). I also spent a few years in industry, and before that, I earned my BA from [Amherst College](https://www.amherst.edu/) with a double major in Computer Science and Economics.

I help organize Princeton's [Systems Lunch Seminar](http://sns.cs.princeton.edu/seminar/). If you are interested in giving a talk, please send me an email.

## Publications
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


## Teaching
{%- assign schools = site.data.teaching | map: "school" | uniq -%}

{% for school in schools %}
#### {{ school }}
{%- assign positions = site.data.teaching | where: "school", school -%}

{%- for position in positions %}
* {{ position.title }} for [{{ position.course }}]({{ position.link }}). {{ position.semesters }}
{%- endfor %}
{% endfor %}


## Professional
{%- assign positions = site.data.professional -%}

{%- for position in positions %}
* {{ position.title }}, [{{ position.employer }}]({{ position.link }}). {{ position.start }}–{{ position.end }}
{%- endfor %}
