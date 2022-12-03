---
layout: page
title: Tools
category: tools
permalink: /tools/
---

  <section class="blog">
    <div class="container">
      <div class="post-list" itemscope="" itemtype="http://schema.org/Blog">

        {% for post in site:posts %}
          {% if post.category contains "tools" %}
            {% include card.html %}
          {% endif %}
        {% endfor %}

      </div>
    </div>
  </section>

<div>
  <div class="archive-group">
    {% for post in site.categories["tools"] %}
    <article class="archive-item">
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
    </article>
    {% endfor %}
  </div>
</div>
