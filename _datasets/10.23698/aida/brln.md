---
hidden: no
datacite:
  "@context": "http://schema.org"
  "@type": "Dataset"
  "@id": "https://doi.org/mock_1"
  name: "Mock data 1"
  about: "Pathology"
  url: "https://bp.Mock data 1"
  author:
  - name: "Person 1"
    #"@id": # FIXME: missing info
    "@type": "Person"
  - name: "Person 2"
    "@id": "https://orcid.org/0"
    "@type": "Person"
  - name: "Person 3"
    "@id": "https://orcid.org/0"
    "@type": "Person"
  - name: "Person 4"
    "@id": "https://orcid.org/0"
    "@type": "Person"
  - name: "Person 4"
    "@id": "https://orcid.org/0"
    "@type": "Person"
  - name: "Person 5"
    "@id": "https://orcid.org/0"
    "@type": "Person"
  publisher:
    "@type": "Organization"
    name: "BP"
  copyrightYear: 2019
  copyrightHolder:
  - name: "University 1"
    url: "https://uni1.se/"
    "@type": "Organization"
  - name: "person 1"
    "@id": "https://orcid.org/0"
    "@type": "Person"
  provider:
  - name: "Person 2"
    email: "person1@uni1.se"
    "@id": "https://orcid.org/0"
    "@type": "Person"
  - name: "person 3"
    email: "person3@uni1.se"
    #"@id": "" # FIXME: missing info
    "@type": "Person"        
  - name: "Person 4"
    email: "Person4@uni1.se"
    "@id": "https://orcid.org/0"
    "@type": "Person"
  - name: "BP"
    email: "BP@mock.com"
    "@id": "https://datahub.aida.scilifelab.se"
    "@type": "Organization"
  dateCreated: "2019-11-19"
  datePublished: "2019-11-19"
  dateModified: "2019-11-21"
  keywords: "Pathology, Whole slide imaging, Breast, Lymph nodes, Cancer, Sentinel nodes, Immunohistochemical staining, cytokeratin, CKAE1/AE3"
  version: "1.0.2"
  # v1.0.2 2020-07-05: Update size in bytes.
  description: |
    Whole slide imaging of 396 full cases of axillary lymph nodes in breast
    cancer cases. 
  license:
  - name: "Controlled access"
    id: "https://datahub.aida.scilifelab.se/10.23698/aida/brln#controlled-access"
    "@type": "CreativeWork"
    abstract: |
      Free for use in legal and ethical medical diagnostics research.
  - name: "AIDA BY CA license"
    id: "https://datahub.aida.scilifelab.se/10.23698/aida/brln#aida-by-ca-license"
    "@type": "CreativeWork"
    abstract: "Free for use within AIDA with attribution and co-authorship."
  citation:
    #- "@type": "CreativeWork"
    #  "@id": "https://doi.org/..."
    #  name: "Title of paper goes here"
other:
  shortName: "DAT1"
  status: "Ongoing"
  annotation: |
    No in-image annotations available. Additional information at case level
    available on request.
  countries-shared:
  - "FI"
  - "NO"
  - "SE"
  organ:
  - name: "Breast"
    sctid: 38498374 # SNOMED-CT https://termbrowser.nhs.uk/?perspective=full&conceptId1=%s
  age-span: "-"
  bytes: 2363159897649  # 2.4 TB
  numberOfScans: 4462
  numberOfAnnotations: 0
  resolution: "20x"
  modality:
  - "SM"
  scanner:
  - Aperio ScanScope AT
  - Hamamatsu NanoZoomer XR
  - Hamamatsu NanoZoomer S360
  - Hamamatsu NanoZoomer S60
  stain: "Hematoxylin and eosin. In sentinel node cases also immunohistochemical stain  for cytokeratin AE1/AE3."
  phase:
  image: "/assets/images/10.23698/aida/brln/ckae-metastasis-thumbnail.jpeg"
  exampleImage:
  - title: "Overview of whole slide imaging with hematoxylin and eosin staining."
    url: "/assets/images/10.23698/aida/brln/he-overview.jpeg"
    thumbnail-url: "/assets/images/10.23698/aida/brln/he-overview-thumbnail.jpeg"
  - title: "Overview of whole slide imaging with cytokeratin immunostaining."
    url: "/assets/images/10.23698/aida/brln/ckae-overview.jpeg"
    thumbnail-url: "/assets/images/10.23698/aida/brln/ckae-overview-thumbnail.jpeg"
  - title: "Detail view of metastasis with hematoxylin and eosin staining."
    url: "/assets/images/10.23698/aida/brln/he-metastasis.jpeg"
    thumbnail-url: "/assets/images/10.23698/aida/brln/he-metastasis-thumbnail.jpeg"
  - title: "Detail view of metastasis with cytokeratin immunostaining."
    url: "/assets/images/10.23698/aida/brln/ckae-metastasis.jpeg"
    thumbnail-url: "/assets/images/10.23698/aida/brln/ckae-metastasis-thumbnail.jpeg"
---
## File formats
### Pixel position scaling
Coordinates given are relative to the image *width*. To get the correct pixel
position, X coordinates (and Y coordinates!) should therefore be multiplied with
the image *width*.

## License
### Controlled access
Free for use in legal and ethical medical diagnostics research.
Please contact the dataset provider for terms of access.

{% include access-request-blurb.md coauthorship="yes" %}

### AIDA BY CA license
Copyright
{{ page.datacite.copyrightYear }}
{{ page.datacite.copyrightHolder | map: "name" |  join: ", " }}

Permission to use, copy, modify, and/or distribute this data within Analytic
Imaging Diagnostics Arena ([AIDA](https://medtech4health.se/aida)) for the
purpose of medical diagnostics research with or without fee is hereby granted,
provided that the above copyright notice and this permission notice appear in
all copies, and that publications resulting from the use of this data include
the authors of this dataset Person 1 and Person 2in the author list
and cite the following works:

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
