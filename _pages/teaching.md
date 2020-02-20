---
layout: page
title: Teaching 
permalink: /teaching/
description: Courses taught 
---

{% for course in site.teaching %}

{% if course.redirect %}
<div>
    <a href="{{ course.redirect }}" target="_blank">
    <span>
        <strong>{{ course.title }}</strong>
        <br/>
        <p>{{ course.description }}</p>
    </span>
    </a>
</div>
{% else %}

<div>
    <a href="{{ course.url | prepend: site.baseurl | prepend: site.url }}">
    <span>
        <strong>{{ course.title }}</strong>
        <br/>
        <p>{{ course.description }}</p>
    </span>
    </a>
</div>

{% endif %}

{% endfor %}
