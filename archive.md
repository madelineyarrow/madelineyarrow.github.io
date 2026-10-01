---
layout: default
title: Blog Archive
---

<section class="archive-page">
  <header class="post-header">
    <h1 class="post-title">{{ page.title }}</h1>
  </header>

  <div class="post-content">
    {% assign postsByYear = site.posts | group_by_exp:"post", "post.date | date: '%Y'" %}

    {% for year in postsByYear %}
      <section class="archive-section">
        <h3>{{ year.name }}</h3>

        <ul class="archive-list">
          {% for post in year.items %}
            <li>
              <a href="{{ post.url | relative_url }}">
                {{ post.date | date: "%B %-d" }} — {{ post.title }}
              </a>
            </li>
          {% endfor %}
        </ul>
      </section>
    {% endfor %}
  </div>
</section>
