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
  <div style="background:gray; margin:10px; width:300px; height: 100%; float:left;">
    <h4 style="color:white; overflow:hidden; margin: 0 10px 0 10px; padding: 10px; text-align:center">{{video.title}}</h4>
    <iframe style="background: black;" width="300" height="300" src="{{video.link}}" frameborder="0" allowfullscreen></iframe>
  </div>
  {% endif %}
  {% endfor %}
</div>

###Outreach Resources
{% for resource in site.data.resources %}
{% if resource.type == "outreach" %}
  {{resource.title}}<a href="{{resource.link}}">{{resource.link}}</a>
{% endif %}
{% endfor %}


###General Resources

{% for resource in site.data.resources %}
{% if resource.type == "web" %}
  {{resource.title}}<a href="{{resource.link}}">{{resource.link}}</a>
{% endif %}
{% endfor %}

