---
suppress_link: true
---
# Welcome

I am an SF writer, a computer programmer, a father, a husband, a Jew,
and a general factotum.

I have less hair than [this guy](https://www.imdb.com/name/nm1164861/)
but more than [this one](https://www.sethgodin.com/).

## Where else to find me

<ul class="flatlist">
{% for medium in site.social_media %}
<li><a href="{{ medium.url }}">{{ medium.name }}</a></li>
{% endfor %}
</ul>

## My short fiction

<dl class="flatlist">
{% for story in site.fiction %}
  <dt>“{{ story.title }}”, in <i>{{ story.publisher }}</i>, {{ story.pubdate }}</dt>
  <dd>{{ story.content }}</dd>
  {% endfor %}
</dl>

## My blog, *yesh omrim*

[See the front page here.]({% link yo/index.html %})

### Recent posts

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

### Tags

{% capture tags %}
  {% for tag in site.tags %}
    {{ tag[0] }}
  {% endfor %}
{% endcapture %}
{% assign sortedtags = tags | split:' ' | sort %}
<ul>
{% for tag in sortedtags %}
<li><a href="/tags/{{ tag }}/">{{ tag }}</a></li>
{% endfor %}
</ul>	
