---
layout: page
title: Hello World!
tagline: about
---
{% include JB/setup %}

Zhang LongQi

I am working in [Energy Research Institute](http://erian.ntu.edu.sg) of [Nanyang Technological University](http://www.ntu.edu.sg).

Here is my [CV](http://longqi.pro/cv.html)

### Posts list

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
