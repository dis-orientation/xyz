---
title: XYZ Dis-orientation Sample Blog
layout: default
---

## XYZ Dis-orientation Sample Blog

{% for post in site.posts %}
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