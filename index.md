A place for fragments, questions, and occasional glimpses into the writing of *She Dressed for No One*.

---

{% for post in site.posts %}

### [{{ post.title }}]({{ post.url | relative_url }})

*{{ post.date | date: "%B %-d, %Y" }}*

{{ post.excerpt }}

[Continue reading →]({{ post.url | relative_url }})

{% unless forloop.last %}
<br>
{% endunless %}

{% endfor %}
