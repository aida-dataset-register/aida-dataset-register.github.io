---
datacite:
  "@context": "http://schema.org"
  "@type": "Dataset"
  "@id": "https://doi.org/10.23698/aida/lnco"
  name: "Regional lymph node metastasis in colon adenocarcinoma"
  about: "Pathology"
  url: "https://datasets.aida.medtech4health.se/10.23698/aida/lnco"
  author:
    - name: "Gordan Maras"
      "@id": # FIXME: missing info
      "@type": "Person"
    - name: "Martin Lindvall"
      "@id": "https://orcid.org/0000-0002-7014-8874"
      "@type": "Person"
    - name: "Claes Lundstrom"
      "@id": "https://orcid.org/0000-0002-9368-0177"
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
    - name: "Gordan Maras"
      email: "gordan.maras@regiongavleborg.se"
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
  dateCreated: "2019-08-13"
  datePublished: "2019-08-13"
  dateModified: "2019-08-13"
  keywords: "Pathology, Whole slide imaging, Annotated, Lymph nodes, Cancer, Colon, Adenocarcinoma"
  version: "1.0.0"
  description: |
    Whole slide pathology images from regional lymph node metastasis in colon
    adenocarcinoma produced at Region Gävleborg Clinical Pathology and Cytology
    department and Region Östergötland Clinical Pathology department.
    Annotations for AI training produced as part of AIDA clinical fellowship
    project investigating AI decision support in metastasis detection.
  license:
    - name: "Restricted access"
      id: "https://datasets.aida.medtech4health.se/10.23698/aida/lnco#license"
      "@type": "CreativeWork"
  citation:
    #- "@type": "CreativeWork"
    #  "@id": "https://doi.org/..."
    #  name: "Title of paper goes here"
other:
  status: "Ongoing"
  annotation: |
    Lymph nodes manually classified into two groups, either with or without
    tumor metastases. Tumors have been non-exhaustively annotated in lymph nodes
    that have them, so only lymph nodes without tumor present can be reliably
    used as examples of normal tissue. Regions deemed not suitable for AI
    training have been annotated for exclusion (eg missing or poor quality
    material), or as preparation artefact (eg folded tissue sample).

    Note: Data collection is still ongoing &ndash; not all samples have yet been
    classified.
  download:
    links:
      - text: ""
        url: ""
  organ:
    - name: "Colon"
      sctid: 71854001 # SNOMED-CT https://termbrowser.nhs.uk/?perspective=full&conceptId1=%s
  age-span: 
  bytes: 213024235159 # 198 Gibibytes
  numberOfScans: 740
  numberOfAnnotations: 5720
  resolution: "20x and 40x"
  modality:
    - "Aperio Scanscope (20x)"
    - "Hamamatsu NanoZoomer (40x)"
  stain: "Hematoxylin and eosin."
  phase:
  image:
  exampleImage:
    - title: "Overview of whole slide imaging with hematoxylin and eosin staining."
      url: "/assets/images/10.23698/aida/lnco/he-overview.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/lnco/he-overview-thumbnail.jpeg"
    - title: "To-scale view of pixel resolution in original whole slide imaging data from hematoxylin and eosin staining."
      url: "/assets/images/10.23698/aida/lnco/he-to-scale.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/lnco/he-to-scale-thumbnail.jpeg"
---
## License
Copyright
{{ page.datacite.copyrightYear }}
{{ page.datacite.copyrightHolder | map: "name" |  join: ", " }}

Permission to use, copy, modify, and/or distribute this data within Analytic
Imaging Diagnostics Arena ([AIDA](https://medtech4health.se/aida)) for any
purpose with or without fee is hereby granted, provided that the above copyright
notice and this permission notice appear in all copies, and that publications
resulting from the use of this data include the authors of this dataset Gordan
Maras and Martin Lindvall in the author list and cite the following works:

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
