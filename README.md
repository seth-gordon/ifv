# Welcome

This is my Web site. There are many like it, but this one is mine.

My Web site is my best friend. It is my life. I must master it as I
must master my life.

Without me, my Web site is useless. Without my Web site, I am useless.

## My short fiction

{% for story in site.fiction %}
### “{{ story.title }}”, in _{{ story.publisher }}_, {{ story.pubdate }}
{{ story.content }}
{% endfor %}

## Where else to find me

<ul>
{% for medium in site.social_media %}
<li><a href="{{ medium.url }}">{{ medium.name }}</a></li>
{% endfor %}
</ul>

## Recent blog posts

<dl>
{% for post in site.posts limit:5 %}
<dt><a href="{{ post.url }}">{{ post.title }}</a></dt>
<dd>{{ post.excerpt }}</dd>
{% endfor %}
</dl>
