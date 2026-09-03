# Research software and models

_Last updated: 2026-09-03_

Research software could be considered being any software used in the research process. It may be:

* created or modified by researchers or other experts
* used as a specific component in, or making up the entirety of, delimited workflows or processes
* packaged to reproduce deterministic processing or analyses, demonstrating results
* used in fuzzy or non-deterministic processes, such as using ML/AI models running on GPUs
* referred to in generic terms when planning, budgeting or discussing methodology

Research software may often be free and open source software, enabling peer review, future reuse and further development. In other cases, it may be proprietary software requiring a paid license, or vendor-specific software only distributed together with specific research instruments or other equipment. The specific form of research software created or used may vary considerably depending on the discipline, processing needs and availability of common tools and methodology. With the increased use of machine learning and AI applications, research software may come in the form of pre-trained model files.

Transparency of the research process is a core value of open science. With the increasing digitalisation of research, open distribution and unambiguous identification of research software is of paramount importance. The use of PIDs and other software identifiers serve as important methods to achieve this.

## Typical use cases for identifying research software

### Developed or adapted as source code, scripts or project files

Research software may be created as implementation-specific source code or scripts. It may be created from scratch, make use of specific pre-existing software libraries or modules, or it may make up a specific customisation, project setup or syntax for a specific analysis package or workflow.

Research software consisting of source code and other text-based files is often managed using source code control and version management tools, such as Git. Common international source code repositories used for research software include Github and Codeberg.

An example of this use case is to identify the preserved **contents of a source code repository**, and the specific **revisions** or **changes** associated with published results or published methodology.

### Specific releases and reproducibility packaging

Research software using source code management may be versioned and packaged in **specific releases** for a specific purpose. This packaging may be created as a canonical feature release with a version number. It may be a user-oriented release, possibly containing compiled binaries or other additions making the software easier to configure, install and run. If using versioning software such as Git, the repository software may support specific functionality for creating and maintaining releases, such as packaging them as compressed file archives.

Some researchers distribute software together with specific input data and examples of output. The purpose of such packaging is most often to enable and demonstrate the reproduction of specific results, or to provide a reliable reference implementation of a specific methodology. This may be done in a modular fashion where data is obtainable or automatically fetched from a specific source, or in some cases as a single package enclosing everything needed. While the words _replication_ and _reproduction_ may carry different connotations in different fields, an inclusive generic term for this type of distribution is **reproducibility packaging**.

In both these cases, the package and its related materials should be able to be preserved and clearly identified.

### Distribution of models

In machine learning and AI-based workflows, **models** may be trained from scratch, re-used, or enhanced through further training of existing models. When models are used or produced as research software, identifying the specific model, variant and version is important.

Models will often be large files in binary formats, and distribution and identification of models used as research software share many traits with specific software releases created as file archives. 

Moreover, the specific environment in which the model was used and/or trained needs to be specified, such as training data used for training the model, input data used to produce a result using the model, and the specific hardware and software environment used. This is similar to other types of reproducibility packaging and identification of research software.

### Reuse from package repositories or registries

Research software may often be created using existing building blocks, commonly in the form of established **packages or libraries** for a specific language, programming environment or tool. These may be published in internationally recognised open source package repositories, such as _PyPI_ for Python or _CRAN_ for R. Some proprietary software may use similar package repository solutions.

Containerisation is a technique for packaging software as self-contained and complete computing environments ready to run or customise further. Software meant for use in such environments is often packaged in the form of **container images** in an _image registry_. Examples of such registries include Docker Hub or Quay.io. Research software employing containerisation methods may make use of such container images to create reproducible workflows or customise workflows created by others.

It is also possible that software has been created in the form of a valid package or library, or instructions for creating a container image, but has not been published in an official package repository or image registry. In such cases, it may be distributed in a source code repository or as a packaged release.

When using package repositories and image registries, identifying the specific package or image along with the specific version used is important for research software. A canonical name along with a version tag is most often available. Development tools for programming and software deployment may often enable reliable and automated recreation of a specific processing environment using such package/image names and versions.

### Hosted live applications

Research software may be hosted as **live applications** that can run in a web browser using specific hosting solutions. This may be used to allow for reproduction of results, implementation of a methodology and workflow, visualisation, collaboration, data collection or other purposes. The applications may be running constantly, or a user session may be started up at an access point when a user requests it. Such applications need to be identified in a persistent manner.

### Mentioning as a generic tool or solution

Research software is often mentioned in broader terms as **generic tools or solutions** when describing a method, process or conducting planning. This may refer to an existing package, product or solution, i.e. "the transcripts were cleaned using the word processor _X_", "survey data will be collected using the survey tool _Y_", etc. The researchers themselves may not have generated any research software artifacts that need specific identification, or they may not yet have done so at the time of making a reference to the software tool or solution. Nevertheless, needs to clearly identify the software, specific versions of it, and to prevent possible disambiguation will remain.

## International PIDs and identifiers

### SWHID

🟢 Active

[SWHID](../data-on-pids/swhid.md) (SoftWare Hash IDentifier) is a PID system created to meet several specific needs for persistent identification and preservation of research software.

The SWHID concept has been specially designed to handle the architectures of source code repositories created when using version management tools such as Git, Subversion or CVS, and identification of specific elements within them.
SWHID is however not limited to identification of software in source code repositories, and may be used to identify software that is using many other types of distribution methods. 

This means that SWHID provides a flexible solution for many of the use cases for identifying research software.

The landing page of the SWHID PID target will provide a persistent representation of the research software object being identified. This will ensure that a valid copy will still be available if the original source repository or distribution is moved, renamed or deleted.

The [Software Heritage Archive](https://www.softwareheritage.org) has been set up as a globally available infrastructure and SWHID minting service, that will make a persistent copy of the software distribution and/or source code being identified at the time of creating the SWHID[@conf-ArchivingReferencingSource-20].

A SWHID may identify a full code repository, or pinpoint specific versions, releases, commits, directories, files or excerpts of source code within it. This corresponds to different SWHID subtypes, or a combination of them used as qualifiers.

The characters in the SWHID core identifier are computed from the contents of the target that it is identifying, making it an intrinsic PID. Qualifiers added to the SWHID may be used to pinpoint subdivisions or fragments of the software object.

**Example:** _Neuroscout_ is an open source tool for analysing fMRI data. 

It is maintained in a Github repository at: <https://github.com/neuroscout/neuroscout>

A **swh:dir** type SWHID has been created for the neuroscout repository, `swh:1:dir:a358fe02406a82b5e06c79e8ca6edd2b0332f817`. Doing this will also enable identification of several other elements of the repository. The swh:dir SWHID may be resolved at: <https://archive.softwareheritage.org/swh:1:dir:a358fe02406a82b5e06c79e8ca6edd2b0332f817>

A researcher group uses Neuroscout in their workflow and wants to identify the exact version they used in an analysis. They do this by using a SWHID identifying the specific revision used with a **swh:rev** type SWHID, in this case corresponding to a specific commit on Github, `ed79e9c` from September 2, 2022: `swh:1:rev:ed79e9cf4b1ee1320a2d43c72e95f3fd3619c9b7`. This may be resolved at: <https://archive.softwareheritage.org/swh:1:rev:ed79e9cf4b1ee1320a2d43c72e95f3fd3619c9b7>


### DOI

🟢 Active

Just like when using [DOI](../data-on-pids/doi.md) for publications or research data, DOIs may be minted for research software. They are useful for identifying a specific release, such as a .zip file with a software distribution or a reproducibility package. They may also be used for identifying a live application. The DOI [Providers](../pid-concepts/pid-ecosystem.md#provider) DataCite and Crossref both have good support for software objects.

An example of a DOI-based workflow for creating a software release and minting a DOI for it is found in [the integration](https://help.zenodo.org/docs/github/) which enables Github releases to be published automatically on Zenodo and receive a DOI.

**Example:** The article "BoneJ2 - refactoring established research software" discusses use of BoneJ, research software for skeletal imaging based on the common imaging suite ImageJ: <https://doi.org/10.12688/wellcomeopenres.16619.2>

The software is developed through working on it in a Github repository: <https://github.com/bonej-org/BoneJ2>

A specific release of BoneJ, bonej-7.2.2 with the release name radius-r3, was published on Zenodo and received a DOI: <https://doi.org/10.5281/zenodo.21004883>. This was used in the article by the authors when citing and identifying the specific release.

**Example of DOI together with SWHID:** A machine learning preprint was published in 2025, called "Beyond Scaling Curves: Internal Dynamics of Neural Networks Through the NTK Lens" which is accessible at <https://doi.org/10.48550/arXiv.2507.05035>. 

This has an associated replication package with data, scripts and computational notebooks published in a Dataverse repository with a DOI: <https://doi.org/10.18419/DARUS-5717>

The authors also used SWHID to persistently identify exactly which code on their Github source repository was used and to preserve it: <https://archive.softwareheritage.org/swh:1:dir:3cd1808f87c952f33c10f3bb835f820dbfc6b76c;origin=https://github.com/zincware/papyrus;visit=swh:1:snp:4de7f486cb61e63c3aad5adc58754735c19fcfdb;anchor=swh:1:rev:abdae595b7701bbdea00d5c4cc212c79c79575c2>

### RRID

🟢 Active

[RRID](../data-on-pids/rrid.md) is a PID for identification of several different entities, such as reagents or infrastructures, and is commonly used in life sciences and physical sciences. RRID has a specific subtype for software and tools, which is suitable for identifying research software, especially in the use case where it is identifying a generic tool or solution.

An example of this is the imaging software suite _ImageJ_ being assigned the RRID: `RRID:SCR_003070`. This refers to the software tool in general, no specific version of it. This may be resolved using: <https://identifiers.org/RRID:SCR_003070>

**Example:** The article "The GBA variant E326K is associated with alpha-synuclein aggregation and lipid droplet accumulation in human cell lines" makes use of RRIDs for software: <https://doi.org/10.1093/hmg/ddac233>

The RRIDs are here referred using compact identifiers without a resolver. The software references include:

Micro-Manager with `RRID:SCR_000415`  
ImageJ with `RRID:SCR_003070`  
GraphPad Prism with `RRID:SCR_002798`

Since the RRID entiries do not pinpoint software versions, in this case the authors added some manual information on versions within the article text.

**Example:** The article "Allele-specific endogenous tagging and quantitative analysis of β-catenin in colorectal cancer cells" uses a resource table for several of the entities mentioned, including software: <>

The resource table is a common format for making references in several disciplines. In this article, it identifies the following software as generic tools using RRID compact identifiers:

| Software name | Software identifier |
| -------- | ------- |
| Adobe Photoshop CS6 | RRID:SCR_014199 |
| Adobe Illustrator CS6 | RRID:SCR_010279 |
| Adobe Affinity Designer | RRID:SCR_016952 |
| Fiji | RRID:SCR_002285 |
| ImageJ | RRID:SCR_003070 |
| Biorender | RRID:SCR_018361 |
| OriginPro | RRID:SCR_014212 |
| MATLAB | RRID:SCR_013499 |

## Repository packages

## Container images and registries