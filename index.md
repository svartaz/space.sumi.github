# index

<script type='text/javascript' src='https://storage.ko-fi.com/cdn/widget/Widget_2.js'></script><script type='text/javascript'>kofiwidget2.init('Support me on Ko-fi', '#72a4f2', 'M4M6KQQBR');kofiwidget2.draw();</script>

## html

{% assign html_files = site.static_files | where: "extname", ".html" | sort: "path" %}

<ul>
  {% for file in html_files %}
    <li><a href="{{ file.path | relative_url }}">{{ file.basename | replace: "-", " " | escape }}</a></li>
  {% endfor %}
</ul>

## markdown

<ul>
  {% for page in site.pages %}
    {% if page.title and page.url != "/" %}
      <li><a href="{{ page.url | relative_url }}">{{ page.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
