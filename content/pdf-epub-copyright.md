---
layout: page
order: 5
classes:
  - copyright-page
outputs:
  - epub
  - pdf
page_pdf_output: false
toc: false
---

{% copyright %}

{% if publication.identifier.isbn %}
ISBN: {{ publication.identifier.isbn }}
{% endif %}
