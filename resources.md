---
title: Resources
layout: top
---

<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.2.0/jquery.min.js"></script>

<script>
  $(document).ready(function () {

    //list of players registered
    var players = ["society", "player"];

    //for all id's create players
      $(".arrow-right").bind("click", function (event) {
          event.preventDefault();
          $(".vid-list-container").stop().animate({
              scrollLeft: "+=336"
          }, 750);
      });
      $(".arrow-left").bind("click", function (event) {
          event.preventDefault();
          $(".vid-list-container").stop().animate({
              scrollLeft: "-=336"
          }, 750);
      });
  });
</script>

##Resources

This page has video libraries curated by topic and a current list of
volunteer opportunities on campus. Videos are used in lieu of a textbook
and they will be used to support in class discussions and activities.

At the bottom of the page you will find information about volunteer
opportunities at UNC Charlotte.

<hr/>

###Society and Motivation

{% assign id = "society" %}
{% assign data = site.data.resources | where: "type", id  %}
{%include player.html %}

###Community

{% assign id = "startups" %}
{% assign data = site.data.resources | where: "type", id  %}
{%include player.html %}

###Management

{% assign id = "management" %}
{% assign data = site.data.resources | where: "type", id  %}
{%include player.html %}



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
