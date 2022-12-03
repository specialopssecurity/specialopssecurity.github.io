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
          {% if post.categories contains page.category %}
            {% include card.html %}
          {% endif %}
        {% endfor %}

      </div>
    </div>
  </section>

<div>
{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>
    <h3 class="category-head">{{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
    <article class="archive-item">
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
    </article>
    {% endfor %}
  </div>
{% endfor %}
</div>
