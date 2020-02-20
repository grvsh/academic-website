---
layout: page
title: Datasets 
permalink: /datasets/
description: Datasets released as public benchmarks 
---

{% for ds in site.datasets %}

{% if ds.redirect %}
<div>
    <a href="{{ ds.redirect }}" target="_blank">
    <span>
        <strong>{{ ds.title }}</strong>
        <br/>
        <p>{{ ds.description }}</p>
    </span>
    </a>
</div>
{% else %}

<div>
    <a href="{{ ds.url | prepend: site.baseurl | prepend: site.url }}">
    <span>
        <strong>{{ ds.title }}</strong>
        <br/>
        <p>{{ ds.description }}</p>
    </span>
    </a>
</div>

{% endif %}

{% endfor %}
