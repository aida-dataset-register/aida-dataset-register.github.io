---
title: "Metrics"
description: "AIDA data hub sharing in numbers."
---
Basic metrics for datasets shared on the AIDA data hub.
{% capture ignored %}
  {% assign n = 0 %}
  {% assign b = 0 %}
  {% assign i = 0 %}
  {% assign a = 0 %}
  {% assign annn = 0 %}
  {% assign annb = 0 %}
  {% assign anni = 0 %}
  {% assign anna = 0 %}
  {% assign patn = 0 %}
  {% assign patb = 0 %}
  {% assign pati = 0 %}
  {% assign pata = 0 %}
  {% assign radn = 0 %}
  {% assign radb = 0 %}
  {% assign radi = 0 %}
  {% assign rada = 0 %}
  {% assign organs = '' | split: '' %}
  {% for d in site.datasets %}
    {% if d.hidden %}
      {% continue %}
    {% endif %}
    {% assign kw = d.datacite.keywords | split:", " %}
    {% assign n = n | plus: 1 %}
    {% assign b = d.other.bytes | default: 0 | plus: b %}
    {% assign i = d.other.numberOfImages | default: 0 | plus: i %}
    {% assign a = d.other.numberOfAnnotations | default: 0 | plus: a %}
    {% if kw contains 'Annotated' %}
      {% assign annn = annn | plus: 1 %}
      {% assign annb = d.other.bytes | default: 0 | plus: annb %}
      {% assign anni = d.other.numberOfImages | default: 0 | plus: anni %}
      {% assign anna = d.other.numberOfAnnotations | default: 0 | plus: anna %}
    {% endif %}
    {% if kw contains 'Pathology' %}
      {% assign patn = patn | plus: 1 %}
      {% assign patb = d.other.bytes | default: 0 | plus: patb %}
      {% assign pati = d.other.numberOfImages | default: 0 | plus: pati %}
      {% assign pata = d.other.numberOfAnnotations | default: 0 | plus: pata %}
    {% endif %}
    {% if kw contains 'Radiology' %}
      {% assign radn = radn | plus: 1 %}
      {% assign radb = d.other.bytes | default: 0 | plus: radb %}
      {% assign radi = d.other.numberOfImages | default: 0 | plus: radi %}
      {% assign rada = d.other.numberOfAnnotations | default: 0 | plus: rada %}
    {% endif %}
    {% assign o = d.other.organ | map: "name" %}
    {% assign organs = organs | concat: o %}
  {% endfor %}
  {% assign organs = organs | uniq | sort %}
{% endcapture %}
## Datasets
<table class="info-box">
  <tr><th></th><th>Datasets</th><th>Images / Cases</th><th>Annotations</th><th>Size</th></tr>
  <tr>
    <th>Total</th>
    <td>{{ n }}</td>
    <td>{{ i }}</td>
    <td>{{ a }}</td>
    <td>{% include human_friendly_filesize bytes=b %}</td>
  </tr>
  <tr>
    <td><a href="/search?q=Annotated">Annotated</a></td>
    <td>{{ annn }}</td>
    <td>{{ anni }}</td>
    <td>{{ anna }}</td>
    <td>{% include human_friendly_filesize bytes=annb %}</td>
  </tr>
  <tr>
    <td><a href="/search?q=Pathology">Pathology</a></td>
    <td>{{ patn }}</td>
    <td>{{ pati }}</td>
    <td>{{ pata }}</td>
    <td>{% include human_friendly_filesize bytes=patb %}</td>
  </tr>
  <tr>
    <td><a href="/search?q=Radiology">Radiology</a></td>
    <td>{{ radn }}</td>
    <td>{{ radi }}</td>
    <td>{{ rada }}</td>
    <td>{% include human_friendly_filesize bytes=radb %}</td>
  </tr>
</table>

## Organs
Organs: {{ organs | size }} (unique names).

Please click the names below to do a simple text search for matching datasets:

<ul>
{% for o in organs %}
  <li><a href="/search?q={{ o }}">{{ o }}</a></li>
{% endfor %}
</ul>
