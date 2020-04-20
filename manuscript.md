---
author-meta:
- John Doe
- Jane Roe
bibliography:
- content/manual-references.json
date-meta: '2020-04-20'
header-includes: '<!--

  Manubot generated metadata rendered from header-includes-template.html.

  Suggest improvements at https://github.com/manubot/manubot/blob/master/manubot/process/header-includes-template.html

  -->

  <meta name="dc.format" content="text/html" />

  <meta name="dc.title" content="Manuscript Title" />

  <meta name="citation_title" content="Manuscript Title" />

  <meta property="og:title" content="Manuscript Title" />

  <meta property="twitter:title" content="Manuscript Title" />

  <meta name="dc.date" content="2020-04-20" />

  <meta name="citation_publication_date" content="2020-04-20" />

  <meta name="dc.language" content="en-US" />

  <meta name="citation_language" content="en-US" />

  <meta name="dc.relation.ispartof" content="Manubot" />

  <meta name="dc.publisher" content="Manubot" />

  <meta name="citation_journal_title" content="Manubot" />

  <meta name="citation_technical_report_institution" content="Manubot" />

  <meta name="citation_author" content="John Doe" />

  <meta name="citation_author_institution" content="Department of Something, University of Whatever" />

  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />

  <meta name="twitter:creator" content="@johndoe" />

  <meta name="citation_author" content="Jane Roe" />

  <meta name="citation_author_institution" content="Department of Something, University of Whatever" />

  <meta name="citation_author_institution" content="Department of Whatever, University of Something" />

  <meta name="citation_author_orcid" content="XXXX-XXXX-XXXX-XXXX" />

  <link rel="canonical" href="https://BIRSBiointegration.github.io/whitePaper/" />

  <meta property="og:url" content="https://BIRSBiointegration.github.io/whitePaper/" />

  <meta property="twitter:url" content="https://BIRSBiointegration.github.io/whitePaper/" />

  <meta name="citation_fulltext_html_url" content="https://BIRSBiointegration.github.io/whitePaper/" />

  <meta name="citation_pdf_url" content="https://BIRSBiointegration.github.io/whitePaper/manuscript.pdf" />

  <link rel="alternate" type="application/pdf" href="https://BIRSBiointegration.github.io/whitePaper/manuscript.pdf" />

  <link rel="alternate" type="text/html" href="https://BIRSBiointegration.github.io/whitePaper/v/9b9e0126d92d4f173aa9a99c7ad252242898a1d7/" />

  <meta name="manubot_html_url_versioned" content="https://BIRSBiointegration.github.io/whitePaper/v/9b9e0126d92d4f173aa9a99c7ad252242898a1d7/" />

  <meta name="manubot_pdf_url_versioned" content="https://BIRSBiointegration.github.io/whitePaper/v/9b9e0126d92d4f173aa9a99c7ad252242898a1d7/manuscript.pdf" />

  <meta property="og:type" content="article" />

  <meta property="twitter:card" content="summary_large_image" />

  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />

  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />

  <meta name="theme-color" content="#ad1457" />

  <!-- end Manubot generated metadata -->'
keywords:
- markdown
- publishing
- manubot
lang: en-US
manubot-clear-requests-cache: false
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
title: Manuscript Title
...






<small><em>
This manuscript
([permalink](https://BIRSBiointegration.github.io/whitePaper/v/9b9e0126d92d4f173aa9a99c7ad252242898a1d7/))
was automatically generated
from [BIRSBiointegration/whitePaper@9b9e012](https://github.com/BIRSBiointegration/whitePaper/tree/9b9e0126d92d4f173aa9a99c7ad252242898a1d7)
on April 20, 2020.
</em></small>

## Authors



+ **John Doe**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [johndoe](https://github.com/johndoe)
    · ![Twitter icon](images/twitter.svg){.inline_icon}
    [johndoe](https://twitter.com/johndoe)<br>
  <small>
     Department of Something, University of Whatever
     · Funded by Grant XXXXXXXX
  </small>

+ **Jane Roe**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [XXXX-XXXX-XXXX-XXXX](https://orcid.org/XXXX-XXXX-XXXX-XXXX)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [janeroe](https://github.com/janeroe)<br>
  <small>
     Department of Something, University of Whatever; Department of Whatever, University of Something
  </small>



## Abstract {.page_break_before}




## Introduction to single cell and imaging multi-omics


## Current multi-omic technologies


## Challenges for interpretation

Need for technology-specific questions and analysis methods vs one size fits all data blender


## Case studies


### scNMT-seq as a case-study for epigenetic regulation

#### Overview and biological question

#### Computational challenges

* Identification of multi-omics signatures that characterise lineage, stage or both.
* Handling missing values
* Do epigenetic changes in some genomic contexts affect cell fate decision more than others? If so, how?

#### Methods for stats/maths analyses and results summary


### scRNA-seq + FISH as a case study for spatial transcriptomics

#### Overview and biological question

#### Computational challenges

* Can scRNA-seq data be overlaid onto seqFISH for resolution enhancement
* What is the minimal number of genes needed for data integration?
* Are there signatures of cellular co-localization or spatial coordinates in the non-spatial scRNA-seq data?

#### Methods for stats/maths analyses and results summary


### Spatial proteomics and cross-study analysis

#### Overview and biological question

#### Computational challenges

* Integrating partially-overlapping proteomic data collected on different patients with similar phenotypes
* Integration of spatial x-y coordinate co-location and co-expression
* Integration with other 'omics datasets (e.g., scRNA-seq) to support the results of these proteomic analyses
* Can we predict the spatial expression patterns of proteins measured on mass-tag but not measured in the MIBI-TOF data?
* What additional information can we learn about the different macrophage and immune populations in breast cancer by conducting integrated analyses of these datasets?

#### Methods for stats/maths analyses and results summary


## Overview of common analytical methods spanning technologies / case studies

* matrix factorization
* neural network / autoencoders


## Data structures and software packages to enable analyses

* Bioc/multiAssayExperiment for single cell
* new classes for proteomics
* PyTorch


## Techniques and challenges for benchmarking methods

* realistic simulation studies
* cross-study validation
* benchmark datasets


## Discussion

### Emerging analytical methods and technologies

### Community needs for data structures, analysis methods, etc 


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
