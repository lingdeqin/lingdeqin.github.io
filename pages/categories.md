---
layout: default
title: 分类
description: 文章分类列表
keywords: 分类
permalink: /categories/
---

<div class='tag_cloud'>
{% for cat in site.categories %} 
<a href="#{{ cat[0] }}" title="{{ cat[0] }}" rel="{{ cat[1].size }}">{{ cat[0] }}({{ cat[1].size }}) </a>
{% endfor %}
</div>

{% for category in site.categories %}
<h4>{{ category | first }}</h4>
<ul id="{{ category[0] }}">
{% for post in category.last %}
<li><a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
{% endfor %}
