---
title: "Metrics"
description: "AIDA data hub sharing in numbers."
---
{% capture ignored %}
  {% assign totn = 0 %}
  {% assign totb = 0 %}
  {% assign tots = 0 %}
  {% assign tota = 0 %}
  {% assign annn = 0 %}
  {% assign annb = 0 %}
  {% assign anns = 0 %}
  {% assign anna = 0 %}
  {% assign patn = 0 %}
  {% assign patb = 0 %}
  {% assign pats = 0 %}
  {% assign pata = 0 %}
  {% assign radn = 0 %}
  {% assign radb = 0 %}
  {% assign rads = 0 %}
  {% assign rada = 0 %}
  {% assign organs = '' | split: '' %}
  {% for d in site.datasets %}
    {% if d.hidden %}
      {% continue %}
    {% endif %}
    {% assign kw = d.datacite.keywords | split:", " %}
    {% assign b = d.other.bytes | default: 0 %}
    {% assign s = d.other.numberOfScans | default: 0 %}
    {% assign a = d.other.numberOfAnnotations | default: 0 %}
    {% assign totn = totn | plus: 1 %}
    {% assign totb = totb | plus: b %}
    {% assign tots = tots | plus: s %}
    {% assign tota = tota | plus: a %}
    {% if kw contains 'Annotated' %}
      {% assign annn = annn | plus: 1 %}
      {% assign annb = annb | plus: b %}
      {% assign anns = anns | plus: s %}
      {% assign anna = anna | plus: a %}
    {% endif %}
    {% if kw contains 'Pathology' %}
      {% assign patn = patn | plus: 1 %}
      {% assign patb = patb | plus: b %}
      {% assign pats = pats | plus: s %}
      {% assign pata = pata | plus: a %}
    {% endif %}
    {% if kw contains 'Radiology' %}
      {% assign radn = radn | plus: 1 %}
      {% assign radb = radb | plus: b %}
      {% assign rads = rads | plus: s %}
      {% assign rada = rada | plus: a %}
    {% endif %}
    {% assign o = d.other.organ | map: "name" %}
    {% assign organs = organs | concat: o %}
  {% endfor %}
  {% assign organs = organs | uniq | sort %}
{% endcapture %}
## Datasets
<table class="info-box">
  <tr><th></th><th>Datasets</th><th>Scans</th><th>Annotations</th><th>Size</th></tr>
  <tr>
    <th>Total</th>
    <td>{{ totn }}</td>
    <td>{{ tots }}</td>
    <td>{{ tota }}</td>
    <td>{% include human_friendly_filesize bytes=totb %}</td>
  </tr>
  <tr>
    <td><a href="/search?q=Annotated">Annotated</a></td>
    <td>{{ annn }}</td>
    <td>{{ anns }}</td>
    <td>{{ anna }}</td>
    <td>{% include human_friendly_filesize bytes=annb %}</td>
  </tr>
  <tr>
    <td><a href="/search?q=Pathology">Pathology</a></td>
    <td>{{ patn }}</td>
    <td>{{ pats }}</td>
    <td>{{ pata }}</td>
    <td>{% include human_friendly_filesize bytes=patb %}</td>
  </tr>
  <tr>
    <td><a href="/search?q=Radiology">Radiology</a></td>
    <td>{{ radn }}</td>
    <td>{{ rads }}</td>
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
