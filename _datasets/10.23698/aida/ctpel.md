---
hidden: true
datacite:
  "@context": "http://schema.org"
  "@type": "Dataset"
  "@id": "https://doi.org/10.23698/aida/ctpel"
  name: "Segmented CT pelvis scans with annotated anatomical landmarks"
  about: "Radiology"
  url: "https://datasets.aida.medtech4health.se/10.23698/aida/ctpel"
  author:
    - name: "Bryan Connolly"
      "@id": "" # FIXME: missing info
      "@type": "Person"
    - name: "Chunliang Wang"
      "@id": "https://orcid.org/0000-0002-0442-3524"
      "@type": "Person"
  publisher:
    "@type": "Organization"
    name: "AIDA"
  copyrightYear: 2019
  copyrightHolder:
    - name: "KTH"
      url: "https://kth.se/"
      "@type": "Organization"
    - name: "Chunliang Wang"
      "@id": "https://orcid.org/0000-0002-0442-3524"
      "@type": "Person"
  provider:
    - name: "Chunliang Wang"
      email: "chunwan@kth.se"
      "@id": "https://orcid.org/0000-0002-0442-3524"
      "@type": "Person"
    - name: "Joel Hedlund"
      email: "joel.hedlund@liu.se"
      "@id": "https://orcid.org/0000-0001-6443-3604"
      "@type": "Person"
    - name: "Claes Lundstrom"
      email: "claes.lundstrom@liu.se"
      "@id": "https://orcid.org/0000-0002-9368-0177"
      "@type": "Person"
  dateCreated: "2019-05-03"
  datePublished: "2019-05-03"
  dateModified: "2019-05-03"
  keywords: "Radiology, Annotated, Pelvis, CT, Computed tomography, Anatomical landmarks, Bone segmentation"
  version: "1.0"
  description: |
    Segmentation masks and annotations of anatomical landmarks for pelvis bones
    for 90 segmented Computed Tomography (CT) cases extracted from the “CT Lymph
    nodes” and “CT Colonography” collections from the The Cancer Imaging Archive
    (TCIA).
  license:
    - name: "Restricted access"
      id: "https://datasets.aida.medtech4health.se/10.23698/aida/ctpel#license"
      "@type": "CreativeWork"
  citation:
    - "@type": "Chapter"
      "@id": "https://doi.org/10.1007/978-3-030-11166-3_5"
      name: |
        Wang C., Connolly B., de Oliveira Lopes P.F., Frangi A.F., Smedby Ö.
        (2019) Pelvis Segmentation Using Multi-pass U-Net and Iterative Shape
        Estimation. In: Vrtovec T., Yao J., Zheng G., Pozo J. (eds)
        Computational Methods and Clinical Applications in Musculoskeletal
        Imaging. MSKI 2018. Lecture Notes in Computer Science, vol 11404.
        Springer, Cham
other:
  status: "Ongoing"
  annotation: |
    Segmentation was done first with an interactive software (Mialab), followed
    by manual inspection and correction using ITKSNAP. The interactive method is
    based on fuzzy connectedness followed by level set method. Both the
    segmentation mask and annotated anatomical landmarks were created by a
    trained radiologist.
  ethicsApproval: |
    Please refer to the original ethical approvals, available through
    [TCIA](https://www.cancerimagingarchive.net/).
  download:
    links:
      - text: ""
        url: ""
  organ:
    - name: "Pelvis"
      sctid: 12921003 # SNOMED-CT https://termbrowser.nhs.uk/?perspective=full&conceptId1=%s
  age-span: "" # FIXME: missing data
  bytes: 28000000000
  numberOfImages: 90
  numberOfAnnotations: # FIXME: missing data
  resolution:
  modality:
    - "Computed tomography"
  stain:
  phase:
  image: "/assets/images/10.23698/aida/ctpa/axial-ctpa-thumbnail.jpg"
  exampleImage:
    - title: "3D volume rendered image."
      url: "/assets/images/10.23698/aida/ctpa/3d.jpg"
      thumbnail-url: "/assets/images/10.23698/aida/ctpa/3d-thumbnail.jpg"
    - title: "Axial CTPA image showing pulmonary emboli."
      url: "/assets/images/10.23698/aida/ctpa/axial-ctpa.jpg"
      thumbnail-url: "/assets/images/10.23698/aida/ctpa/axial-ctpa-thumbnail.jpg"
    - title: "Axial CTPA image with annotated pulmonary emboli."
      url: "/assets/images/10.23698/aida/ctpa/axial-ctpa-annotated.jpg"
      thumbnail-url: "/assets/images/10.23698/aida/ctpa/axial-ctpa-annotated-thumbnail.jpg"
---
## License

### Segmentation masks and anatomical landmark annotations
Copyright
{{ page.datacite.copyrightYear }}
{{ page.datacite.copyrightHolder | map: "name" |  join: ", " }}

Permission to use, copy, modify, and/or distribute the data within AIDA (Analytic
Imaging Diagnostics Arena https://medtech4health.se/aida) for any purpose with
or without fee is hereby granted, provided that the above copyright notice and
this permission notice appear in all copies.

THE DATA IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD
TO THIS DATA INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN
NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT, INDIRECT, OR
CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA
OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS
ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR CHARACTERISTICS OF THIS
DATA.

### Attribution
In addition to the TCIA rules about using the image data, we would really
appreciate if you include the following references in publications that make use
of the provided segmentation masks or anatomical landmarks:

[1] {{ page.datacite.author | map: "name" | array_to_sentence_string }}
({{ page.datacite.datePublished | date: "%Y" }})
{{ page.datacite.name }}
[doi:{{ page.datacite['@id'] | remove: "https://doi.org/" }}]({{ page.datacite["@id"] }}).

{% for c in page.datacite.citation %}
  [{{ forloop.index | plus: 1 }}]
  [{{ c.name }}]({{c["@id"]}})

{% endfor %}
