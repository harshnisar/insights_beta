---
layout: default
title: Home
tags: gender
---

<b>Insights</b> is an intiative by <a href='http://research.aspiringminds.com'>Aspiring Minds Research</a> to give 52 rich insights into the Indian labour market, one week at a time. 
Subscribe here to get the Insights delivered to your inbox.
<br><br>
Read more about the project <a href=""> here</a>
<br><br>


{% include tile-menu.html %}

Insights:
<br>
<a id="seeMore" onclick="toggleSeeMore()" href="javascript:void(0);">(Show table of contents)</a>
<br>
<div id="textarea" style="display: none">
<ol>
{% for post in site.posts %}
{% if post.tags contains page.tags %}
<li>
<a href="#{{ post.title }}"> {{ post.title }}  </a>
<br>
</li>
{% endif %}
{% endfor %}
</ol>
</div>
<br>

{{ page.tags }}

<div class="posts">
  {% for post in site.posts %}
  {% if post.tags contains page.tags %}
        <b>the one I want</b>
        <div class="post">
          <h1 class="post-title">
            <a name="{{ post.title }}"></a>
            <a href="{{ site.url }}{{ post.url }}">
              {{ post.title }}
            </a>
          </h1>

          <span class="post-date">{{ post.date | date_to_string }}</span>

          {{ post.content }}
        </div>
  
  {% endif %}
  {% endfor %}
</div>


