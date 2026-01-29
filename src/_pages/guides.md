---
layout: page
title: Guides
---

<ul>
  {% collections.guides.resources.each do |guide| %}
    <li>
      <a href="{{ guide.relative_url }}">{{ guide.data.title }}</a>
    </li>
  {% end %}
</ul>