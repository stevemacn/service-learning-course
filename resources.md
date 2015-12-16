---
title: Resources
layout: top
---

##Resources
<hr/>

###Video Resources

{% for video in site.data.resources %}
{% if video.type == "video" %}
  <iframe width="300" height="300" src="{{video.link}}" frameborder="0" allowfullscreen></iframe>
{% endif %}
{% endfor %}

###Tech Resources

{% for resource in site.data.resources %}
{% if resource.type == "web" %}
  <a href="{{resource.link}}">{{resource.link}}</a>
{% endif %}
{% endfor %}
