---
layout: home
lang: en
title: home
sub_title: conversations about art, creativity and entrepreneurship
---
<p style="color:grey;font-size:30px;"><strong>THE LATEST</strong></p>      

<html>
    {% for post in site.posts %}
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      {% if post.featured-image %}{% include post-featured-image.html image=post.featured-image alt=post.featured-image-alt %}{% endif %}
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
    {% if page.author %} •
      <span itemprop="author" itemscope itemtype="http://schema.org/Person"><span itemprop="name">{{ page.author }}</span></span>{% endif %}

    {{ post.excerpt }}
    {% endfor %}
</html>
