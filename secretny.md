---
layout: default
---

<h3 style="text-align: center; collor: #000"> просто секретные посты для своих от <a href="https://twitter.com/upermane" target="_blank">@upermane</a></h3>

{% for post in site.categories.secretny %}


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