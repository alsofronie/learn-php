# Lessons

{% for item in site.lessons %}
  <p>
    <a href="learn-php/{{ item.url }}">
      <b>{{ item.title}}</b><br />
      <small>{{ item.description }}</small>
    </a>
  </p>
{% endfor %}
