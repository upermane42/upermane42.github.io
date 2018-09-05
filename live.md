---
layout: default
---

{% for post in site.categories.live %}


<div class="posts">
    <div class="post">
    <h2> <a href="{{ post.url|prepend: site.baseurl }}">{{ post.title }}</a></h2>
    <p>{{ post.autor }} {{ post.date|date:"%d.%m.%Y" }}</p>
    <br>
    <img src="{{ post.preview-img }}">
    <p>{{ post.preview }}</p>
    <h4> <a href="{{ post.url|prepend: site.baseurl }}">Читать дальше </a> </h4>
    </div>
</div>


{% endfor %}