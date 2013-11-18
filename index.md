---
title: XYZ Dis-orientation 
layout: default
---

## XYZ Blog

{% for post in site.posts %}
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
<hr style="background:#4B4137; border:0; height:7px" />
</div>
{% endfor %}