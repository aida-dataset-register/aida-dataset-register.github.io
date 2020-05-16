---
datacite:
  "@context": "http://schema.org"
  "@type": "Dataset"
  "@id": "https://doi.org/10.23698/aida/drli"
  name: "Liver data from the Visual Sweden project DROID"
  about: "Radiology"
  url: "https://datasets.aida.medtech4health.se/10.23698/aida/drli"
  author:
    - name: "Mischa Woisetschläger"
      "@id": "https://orcid.org/0000-0003-0066-4985"
      "@type": "Person"
    - name: "Johan Blomma"
      #"@id": "" # FIXME: missing info
      "@type": "Person"
    - name: "Nils Dahlström"
      "@id": "https://orcid.org/0000-0002-4111-1693"
      "@type": "Person"
    - name: "Caroline Bivik Stadler"
      "@id": "https://orcid.org/0000-0001-7250-234X"
      "@type": "Person"
    - name: "Daniel Forsberg"
      "@id": "https://orcid.org/0000-0003-0908-9470"
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
      "@id": "https://orcid.org/0000-0003-0066-4985"
      "@type": "Person"
    - name: "Joel Hedlund"
      email: "joel.hedlund@liu.se"
      "@id": "https://orcid.org/0000-0001-6443-3604"
      "@type": "Person"
    - name: "Anders Persson"
      email: "anders.s.persson@liu.se"
      "@id": "https://orcid.org/0000-0002-9446-6981"
      "@type": "Person"
  dateCreated: "2019-01-09"
  datePublished: "2019-01-09"
  dateModified: "2019-01-09"
  keywords: "Radiology, Liver, Cancer, Computed tomography, Annotated"
  version: "1.0.1"
  description: |
    77 CT abdomen (computed tomography) examinations taken with contrast in
    venous phase. All cases showed liver malignancies. Manual oncological
    annotations were made by a radiologist and these were controlled by a second
    experienced radiologist. All changes with a diameter greater than 5mm were
    segmented and assumed metastases (cysts excluded as defined by HU). 317
    lesions were annotated.
  license:
    - name: "Restricted access"
      id: "https://datasets.aida.medtech4health.se/10.23698/aida/drli#license"
      "@type": "CreativeWork"
  citation:
    #- "@type": "CreativeWork"
    #  "@id": "https://doi.org/..."
    #  name: "Title of paper goes here"
other:
  shortName: "DRLI"
  status: "Completed"
  annotation: |
    Manual oncological annotations was made by a radiologist and these were
    controlled by a second radiologist. All changes with a diameter greater than
    5mm was segmented and as assumed metastases (cysts excluded defined by HU).
    317 lesions were annotated.
  download:
    links:
      - text: ""
        url: ""
  countries-shared:
    - "SE"
  organ:
    - name: "Liver"
      sctid: 10200004 # SNOMED-CT https://termbrowser.nhs.uk/?perspective=full&conceptId1=%s
  age-span:
  bytes: 33800000000
  numberOfScans: 77
  numberOfAnnotations: 317
  resolution:
  modality:
    - "CT"
  scanner:
    - "Siemens CT Scanners"
  stain:
  phase: Venuous (with contrast)
  exampleImage:
    - title: "3D illustration of locations, sizes and distribution in liver metastasis (green)."
      url: "/assets/images/10.23698/aida/drli/3d.png"
      thumbnail-url: "/assets/images/10.23698/aida/drli/3d-thumbnail.png"
    - title: "Slice from thorax CT stack with annotated liver metastases."
      url: "/assets/images/10.23698/aida/drli/slice.jpeg"
      thumbnail-url: "/assets/images/10.23698/aida/drli/slice-thumbnail.jpeg"
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
