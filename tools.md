---
layout: page
title: Tools
permalink: /tools/
---

      <section class="blog">
        <div class="container">
          <div class="post-list" itemscope="" itemtype="http://schema.org/Blog">

            {% for post in site.categories.tools %}
              {% include card.html %}
            {% endfor %}

          </div>
        </div>
      </section>

<div>
{% for category in site.categories.tools %}
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
