---
datacite:
  "@context": "http://schema.org"
  "@type": "Dataset"
  "@id": "https://doi.org/10.23698/aida/drske"
  name: "Skeletal data from the Visual Sweden project DROID"
  about: "Radiology"
  url: "https://datasets.aida.medtech4health.se/10.23698/aida/drske"
  author:
    - name: "Mischa Woisetschläger"
      "@id": "https://orcid.org/0000-0003-0066-4985"
      "@type": "Person"
    - name: "Filip Landgren"
      #"@id": "" # FIXME: missing info
      "@type": "Person"
    - name: "Caroline Bivik Stadler"
      "@id": "https://orcid.org/0000-0001-7250-234X"
      "@type": "Person"
    - name: "Daniel Forsberg"
      "@id": "https://orcid.org/0000-0003-0908-9470	"
      "@type": "Person"
  publisher:
    "@type": "Organization"
    name: "AIDA"
  copyrightYear: 2019
  copyrightHolder:
    - name: "Linköping University"
      url: "https://liu.se/"
      "@type": "Organization"
    - name: "Anders Persson"
      "@id": "https://orcid.org/0000-0002-9446-6981"
      "@type": "Person"
  provider:
    - name: "Mischa Woisetschläger"
      email: "Mischa.Woisetschlager@regionostergotland.se"
      "@type": "Person"
      "@id": "https://orcid.org/0000-0003-0066-4985"
    - name: "Claes Lundstrom"
      email: "claes.lundstrom@liu.se"
      "@type": "Person"
      "@id": "https://orcid.org/0000-0002-9368-0177"
    - "@type": "Person"
      email: "joel.hedlund@liu.se"
      "@id": "https://orcid.org/0000-0001-6443-3604"
      name: "Joel Hedlund"
    - name: "Anders Persson"
      email: "anders.s.persson@liu.se"
      "@id": "https://orcid.org/0000-0002-9446-6981"
      "@type": "Person"
  dateCreated: "2019-01-09"
  datePublished: "2019-01-09"
  dateModified: "2019-01-09"
  keywords: "Radiology, Bone, Cancer, Metastasis, Computed tomography, Annotated"
  version: "1.0.1"
  description: |
    36 radiology cases showing lytic and lytic/sclerotic (blastic) metastases
    i.e. bone regenerative and degenerative. These cases have all been punctured
    and pathologically analyzed to verify the diagnose. The metastases were
    segmented accurately by a radiologist and the annotations were confirmed by
    a second radiologist.
  license:
    - name: "Restricted access"
      id: "https://datasets.aida.medtech4health.se/10.23698/aida/drske#license"
      "@type": "CreativeWork"
  citation:
    #- "@type": "CreativeWork"
    #  "@id": "https://doi.org/10.5438/0000-00SS"
    #  name: "Title of paper 1 goes here"
other:
  shortName: "DRSKE"
  status: "Completed"
  annotation: |
    The metastases were segmented accurately by a radiologist and the
    annotations were confirmed by a second radiologist.
  download:
    links:
      - text: ""
        url: ""
  countries-shared:
    - "SE"
  organ:
    - name: "Skeleton"
      sctid: 113192009
  age-span:
  bytes: 14900000000
  numberOfScans: 36
  numberOfAnnotations:
  resolution:
  modality:
    - "CT"
  scanner:
  stain:
  phase:
  exampleImage:
    - title: "A 3D visualization of the region. The crosshair indicates the location of the lytic metastasis."
      url: "/assets/images/10.23698/aida/drske/3d.png"
      thumbnail-url: "/assets/images/10.23698/aida/drske/3d-thumbnail.png"
    - title: "Slice from thorax CT stack with annotated sclerotic and lytic bone metastases."
      url: "/assets/images/10.23698/aida/drske/slice.png"
      thumbnail-url: "/assets/images/10.23698/aida/drske/slice-thumbnail.png"
    - title: "Annotation of sclerotic metastasis."
      url: "/assets/images/10.23698/aida/drske/sclerotic.png"
      thumbnail-url: "/assets/images/10.23698/aida/drske/sclerotic-thumbnail.png"
    - title: "Annotation of lytic metastasis."
      url: "/assets/images/10.23698/aida/drske/lytic.png"
      thumbnail-url: "/assets/images/10.23698/aida/drske/lytic-thumbnail.png"
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
