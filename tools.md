---
layout: page
title: Tools 
lang: en
ref: tools
---

<div class="page-content wc-container">
  <div class="post">
    <h1>Additional Tools</h1>
    <p>The tutorials below provide new tools to manage your IT infrastructure.</p>
    {% assign tools=site.categories.tool | where:"lang", page.lang %}
    {% for post in tools %}
    <h2 class="post-title">
      <a href="{{post.url | prepend:site.baseurl | prepend:site.url}}">
        {{ post.title }}
      </a>
    </h2>
  <div class="post-meta">
    <div class="post-time">
      <i class="fa fa-calendar"></i>
      <time>{{ post.date | date_to_string }}</time>
    </div>
  <ul>
    {% for tag in post.tags %}
    <li><a href="{{site.baseurl | prepend:site.url}}/tag/{{ tag }}">{{ tag }}</a></li>
    {% endfor %}
  </ul>
  </div>
  <div class="post-descr">
    <p>
      {{ post.description }}
    </p>
  </div>

   {% endfor %}

</div>
