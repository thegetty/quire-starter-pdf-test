---
layout: page
order: 5
classes:
  - copyright-page
outputs:
  - epub
  - pdf
  - pdf-pages
toc: false
---

{% copyright %}

{% if publication.identifier.isbn %}
ISBN: {{ publication.identifier.isbn }}
{% endif %}
