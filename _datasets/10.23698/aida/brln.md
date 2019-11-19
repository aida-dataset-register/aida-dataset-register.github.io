---
hidden: yes
datacite:
  "@context": "http://schema.org"
  "@type": "Dataset"
  "@id": "https://doi.org/10.23698/aida/brln"
  name: "Lymph nodes from breast cancer with immunohistochemical staining"
  about: "Pathology"
  url: "https://datasets.aida.medtech4health.se/10.23698/aida/brln"
  author:
    - name: "Sofia Jarkman"
      "@id": # FIXME: missing info
      "@type": "Person"
    - name: "Martin Lindvall"
      "@id": "https://orcid.org/0000-0002-7014-8874"
      "@type": "Person"
    - name: "Joel Hedlund"
      "@id": "https://orcid.org/0000-0001-6443-3604"
      "@type": "Person"
    - name: "Darren Treanor"
      "@id": "https://orcid.org/0000-0002-4579-484X"
      "@type": "Person"
    - name: "Claes Lundstrom"
      "@id": "https://orcid.org/0000-0002-9368-0177"
      "@type": "Person"
    - name: "Jeroen van der Laak"
      "@id": "https://orcid.org/0000-0001-7982-0754"
      "@type": "Person"
  publisher:
    "@type": "Organization"
    name: "AIDA"
  copyrightYear: 2019
  copyrightHolder:
    - name: "Linköping University"
      url: "https://liu.se/"
      "@type": "Organization"
    - name: "Claes Lundström"
      "@id": "https://orcid.org/0000-0002-9368-0177"
      "@type": "Person"
  provider:
    - name: "Sofia Jarkman"
      email: "sofia.jarkman@regionostergotland.se"
      "@id": "" # FIXME: missing info
      "@type": "Person"        
    - name: "Joel Hedlund"
      email: "joel.hedlund@liu.se"
      "@id": "https://orcid.org/0000-0001-6443-3604"
      "@type": "Person"
    - name: "Claes Lundstrom"
      email: "claes.lundstrom@liu.se"
      "@id": "https://orcid.org/0000-0002-9368-0177"
      "@type": "Person"
  dateCreated: "2019-11-19"
  datePublished: "2019-11-19"
  dateModified: "2019-11-19"
  keywords: "Pathology, Whole slide imaging, Breast, Lymph nodes, Cancer, Sentinel nodes, Immunohistochemical staining, cytokeratin, CKAE1/AE3"
  version: "1.0.0"
  description: |
    Whole slide imaging of 396 full cases of axillary lymph nodes in breast 
    cancer cases. Included are both sentinel node surgery and axillary 
    resections pre, peri or post breast cancer surgery or treatment. Sentinel 
    node cases are cut in three levels and mandatory CKAE1/AE3 staining. The 
    other axillary resections with one cut level as default. No frozen 
    sections included. The cases are anonymised and exported from the digital 
    archive at the Department of Clinical Pathology in Linköping, Region 
    Östergötland. Included are both positive and negative cases.
  license:
    - name: "Restricted access"
      id: "https://datasets.aida.medtech4health.se/10.23698/aida/brln#license"
      "@type": "CreativeWork"
  citation:
    #- "@type": "CreativeWork"
    #  "@id": "https://doi.org/..."
    #  name: "Title of paper goes here"
other:
  status: "Ongoing"
  annotation: |
    No in-image annotations available.
  download:
    links:
      - text: ""
        url: ""
  organ:
    - name: "Breast"
      sctid: 76752008 # SNOMED-CT https://termbrowser.nhs.uk/?perspective=full&conceptId1=%s
  age-span: "-"
  bytes: 2366408222458  # 2.4 TB
  numberOfScans: 4462
  numberOfAnnotations: 0
  resolution: "20x"
  modality:
    - Digitized histopathological glass slides
    - Aperio ScanScope AT
    - Hamamatsu NanoZoomer XR
    - Hamamatsu NanoZoomer S360 
    - Hamamatsu NanoZoomer S60
  stain: "Hematoxylin and eosin. In sentinel node cases also immunohistochemical stain  for cytokeratin AE1/AE3."
  phase:
  image: "/assets/images/10.23698/aida/brln/ckae-overview-thumbnail.jpeg"
  exampleImage:
    - title: "Overview of whole slide imaging with cytokeratin immunostaining."
      url: "/assets/images/10.23698/aida/brln/ckae-overview.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/brln/ckae-overview-thumbnail.jpeg"
    - title: "To-scale view of pixel resolution in original whole slide imaging data from cytokeratin immunostaining."
      url: "/assets/images/10.23698/aida/brln/ckae-to-scale.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/brln/ckae-to-scale-thumbnail.jpeg"
    - title: "Overview of whole slide imaging with hematoxylin and eosin staining."
      url: "/assets/images/10.23698/aida/brln/he-overview.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/brln/he-overview-thumbnail.jpeg"
    - title: "To-scale view of pixel resolution in original whole slide imaging data from hematoxylin and eosin staining."
      url: "/assets/images/10.23698/aida/brln/he-to-scale.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/brln/he-to-scale-thumbnail.jpeg"
---
## License
Copyright
{{ page.datacite.copyrightYear }}
{{ page.datacite.copyrightHolder | map: "name" |  join: ", " }}

Permission to use, copy, modify, and/or distribute this data within Analytic
Imaging Diagnostics Arena ([AIDA](https://medtech4health.se/aida)) for any
purpose with or without fee is hereby granted, provided that the above copyright
notice and this permission notice appear in all copies, and that publications
resulting from the use of this data include the authors of this dataset Sofia
Jarkman and Martin Lindvall in the author list and cite the following works:

{{ page.datacite.author | map: "name" | array_to_sentence_string }}
({{ page.datacite.datePublished | date: "%Y" }})
{{ page.datacite.name }}
[doi:{{ page.datacite['@id'] | remove: "https://doi.org/" }}]({{ page.datacite["@id"] }}).

THE DATA IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD
TO THIS DATA INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN
NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT, INDIRECT, OR
CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA
OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS
ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR CHARACTERISTICS OF THIS
DATA.
