---
title: Resources
layout: top
---

##Resources
<hr/>

###Video Resources


<div style="padding:20px;" class="row">
{% for video in site.data.resources %}
{% if video.type == "video" %}
  <div style="width:305px; height: 310; float:left;">
    <h4 style="overflow:hidden; margin: 0 10px 0 10px; padding: 10px; text-align:center">{{video.title}}</h4>
    <iframe width="300" height="300" src="{{video.link}}" frameborder="0" allowfullscreen></iframe>
  </div>
  {% endif %}
  {% endfor %}
</div>


###Tech Resources

{% for resource in site.data.resources %}
{% if resource.type == "web" %}
  {{resource.title}}<a href="{{resource.link}}">{{resource.link}}</a>
{% endif %}
{% endfor %}
