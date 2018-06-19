---
layout: default
---

{% for post in site.categories.java %}


<div class="blog-post">
    <h2 class="blog-post-title"> <a href="{{ post.url|prepend: site.baseurl }}">{{ post.title }}</a></h2>
    <p class="blog-post-meta">{{ post.date|date:"%d.%m.%Y" }}</p>
    {{ post.content }}

</div>


{% endfor %}