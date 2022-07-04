---
layout: default
title: Все в одном
---

# Все вопросы и ответы в одном месте

{% for tag in site.tags %}
{% capture  cat_name %}{{tag[0]}}-questions{% endcapture %}

## {{ tag[1][0].title }}

{% for q in site.categories[cat_name] %}
- [{{ q.title }}]({{ q.url }})
  >{{ q.content }}
{% endfor %}
{% endfor %}