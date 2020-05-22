---
datacite:
  "@context": "http://schema.org"
  "@type": "Dataset"
  "@id": "https://doi.org/10.23698/aida/lnco2"
  name: "Regional lymph node metastasis in colon adenocarcinoma, second collection series"
  about: "Pathology"
  url: "https://datasets.aida.medtech4health.se/10.23698/aida/lnco2"
  author:
    - name: "Gordan Maras"
      "@id": "https://orcid.org/0000-0002-0566-6739"
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
  copyrightYear: 2020
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
      "@id": "https://orcid.org/0000-0002-0566-6739"
      "@type": "Person"        
    - name: "Joel Hedlund"
      email: "joel.hedlund@liu.se"
      "@id": "https://orcid.org/0000-0001-6443-3604"
      "@type": "Person"
    - name: "Claes Lundstrom"
      email: "claes.lundstrom@liu.se"
      "@id": "https://orcid.org/0000-0002-9368-0177"
      "@type": "Person"
  dateCreated: "2020-01-09"
  datePublished: "2020-01-09"
  dateModified: "2020-01-09"
  keywords: "Pathology, Whole slide imaging, Lymph nodes, Cancer, Colon, Adenocarcinoma"
  version: "1.0.0"
  description: |
    Whole slide pathology images from regional lymph node metastasis in colon
    adenocarcinoma produced at Region Gävleborg Clinical Pathology and Cytology
    department. Consists of fifty chronologically consecutive cases.

    This dataset represents a second collection series in connection to the
    <a href="lnco">LNCO dataset</a> using different collection and annotation
    parameters.
  license:
    - name: "Restricted access"
      id: "https://datasets.aida.medtech4health.se/10.23698/aida/lnco2#license"
      "@type": "CreativeWork"
  citation:
    #- "@type": "CreativeWork"
    #  "@id": "https://doi.org/..."
    #  name: "Title of paper goes here"
other:
  shortName: "LNCO2"
  status: "Ongoing"
  annotation: |
    Lymph glands have been identified by an experienced pathologist and annotated
    using region-of-interest boxes.

    Annotation is ongoing and will be included here when available.
  download:
    links:
      - text: ""
        url: ""
  countries-shared:
    - "SE"
  organ:
    - name: "Colon"
      sctid: 71854001 # SNOMED-CT https://termbrowser.nhs.uk/?perspective=full&conceptId1=%s
  age-span:
  bytes: 788018000000 # Rounding down 788018448273 bytes to 788018 MB, to account for few kb json metadata present in dir structure.
  numberOfScans: 1245
  numberOfAnnotations: 0
  resolution: "20x and 40x"
  modality:
    - "SM"
  scanner:
    - "Aperio Scanscope (20x)"
    - "Hamamatsu NanoZoomer (40x)"
  stain: "Hematoxylin and eosin."
  phase:
  image:
  exampleImage:
    - title: "Overview of lymph node whole slide imaging with hematoxylin and eosin staining."
      url: "/assets/images/10.23698/aida/lnco2/lymph-nodes.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/lnco2/lymph-nodes-thumbnail.jpeg"
    - title: "To-scale view of pixel resolution in original lymph node whole slide imaging data from hematoxylin and eosin staining."
      url: "/assets/images/10.23698/aida/lnco2/lymph-nodes-to-scale.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/lnco2/lymph-nodes-to-scale-thumbnail.jpeg"
    - title: "Overview of primary tumor whole slide imaging with hematoxylin and eosin staining."
      url: "/assets/images/10.23698/aida/lnco2/primary-tumor.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/lnco2/primary-tumor-thumbnail.jpeg"
    - title: "To-scale view of pixel resolution in original primary tumor whole slide imaging data from hematoxylin and eosin staining."
      url: "/assets/images/10.23698/aida/lnco2/primary-tumor-to-scale.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/lnco2/primary-tumor-to-scale-thumbnail.jpeg"
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
