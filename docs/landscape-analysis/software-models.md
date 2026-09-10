# Research software and models

_Last updated: 2026-09-10_

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

Moreover, the specific environment in which the model was used and/or trained in needs to be specified, such as details on the training data used for training the model, the input data used to produce a result using the model, and the specific hardware and software environment used. This is similar to other types of reproducibility packaging and identification of research software.

### Reuse from package repositories or registries

Research software may often be created using existing building blocks, commonly in the form of established **packages or libraries** for a specific language, programming environment or tool. These may be published in internationally recognised open source package repositories, such as _PyPI_ for Python or _CRAN_ for R. Some proprietary software may use similar package repository solutions.

Containerisation is a technique for packaging software as self-contained and complete computing environments ready to run or customise further. Software meant for use in such environments is often packaged in the form of **container images** in an _image registry_. Examples of such registries include Docker Hub or Quay.io. Research software employing containerisation methods may make use of such container images to create reproducible workflows or customise workflows created by others.

It is also possible that software has been created in the form of a valid package or library, or instructions for creating a container image, but has not been published in an official package repository or image registry. In such cases, it may be distributed in a source code repository or as a packaged release.

When using package repositories and image registries, identifying the specific package or image along with the specific version used is important for research software. A canonical name along with a version tag is most often available. Development tools for programming and software deployment may often enable reliable and automated recreation of specific processing environments using such package/image names and versions.

### Hosted live applications

Research software may be hosted as **live applications** that can run in a web browser using specific hosting solutions. This may be used to allow for reproduction of results, implementation of a methodology and workflow, visualisation, collaboration, data collection or other purposes. The applications may be running constantly, or a user session may be started up at an access point when the user requests it. Such applications need to be identified in a persistent manner.

### Mentioning as a generic tool or solution

Research software is often mentioned in broader terms as **generic tools or solutions** when describing a method, process or conducting planning. This may refer to an existing package, product or solution, i.e. "the transcripts were cleaned using the word processor _X_", "survey data will be collected using the survey tool _Y_", etc. The researchers themselves may not have generated any research software artifacts that need specific identification, or they may not yet have done so at the time of making a reference to the software tool or solution. Nevertheless, in most cases there is a need to clearly identify the software, the specific version, and to prevent possible disambiguation.

## International PIDs and identifiers

### SWHID

🟢 Active

[SWHID](../data-on-pids/swhid.md) (SoftWare Hash IDentifier) is a PID system created to meet several specific needs for persistent identification and preservation of research software.

The SWHID concept has been specially designed to handle the architectures of source code repositories created when using version management tools such as Git, Subversion or CVS, and identification of specific elements within them.
SWHID is however not limited to identification of software in source code repositories, and may be used to identify software that is using many other types of distribution methods. 

This means that SWHID provides a flexible solution for many of the use cases for identifying research software.

The landing page of the SWHID PID target will provide a persistent representation of the research software object being identified. This will ensure that a valid copy will still be available if the original source repository or distribution is moved, renamed or deleted.

The [Software Heritage Archive](https://www.softwareheritage.org) has been set up as a globally available infrastructure and SWHID minting service, that will make a persistent copy of the software distribution and/or source code being identified at the time of creating the SWHID[@conf-ArchivingReferencingSource-20].

A SWHID may identify a full code repository, or pinpoint specific versions, releases, commits, directories, files or excerpts of source code within it. This corresponds to different SWHID core identifier subtypes, or a combination of core identifiers and additional qualifiers.

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

The RRIDs are here referred to using compact identifiers without a resolver URL. The software references include:

Micro-Manager with `RRID:SCR_000415`  
ImageJ with `RRID:SCR_003070`  
GraphPad Prism with `RRID:SCR_002798`

Since the RRID entries themselves do not pinpoint specific software versions, in this case the authors also added some details on versions within the article text.

**Example:** The article "Allele-specific endogenous tagging and quantitative analysis of β-catenin in colorectal cancer cells" uses a resource table for several of the entities mentioned, including software: <https://doi.org/10.7554/eLife.64498>

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

Software distributed in official package repositories, such as libraries and modules meant for direct use in a specific programming environment, will most often be identified by a canonical **package name** along with a specific **package version**. The package repository will most often also hold metadata on a cryptographic checksum for a specific package version, providing additional venues of disambiguiation.

While not being PIDs, these are used as stable identifiers in descriptions as well as in source code and automated workflows that fetch packages from such repositories. Detailed specifications of repository packages may be used to reconstruct environments necessary to run research software, removing the need to constantly redistribute common building blocks.

Specifying the version is often needed to ensure compatibility. It should be noted that specifying the version _used_ is different from identifying what version is _required_ for a specific purpose, and both may be relevant to provide.

Additionally, there may exist a need to identify other constraints, such as that a package needs to be prepared for a specific hardware architecture.

**Example:** The Python module [**pandas**](https://pypi.org/project/pandas/) contains special functions for handling data organised in tabular formats, and is commonly used in research software written in Python. The pandas module is distributed using [PyPI](https://pypi.org) (Python Package Index), which is the official package repository for the Python language. The latest version of pandas at the time of writing is **3.0.5**.

The canonical package name `pandas` will provide sufficient information to identify and obtain the package in general, f.e. using the standard package manager, _pip_, which interacts with PyPI. 

Identification of the package is often provided together with specifications of what version is needed to make research software using it run correctly. This may be done in several ways, such as using the [official requirements syntax](https://pip.pypa.io/en/stable/reference/requirements-file-format/). Using this, expressing that exactly version 3.0.5 is needed would be `pandas == 3.0.5`, while indicating that any version from 3 and onwards may be used would be `pandas >= 3.*`. Other requirements may be specified as detailed in the [dependency specification](https://peps.python.org/pep-0508/).

**Example:** The package [**dplyr**](https://dplyr.tidyverse.org) is a library for the R programming language with functions for subsetting, rearranging and merging data in tabular data structures. It is a part of the larger _tidyverse_ meta-package and commonly used in research software. The [dplyr package](https://cran.r-project.org/web/packages/dplyr/) is published in the official [CRAN](https://cran.r-project.org/) repository for R packages.

Just like in the previous example, the name `dplyr` will identify the package in general, but versions may be specified. This is done using various patterns depending on the command or dependency management tool used. Version _1.2.1_ of dplyr may for example be specified as `dplyr@1.2.1` in the R virtual environment tool _renv_.

## Container images and registries

Research software intended for use in container orchestration workflows and virtualisation are often packaged in container images. These are distributed through _image registries_, infrastructures set up to serve the container images to container management and software deployment tools. The images may be used as building blocks in workflows, or as a starting point for additions and refinements resulting in new images. While this is similar to repository packages, a container image often contains a full processing environment including a compact operating system. The images follow containerisation standards in use by common management tools like Docker or Podman, and may be directly deployed in container orchestration environments such as Kubernetes.

Container images will have an official **image name** which is supplemented by a **tag**, using the following pattern: `imagename:tag`. The image name is the canonical name of the software, and the tag may carry versioning information or other distinguishing information. As an example, specifying `imagename:latest` will identify the latest version of a container image that was added to the image registry. In addition to this, images often come in specific variants adapted for running on different CPU architectures, such as _amd64_ or _arm/v6_.

Each container image also has a cryptographic checksum serving as an additional identification mechanism in addition to the name and tag. This is referred to as the **image ID**. The full image ID is usually a hash value created using the SHA-256 algorithm, expressed using 64 hexadecimal digits. For convenience, the practice of using an abbreviated **short image ID** is also very commonly used to represent the image in listings and comparisons. This is usually the first 12 hexadecimal digits of the full image ID.

The image registries support deduplication, meaning that a specific image or subset of an image that is reused in many contexts only needs to be stored once in the registry. Here, hash identifiers are likewise used to identify the various deduplicated parts of the images, serving as stable references to fetch the data required for reconstructing a specific image.

It should be noted that the images are associated with a specific image registry, and this registry may be publicly accessible and in widespread use, or a private image registry in a closed infrastructure. It is therefore important to provide details on the image registry if this has not been made obvious by workflows and documentation. The checksum-based image IDs will facilitate identification of images that may have been moved or used as a base to build other images, regardless if they exist in a public or private registry.

A common method for specifying how to build a container image, or fetch and modify existing images, is the _Dockerfile_. This is a build script for container management tools that will often hold identifiers for images located in a specific registry.

**Example:** The container image `alpine` contains a compact Linux distribution, Alpine Linux, which is often used as a foundation for building research software workflows. A specific version of the image, `alpine:3.23` is available from the common public image registry [Docker Hub](https://hub.docker.com/layers/library/alpine/3.23/images/sha256-f41a99d2d9c1e8abb8024d0ccd08ec3dfdd9b0e1526c276f7249cd455e7fcae5). The image `alpine:3.23` for the architecture `linux/amd64` has the short image ID `1beb0dc0a51d`, while the full image ID is the full SHA-256 checksum: `1beb0dc0a51de7ff38e3b5274078a2e0b81113ba5c7535e1a03d5913a5edbda3`.