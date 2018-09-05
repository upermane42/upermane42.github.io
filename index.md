---
layout: default
---

{% for post in site.categories.jekyll %}


<div class="posts">
    <div class="post">
    <h2 class="blog-post-title"> <a href="{{ post.url|prepend: site.baseurl }}">{{ post.title }}</a></h2>
    <p class="blog-post-meta">{{ post.autor }} {{ post.date|date:"%d.%m.%Y" }}</p>
    <br>
    <img src="{{ post.preview-img }}">
    <p>{{ post.preview }}</p>
    <h4> <a href="{{ post.url|prepend: site.baseurl }}">Читать дальше </a> </h4>
    </div>
</div>


{% endfor %}