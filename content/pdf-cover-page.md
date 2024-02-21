---
title: PDF Cover Page Test
contributor:
  - id: cjane
layout: base.11ty.js
classes:
  - pdf-cover-page
order: 600
outputs:
  - pdf
toc: false
---

<div class="pdf-cover-page__header">

***{% pageTitle title=title label=label subtitle=subtitle %}***
{% contributors context=pageContributors format='string' %}

</div>
<div class="pdf-cover-page__citation">

**Chicago:** {% citation context='page', page=pageData, type='chicago' %}

**MLA:** {% citation context='page', page=pageData, type='mla' %}

</div>
<div class="pdf-cover-page__copyright-and-license">

{% if copyright %}
{{ copyright | markdownify }}
{% elsif publication.copyright %}
{{ publication.copyright | markdownify }}
{% endif %}

{% if publication.license.pdf_ebook_text %}
{{ publication.license.pdf_ebook_text | markdownify }}
{% else %}
{% copyrightLicensing %}
{% endif %}

</div>
<div class="pdf-cover-page__publisher-logo">

{% for org in publication.publisher %}![logo]({{ publication.url }}_assets/images/{{ org.logo }}) {% endfor %}

</div>
