---
layout: default
---

{% for post in site.categories.java %}


<div class="posts">
    <div class="post">
    <h2> <a href="{{ post.url|prepend: site.baseurl }}">{{ post.title }}</a></h2>
    <p>{{ post.date|date:"%d.%m.%Y" }}</p>
    <br>
    {{ post.content }}
    </div>
</div>


{% endfor %}