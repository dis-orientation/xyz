---
layout: default
title: Posts in dis-orientation category
---

## Posts in `dis-orientation` category

{% for post in site.categories.dis-orientation %}
{% if forloop.last != true %}
<div class="post">
<div class="preview-title">
<span class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></span>
<br/>
<div class="date">{{ post.date | date: "%B %e, %Y" }}</div>
</div>
<div class="post-excerpt">
<a href="{{ post.url }}" class="excerpt-link">
{{ post.content | split:"<!-- more -->" | first }}
</a>
<br/>
</div>
</div>
{% else %}
<div class="post-last">
<div class="preview-title">
<span class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></span>
<br/>
<div class="date">{{ post.date | date: "%B %e, %Y" }}</div>
</div>
<div class="post-excerpt">
<a href="{{ post.url }}" class="excerpt-link">
{{ post.content | split:"<!-- more -->" | first }}
</a>
<br/>
</div>
</div>
{% endif %}
{% endfor %}