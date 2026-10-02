A place for fragments, questions, and occasional glimpses into the writing of _[She Dressed for No One](/books/she-dressed-for-no-one/)_.

---

{% for post in site.posts limit:6 %}

### [{{ post.title }}]({{ post.url | relative_url }})

*{{ post.date | date: "%B %-d, %Y" }}*

{{ post.excerpt }}

[Continue reading →]({{ post.url | relative_url }})

{% unless forloop.last %}
<br>
{% endunless %}

{% endfor %}

<br>
---

<br>
[Earlier notes →](/archive.html)
