---
layout: default
lang: en
title: the love
permalink: /love/
image: /assets/Seleba-HERO-1600x600.png
alt_title: Selaba BIZ
sub_title: conversations about art, creativity and entrepreneurship
---
<center><strong>TIPS & ADVICE ABOUT MAKING A LIVING AS AN ARTIST</strong></center>
<br />
<ul>
    {% for post in site.categories.love %}
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      {% if post.featured-image %}{% include post-featured-image.html image=post.featured-image alt=post.featured-image-alt %}{% endif %}
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
    {% if page.author %} •
      <span itemprop="author" itemscope itemtype="http://schema.org/Person"><span itemprop="name">{{ page.author }}</span></span>{% endif %}

    {{ post.excerpt }}
    {% endfor %}
</ul>