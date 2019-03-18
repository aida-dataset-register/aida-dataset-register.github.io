---
datacite:
  "@context": "http://schema.org"
  "@type": "Dataset"
  "@id": "https://doi.org/10.23698/aida/drsk"
  name: "Skin data from the Visual Sweden project DROID"
  about: "Pathology"
  url: "https://doi.aida.medtech4health.se/10.23698/aida/drsk"
  author:
    - name: "Karin Lindman"
      "@id": "https://orcid.org/0000-0003-1298-517X"
      "@type": "Person"
    - name: "Jerónimo F. Rose"
      "@id": "https://orcid.org/0000-0003-3845-8546"
      "@type": "Person"
    - name: "Martin Lindvall"
      "@id": "https://orcid.org/0000-0002-7014-8874"
      "@type": "Person"
    - name: "Caroline Bivik Stadler"
      "@id": "https://orcid.org/0000-0001-7250-234X"
      "@type": "Person"
  publisher:
    "@type": "Organization"
    name: "AIDA"
  copyrightYear: 2019
  copyrightHolder:
    - "@type": "Organization"
      name: "Linköping University"
      url: "https://liu.se/"
    - name: "Claes Lundström"
      "@id": "https://orcid.org/0000-0002-9368-0177"
      "@type": "Person"
  provider:
    - name: "Karin Lindman"
      email: "Karin.Lindman@regionostergotland.se"
      "@id": "https://orcid.org/0000-0003-1298-517X"
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
  keywords: "Pathology, Skin, Cancer, Whole slide imaging, Annotated"
  version: "1.0"
  description: |
    99 skin WSI (whole slide images): 49 abnormal cases and 50 normal benign.
  license:
    - name: "Restricted access"
      url: "#license"
  citation:
    #- "@type": "CreativeWork"
    #  "@id": "https://doi.org/..."
    #  name: "Title of paper goes here"
other:
  status: "Completed"
  annotation: |
    One physician was responsible for the manual annotations controlled by a second pathologist. Accurate annotations were made over the whole tissues. 16509 separate annotations were made.

    The following findings were annotated in the abnormal cases: actinic keratosis, basal cell carcinoma, dermatofibroma, dysplastic nevus, intradermal nevus, keratoachantoma, lentigo malignant melanoma, malignant melanoma, malignant melanoma in situ, scar, seborrheic keratosis, squamous cell carcinoma and squamous cell carcinoma in situ. Other areas annotated: abnormal, acanthosis, artifacts, dermis, epidermis, fibrosis, fibrin body, granuloma, inflammation, inflammatory edema, normal, perichondrium, reactive cellular changes, skin appendage structure, surgical margins, structure of cartilage of auditory canal, subcutaneous fatty tissue, subcutaneous tissue, surgical margins and from which body part the skin was excised.

    In the normal skin cases were following structures chosen to be annotated: artifact, dermis, epidermis, normal skin, perichondrium, skin and subcutaneous structure, skin appendage structure, skin structure, structure of cartilage of auditory canal, subcutaneous fatty tissue, subcutaneous tissue and surgical margins.

  ethicsApproval: |
    The data collection and sharing is ethical approved.
  license: "#license"
  download:
    links:
      - text: ""
        url: ""
  organ:
    - name: "Skin"
      sctid: 39937001 # SNOMED-CT https://termbrowser.nhs.uk/?perspective=full&conceptId1=%s
  age-span: "20-93 years"
  bytes: 32375418471
  numberOfImages: 99
  numberOfAnnotations: 16509
  resolution: "20X single plane"
  modality:
    - "Scanscope AT (Aperio, US)"
    - "NanoZoomer XR (Hamamatsu, Japan)" # FIXME: is this same as "Hamamatsu NanoZoomer-XR C12000 series 2013"?
    - "NanoZoomer XRL (Hamamatsu, Japan)" # FIXME: is this same as "Hamamatsu NanoZoomer 2.0 HT C9600 series 2013"
  stain: "H&E (hematoxylin and eosin)"
  phase:
  exampleImage:
    - title: "Overview of whole slide imaging."
      url: "/assets/images/10.23698/aida/drsk/wsi.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/drsk/wsi-thumbnail.jpeg"
    - title: "Overview of annotations."
      url: "/assets/images/10.23698/aida/drsk/wsi-annotations.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/drsk/wsi-annotations-thumbnail.jpeg"
    - title: "Detail view of abnormal findings."
      url: "/assets/images/10.23698/aida/drsk/detail.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/drsk/detail-thumbnail.jpeg"
    - title: "Detail view of annotations."
      url: "/assets/images/10.23698/aida/drsk/detail-annotations.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/drsk/detail-annotations-thumbnail.jpeg"
    - title: "To-scale view of pixel resolution in original whole slide imaging data."
      url: "/assets/images/10.23698/aida/drsk/to-scale.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/drsk/to-scale-thumbnail.jpeg"
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
