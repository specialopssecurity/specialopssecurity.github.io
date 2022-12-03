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
          {% if post.categories == "tools" %}
            {% include card.html %}
          {% endif %}
        {% endfor %}

      </div>
    </div>
  </section>

2
