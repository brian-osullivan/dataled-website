---
layout: page
title: Blog
description: Latest posts on analytics and conversion rate optimization
---

<article class="blog">

  <ul class="grid" role="list" data-layout='50-50'>
    {% collections.blog.resources.each do |post| %}
    <li class="card border-2 flow">
      <img src="{{ post.data.image || '/images/website.jpg'}}">
      <h3>
        <a href="{{ post.relative_url }}">{{ post.data.title }}</a>
      </h3>
      <p class="text-small">{{ post.data.date | date_to_string: "ordinal", "US" }}</p>
      <p>{{ post.data.description }}</p>
    </li>
    {% end %}
  </ul>

</article>
