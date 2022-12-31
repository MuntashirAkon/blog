Welcome to my blog!

This is my personal blog site. Therefore, anything I say here are my own.

### Posts

{% for post in site.posts %}
  <article>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <span class="mini-note">{{ post.date | date: "%b %-d, %Y" }}</span>
    </article>
{% endfor %}
