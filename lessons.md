# Lessons

{% assign learn = site.lessons | sort: 'title' %}
{% for item in learn %}
  <p>
    <a href="/learn-php{{ item.url }}">
      <b>{{ item.title}}</b><br />
      <small>{{ item.description }}</small>
    </a>
  </p>
{% endfor %}
