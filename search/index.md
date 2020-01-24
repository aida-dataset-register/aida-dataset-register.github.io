---
title: "Search"
description: "Find datasets of interest on the AIDA data hub."
---
Please use the interactive table below for basic sorting and text search.

<table id="dataset-table">
 <thead><tr><th>Name</th><th>Subject</th><th>Modality</th><th>Date</th><th>Size</th><th>Organ</th><th>Title</th></tr></thead>
 <tbody>
 {% for d in site.datasets %}
   {% if d.hidden %}{% continue  %}{% endif %}
   {% assign kw = d.datacite.keywords | split:", " %}
   {% assign organs = d.other.organ | map: "name" |join: ',' %}
   <tr>
     <td><a href="{{ d.url }}">{{ d.other.shortName }}</a></td>
     <td>{% if kw contains 'Pathology' %}<a href="/search?q=Pathology">Pathology</a>{% endif %}{% if kw contains 'Radiology' %}<a href="/search?q=Radiology">Radiology</a>{% endif %}</td>
     <td>
       {% for m in d.other.modality %}
         {% include modality-title.html modality=m %}<br/>
       {% endfor %}
     </td>
     <td>{{ d.datacite.datePublished }}</td>
     <td>{% include human_friendly_filesize bytes=d.other.bytes %}</td>
     <td>{% for o in organs %}<a href="/search?q={{ o }}">{{ o }}</a> {% endfor %}</td>
     <td><b><a href="{{ d.url }}">{{ d.datacite.name }}</a></b><br/><span style="font-size: small;">{% for k in kw %}<a href="/search?q={{ k }}">{{ k }}</a>{% unless forloop.last %},{% endunless %} {% endfor %}</span></td>
   </tr>
 {% endfor %}
 </tbody>
</table>

<script type="text/javascript" language="javascript" src="//code.jquery.com/jquery-3.3.1.min.js"></script>
<script type="text/javascript" language="javascript" src="//cdn.datatables.net/1.10.19/js/jquery.dataTables.min.js"></script>
<script type="text/javascript" language="javascript" src="//cdn.datatables.net/plug-ins/1.10.19/sorting/file-size.js"></script>
<script>
$(document).ready( function () {
  $('#dataset-table').DataTable({
     paging: false,
     columnDefs: [
       { type: 'file-size', targets: 3 }
     ]
  }).search(new URLSearchParams(window.location.search).get('q') || '').draw();
} );
</script>
