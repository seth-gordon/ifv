# Welcome

This is my Web site. There are many like it, but this one is mine.

My Web site is my best friend. It is my life. I must master it as I
must master my life.

Without me, my Web site is useless. Without my Web site, I am useless.

## My short fiction

<dl class="flatlist">
{% for story in site.fiction %}
  <dt>“{{ story.title }}”, in <i>{{ story.publisher }}</i>, {{ story.pubdate }}</dt>
  <dd>{{ story.content }}</dd>
  {% endfor %}
</dl>

## Where else to find me

<ul class="flatlist">
{% for medium in site.social_media %}
<li><a href="{{ medium.url }}">{{ medium.name }}</a></li>
{% endfor %}
</ul>

## Recent blog posts

<dl>
{% for post in site.posts limit:5 %}
<dt>
    <span class="date">{{ post.date | date_to_string }}</span>
    &mdash;
    <a href="{{ post.url }}">{{ post.title }}</a>
</dt>
<dd>{{ post.excerpt }}</dd>
{% endfor %}
</dl>
