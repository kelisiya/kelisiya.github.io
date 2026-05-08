---
layout: default
title: "Blog"
permalink: /blog/
author_profile: true
description: "Notes and tutorials by Jiake Xie on image matting, AI cutout, plant identification, generative models, and the intersection of computer vision research and real-world AI products."
---

# 📝 Blog

Hi, I'm **Jiake Xie**, a computer vision researcher at [LibAI Lab](https://www.cutout.pro/). Here I share notes, deep-dives and how-to guides on the things I work on every day: **image matting / cutout**, **diffusion-based generation**, and the AI products our team incubates — like [Cutout.Pro](https://www.cutout.pro) for image editing and [heysproutly](https://heysproutly.com/) for plant identification.

If a post helps you, [star my GitHub](https://github.com/Kelisya) or [drop me an email](mailto:jxie@picup.ai). Cross-links and discussion are always welcome.

---

<ul class="blog-post-list">
{% for post in site.posts %}
  <li class="blog-post-item">
    <h2 class="blog-post-item__title">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h2>
    <p class="blog-post-item__meta">
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time>
      {% if post.tags and post.tags.size > 0 %}
        · {% for tag in post.tags %}<span class="post-tag">#{{ tag }}</span>{% unless forloop.last %} {% endunless %}{% endfor %}
      {% endif %}
    </p>
    {% if post.excerpt %}
      <div class="blog-post-item__excerpt">{{ post.excerpt }}</div>
    {% endif %}
    <p><a class="blog-post-item__readmore" href="{{ post.url | relative_url }}">Read more →</a></p>
  </li>
{% endfor %}
</ul>

{% if site.posts.size == 0 %}
*No posts yet — check back soon.*
{% endif %}
