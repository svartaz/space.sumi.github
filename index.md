# index

## markdown

<ul>
  {% for page in site.pages %}
    {% if page.title and page.url != "/" %}
      <li><a href="{{ page.url | relative_url }}">{{ page.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

## html

{% assign html_files = site.static_files | where: "extname", ".html" | sort: "path" %}
<ul>
  {% for file in html_files %}
    <li><a href="{{ file.path | relative_url }}">{{ file.basename | replace: "-", " " | escape }}</a></li>
  {% endfor %}
</ul>
