---
datacite:
  "@context": "http://schema.org"
  "@type": "Dataset"
  "@id": "https://doi.org/10.23698/aida/drbr"
  name: "Breast data from the Visual Sweden project DROID"
  about: "Pathology"
  url: "https://doi.aida.medtech4health.se/10.23698/aida/drbr"
  author:
    - name: "Anna Bodén"
      "@id": "https://orcid.org/0000-0002-0128-870X"
      "@type": "Person"
      givenName: "Anna"
      familyName: "Bodén"
    - name: "Jerónimo F. Rose"
      "@id": "https://orcid.org/0000-0003-3845-8546"
      "@type": "Person"
      givenName: "Jerónimo"
      familyName: "Rose"
    - name: "Martin Lindvall"
      "@id": "https://orcid.org/0000-0002-7014-8874"
      "@type": "Person"
      givenName: "Martin"
      familyName: "Lindvall"
    - name: "Caroline Bivik Stadler"
      "@id": "https://orcid.org/0000-0001-7250-234X"
      "@type": "Person"
      givenName: "Caroline"
      familyName: "Bivik Stadler"      
  publisher:
    "@type": "Organization"
    name: "AIDA"
  copyrightYear: 2019
  copyrightHolder:
    - name: "Linköping University"
      "@type": "Organization"
      url: "https://liu.se/"
    - name: "Claes Lundström"
      "@id": "https://orcid.org/0000-0002-9368-0177"
      "@type": "Person"
      givenName: "Claes"
      familyName: "Lundström"
  provider:
    - name: "Anna Bodén"
      email: "Anna.C.Boden@regionostergotland.se"
      "@id": "https://orcid.org/0000-0002-0128-870X"
      "@type": "Person"
    - name: "Claes Lundstrom"
      email: "claes.lundstrom@liu.se"
      "@id": "https://orcid.org/0000-0002-9368-0177"
      "@type": "Person"
    - name: "Joel Hedlund"
      email: "joel.hedlund@liu.se"
      "@id": "https://orcid.org/0000-0001-6443-3604"
      "@type": "Person"
  dateCreated: "2019-01-09"
  datePublished: "2019-01-09"
  dateModified: "2019-01-09"
  keywords: "Pathology, Breast, Cancer, Whole slide imaging, Annotated"
  version: "1.0"
  description: |
    This dataset consists of 337 whole slide images (WSI) - 272 malignant from
    women with invasive breast cancer (HER2 neg) and 65 benign. The tumours have
    been classified with four SNOMED-CT categories based on morphology: invasive
    duct carcinoma, invasive lobular carcinoma, in situ carcinoma, and others.
    4381 separate annotations have been made to segment different tissue
    structures connected to ontologies.
  license:
    - name: "Restricted access"
      url: "#license"
      "@type": "CreativeWork"
  citation:
    #- "@type": "CreativeWork"
    #  "@id": "https://doi.org/..."
    #  name: "Title of paper goes here"
other:
  status: "Completed"
  annotation: |
    The breast tumours were classified with four SNOMED-CT categories based on
    morphology: invasive duct carcinoma, Invasive lobular carcinoma, in situ
    carcinoma and others. 4381 separate annotations were made to segment
    different tissue structures connected to ontologies. One physician were
    responsible for the manual annotations controlled by a second pathologist.
  ethicsApproval: |
    The data collection and sharing is ethical approved.
  download:
    links:
      - text: ""
        url: ""
  organ:
    - name: "Breast"
      sctid: 76752008 # SNOMED-CT https://termbrowser.nhs.uk/?perspective=full&conceptId1=%s
  age-span:
  bytes: 577999734414
  numberOfImages: 337
  numberOfAnnotations: 4381
  resolution: "40X single plane, scanned in NDP format"
  modality:
    - "Hamamatsu NanoZoomer-XR C12000 series 2013"
    - "Hamamatsu NanoZoomer 2.0 HT C9600 series 2013"
  stain: "H&E (hematoxylin and eosin)"
  phase:
  exampleImage:
    - title: "Overview of whole slide imaging."
      url: "/assets/images/10.23698/aida/drbr/wsi.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/drbr/wsi-thumbnail.jpeg"
    - title: "Overview of annotations."
      url: "/assets/images/10.23698/aida/drbr/annotations.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/drbr/annotations-thumbnail.jpeg"
    - title: "Detail view of annotations."
      url: "/assets/images/10.23698/aida/drbr/detail.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/drbr/detail-thumbnail.jpeg"
    - title: "To-scale view of pixel resolution in original whole slide imaging data."
      url: "/assets/images/10.23698/aida/drbr/to-scale.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/drbr/to-scale-thumbnail.jpeg"
---
## License
Copyright
{{ page.datacite.copyrightYear }}
{{ page.datacite.copyrightHolder | map: "name" |  join: ", " }}

Permission to use, copy, modify, and/or distribute this data within Analytic
Imaging Diagnostics Arena ([AIDA](https://medtech4health.se/aida)) for any
purpose with or without fee is hereby granted, provided that the above copyright
notice and this permission notice appear in all copies, and that publications
resulting from the use of this data cite the following works:

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
