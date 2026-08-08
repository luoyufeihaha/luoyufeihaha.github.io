---
layout: default
permalink: /blog/
title: Blog
description: Long-form notes on research, learning, tools, and ideas worth revisiting.
nav: true
nav_order: 3
pagination:
  enabled: true
  collection: posts
  permalink: /page/:num/
  per_page: 5
  sort_field: date
  sort_reverse: true
  trail:
    before: 1
    after: 3
---

<link rel="stylesheet" href="{{ '/assets/css/blog-page.css' | relative_url }}">

<div class="blog-index">
  <header class="blog-hero">
    <p class="blog-hero__eyebrow">Writing</p>
    <h1>{{ site.blog_name }}</h1>
    <p class="blog-hero__description">{{ site.blog_description }}</p>
    <p class="blog-hero__introduction">
      I use this space for longer reflections on research, learning, tools, and ideas that I want to revisit over time.
    </p>
  </header>

{% if site.display_tags and site.display_tags.size > 0 or site.display_categories and site.display_categories.size > 0 %}
<nav class="blog-taxonomy" aria-label="Blog topics">
{% for tag in site.display_tags %}
<a href="{{ tag | slugify | prepend: '/blog/tag/' | relative_url }}">
<i class="fa-solid fa-hashtag" aria-hidden="true"></i>{{ tag }}
</a>
{% endfor %}
{% for category in site.display_categories %}
<a href="{{ category | slugify | prepend: '/blog/category/' | relative_url }}">
<i class="fa-solid fa-tag" aria-hidden="true"></i>{{ category }}
</a>
{% endfor %}
</nav>
{% endif %}

{% if page.pagination.enabled %}
{% assign postlist = paginator.posts %}
{% else %}
{% assign postlist = site.posts %}
{% endif %}

{% if postlist.size > 0 %}
<div class="blog-archive">
{% assign current_year = "" %}
{% for post in postlist %}
{% assign post_year = post.date | date: "%Y" %}
{% if post_year != current_year %}
{% unless forloop.first %}
</div>
</section>
{% endunless %}
<section class="blog-year" aria-labelledby="blog-year-{{ post_year }}">
<div class="blog-year__heading">
<span class="blog-year__dot" aria-hidden="true"></span>
<h2 id="blog-year-{{ post_year }}">{{ post_year }}</h2>
</div>
<div class="blog-year__posts">
{% assign current_year = post_year %}
{% endif %}

        {% if post.external_source == blank %}
          {% assign read_time = post.content | number_of_words | divided_by: 180 | plus: 1 %}
        {% else %}
          {% assign read_time = post.feed_content | strip_html | number_of_words | divided_by: 180 | plus: 1 %}
        {% endif %}

        {% capture post_url %}
          {% if post.redirect == blank %}
            {{ post.url | relative_url }}
          {% elsif post.redirect contains '://' %}
            {{ post.redirect }}
          {% else %}
            {{ post.redirect | relative_url }}
          {% endif %}
        {% endcapture %}

        {% assign card_side = forloop.index | modulo: 2 %}
        <article class="blog-card {% if post.thumbnail %}{% if card_side == 0 %}blog-card--media-right{% else %}blog-card--media-left{% endif %}{% else %}blog-card--text-only{% endif %}">
          {% if post.thumbnail %}
            <a
              class="blog-card__media"
              href="{{ post_url | strip }}"
              {% if post.redirect contains '://' %}target="_blank" rel="noopener noreferrer"{% endif %}
              aria-label="Read {{ post.title | escape }}"
            >
              <img src="{{ post.thumbnail | relative_url }}" alt="" loading="lazy">
            </a>
          {% endif %}

          <div class="blog-card__content">
            {% if post.featured %}<span class="blog-card__featured"><i class="fa-solid fa-thumbtack" aria-hidden="true"></i>Featured</span>{% endif %}
            <h3>
              <a href="{{ post_url | strip }}" {% if post.redirect contains '://' %}target="_blank" rel="noopener noreferrer"{% endif %}>
                {{ post.title }}
              </a>
            </h3>
            {% if post.description %}<p class="blog-card__summary">{{ post.description }}</p>{% endif %}

            <div class="blog-card__meta">
              <span><i class="fa-regular fa-calendar" aria-hidden="true"></i><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time></span>
              <span><i class="fa-regular fa-clock" aria-hidden="true"></i>{{ read_time }} min read</span>
              {% if post.external_source %}<span>{{ post.external_source }}</span>{% endif %}
            </div>

            {% if post.tags.size > 0 or post.categories.size > 0 %}
              <div class="blog-card__taxonomy" aria-label="Post topics">
                {% for tag in post.tags %}
                  <a href="{{ tag | slugify | prepend: '/blog/tag/' | relative_url }}"><i class="fa-solid fa-hashtag" aria-hidden="true"></i>{{ tag }}</a>
                {% endfor %}
                {% for category in post.categories %}
                  <a href="{{ category | slugify | prepend: '/blog/category/' | relative_url }}"><i class="fa-solid fa-tag" aria-hidden="true"></i>{{ category }}</a>
                {% endfor %}
              </div>
            {% endif %}
          </div>
        </article>

        {% if forloop.last %}
            </div>
          </section>
        {% endif %}
      {% endfor %}
    </div>

{% else %}
<section class="blog-empty-state" aria-labelledby="blog-empty-title">
<span class="blog-empty-state__icon" aria-hidden="true"><i class="fa-regular fa-pen-to-square"></i></span>
<div>
<h2 id="blog-empty-title">Writing in progress</h2>
<p>The first long-form note is being prepared. Future essays will appear here in reverse chronological order.</p>
</div>
</section>
{% endif %}

{% if page.pagination.enabled and paginator.total_pages > 1 %}
<div class="blog-pagination">{% include pagination.liquid %}</div>
{% endif %}
</div>
