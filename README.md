# Open and automated manuscript using Manubot

Click on the following badges to access the mauscript:
[![HTML Manuscript](https://img.shields.io/badge/manuscript-HTML-blue.svg)](https://BIRSBiointegration.github.io/whitePaper/)
[![PDF Manuscript](https://img.shields.io/badge/manuscript-PDF-blue.svg)](https://BIRSBiointegration.github.io/whitePaper/manuscript.pdf)
[![GitHub Actions Status](https://github.com/BIRSBiointegration/whitePaper/workflows/Manubot/badge.svg)](https://github.com/BIRSBiointegration/whitePaper/actions)
<!-- usage note: delete CI badges above for services not used by your manuscript -->

## White Paper for the Mathematical Frameworks for Integrative Analysis of Emerging Biological Data Types Workshop
Accurate mathematical models of biological cells during health and disease are essential in understanding biology, advancing precision medicine and treating disease.
Emerging technologies, such as RNA and DNA sequencing give clinical and basic research laboratories great power to quantify tens of thousands of biological molecules and generate highly detailed biological maps at different molecular, spatial and temporal resolutions.
Integrating these diverse data may provide a comprehensive multi-layer view of a biological system that cannot be obtained by considering each dataset individually.
However, currently biological insight is hindered by the inherent complexity of the data and paucity of methods to integrate these data.
By gathering mathematical, statistical and computational experts in the field of genomic data integration, pioneer solutions for data integration problems will be discussed during this workshop.
This white paper describes cutting-edge mathematical, statistical and computational methods to extract reliable information from big biological data.

## How to contribute to the writing of this paper (the easy way)

- On GitHub, go to the [Content folder](https://github.com/BIRSBiointegration/whitePaper/tree/master/content) and make changes to a specific section by editing the document online directly. You will need to write in Rmd format, examples will be given in the document
- Briefly document change if needed and pull your request at the bottom of the document as a new branch 
- Expect some lag before the document is updated.
- Done!


## Manubot

<!-- usage note: do not edit this section -->

Manubot is a system for writing scholarly manuscripts via GitHub.
Manubot automates citations and references, versions manuscripts using git, and enables collaborative writing via GitHub.
An [overview manuscript](https://greenelab.github.io/meta-review/ "Open collaborative writing with Manubot") presents the benefits of collaborative writing with Manubot and its unique features.
The [rootstock repository](https://git.io/fhQH1) is a general purpose template for creating new Manubot instances, as detailed in [`SETUP.md`](SETUP.md).
See [`USAGE.md`](USAGE.md) for documentation how to write a manuscript.

Please open [an issue](https://git.io/fhQHM) for questions related to Manubot usage, bug reports, or general inquiries.

### Repository directories & files

The directories are as follows:

+ [`content`](content) contains the manuscript source, which includes markdown files as well as inputs for citations and references.
  See [`USAGE.md`](USAGE.md) for more information.
+ [`output`](output) contains the outputs (generated files) from Manubot including the resulting manuscripts.
  You should not edit these files manually, because they will get overwritten.
+ [`webpage`](webpage) is a directory meant to be rendered as a static webpage for viewing the HTML manuscript.
+ [`build`](build) contains commands and tools for building the manuscript.
+ [`ci`](ci) contains files necessary for deployment via continuous integration.

### Local execution

The easiest way to run Manubot is to use [continuous integration](#continuous-integration) to rebuild the manuscript when the content changes.
If you want to build a Manubot manuscript locally, install the [conda](https://conda.io) environment as described in [`build`](build).
Then, you can build the manuscript on POSIX systems by running the following commands from this root directory.

```sh
# Activate the manubot conda environment (assumes conda version >= 4.4)
conda activate manubot

# Build the manuscript, saving outputs to the output directory
bash build/build.sh

# At this point, the HTML & PDF outputs will have been created. The remaining
# commands are for serving the webpage to view the HTML manuscript locally.
# This is required to view local images in the HTML output.

# Configure the webpage directory
manubot webpage

# You can now open the manuscript webpage/index.html in a web browser.
# Alternatively, open a local webserver at http://localhost:8000/ with the
# following commands.
cd webpage
python -m http.server
```

Sometimes it's helpful to monitor the content directory and automatically rebuild the manuscript when a change is detected.
The following command, while running, will trigger both the `build.sh` script and `manubot webpage` command upon content changes:

```sh
bash build/autobuild.sh
```

### Continuous Integration

Whenever a pull request is opened, CI (continuous integration) will test whether the changes break the build process to generate a formatted manuscript.
The build process aims to detect common errors, such as invalid citations.
If your pull request build fails, see the CI logs for the cause of failure and revise your pull request accordingly.

When a commit to the `master` branch occurs (for example, when a pull request is merged), CI builds the manuscript and writes the results to the [`gh-pages`](https://github.com/BIRSBiointegration/whitePaper/tree/gh-pages) and [`output`](https://github.com/BIRSBiointegration/whitePaper/tree/output) branches.
The `gh-pages` branch uses [GitHub Pages](https://pages.github.com/) to host the following URLs:

+ **HTML manuscript** at https://BIRSBiointegration.github.io/whitePaper/
+ **PDF manuscript** at https://BIRSBiointegration.github.io/whitePaper/manuscript.pdf

For continuous integration configuration details, see [`.github/workflows/manubot.yaml`](.github/workflows/manubot.yaml) if using GitHub Actions or [`.travis.yml`](.travis.yml) if using Travis CI.

## License

<!--
usage note: edit this section to change the license of your manuscript or source code changes to this repository.
We encourage users to openly license their manuscripts, which is the default as specified below.
-->

[![License: CC BY 4.0](https://img.shields.io/badge/License%20All-CC%20BY%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by/4.0/)
[![License: CC0 1.0](https://img.shields.io/badge/License%20Parts-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

Except when noted otherwise, the entirety of this repository is licensed under a CC BY 4.0 License ([`LICENSE.md`](LICENSE.md)), which allows reuse with attribution.
Please attribute by linking to https://github.com/BIRSBiointegration/whitePaper.

Since CC BY is not ideal for code and data, certain repository components are also released under the CC0 1.0 public domain dedication ([`LICENSE-CC0.md`](LICENSE-CC0.md)).
All files matched by the following glob patterns are dual licensed under CC BY 4.0 and CC0 1.0:

+ `*.sh`
+ `*.py`
+ `*.yml` / `*.yaml`
+ `*.json`
+ `*.bib`
+ `*.tsv`
+ `.gitignore`

All other files are only available under CC BY 4.0, including:

+ `*.md`
+ `*.html`
+ `*.pdf`
+ `*.docx`

Please open [an issue](https://github.com/BIRSBiointegration/whitePaper/issues) for any question related to licensing.
