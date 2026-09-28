# Research software and models

_Last updated: 2026-09-28_

These recommendations concern the identification of research software, including source code, releases, reproducibility packages, machine learning models and software used as tools in research. Software management plans are covered in [Methods, protocols and study preregistrations](methods.md). For the scope of the scope-specific recommendations and how PID systems are preferred, see [Scope-specific recommendations](index.md).

## Deposit source code, create SWHIDs and cite releases with DOIs

_Applies to: researchers, research software engineers, research organisations and repositories._

!!! quote ""

    Deposit source code for research software in the Software Heritage Archive and identify exact software artefacts with SWHIDs. Register DOIs for software releases, reproducibility packages and models that need scholarly citation, and link each DOI to the corresponding SWHID.

??? question "Why?"

    A SWHID is an intrinsic identifier computed from the content it identifies, standardised as ISO/IEC 18670. It can identify a whole repository, a snapshot, a release, a commit, a directory, a file or a fragment of code, and the Software Heritage Archive keeps a copy even if the original repository is moved or deleted. SWHIDs therefore guarantee that the exact code used can be found and verified.

    A DOI for a software release adds kernel metadata: creators with ORCID iDs, organisations with ROR IDs, version, licence, funding and relations to publications and data. Together, the SWHID and the DOI make software both verifiable and part of the PID graph, so that it can be cited and credited like other research outputs.

??? info "How?"

    - Deposit source code in the Software Heritage Archive when results are published, and identify the exact revision used with a SWHID, including qualifiers for the origin and the snapshot.
    - Register DOIs for releases, for example through a repository integrated with the source code platform or through an institutional repository, and record the SWHID as a related identifier in the DOI metadata.
    - Use a concept DOI for the software across its releases (see [Use concept PIDs to group versions and collections](../generic/assigning.md#use-concept-pids-to-group-versions-and-collections)).
    - Include machine-readable metadata in the source code repository, such as CodeMeta or a citation file, and identify licences with SPDX identifiers and their canonical URLs.
    - For machine learning models, register a DOI for each released model and link it to the training data, the code and the environment used.

See also: [Research software and models](../../landscape-analysis/software-models.md) · [SWHID](../../data-on-pids/swhid.md) · [DOI](../../data-on-pids/doi.md) · [Licenses](../../landscape-analysis/licenses.md)

## Identify the software used precisely

_Applies to: researchers, research software engineers and publishers._

!!! quote ""

    When referring to software used in research, identify both the tool, module or library and its version. Use DOIs or SWHIDs for specific releases and code, RRIDs for generic tools where this is established practice, and package or library names with versions or container image digests for dependencies and computing environments.

??? question "Why?"

    Results often depend on the exact software and version used. Generic mentions of a tool in the text of a publication are ambiguous and hard to process. An RRID identifies a tool in general but not a version. Package names with versions and container image digests are not PIDs, but together with the name of the package repository or image registry they identify dependencies and environments precisely, and the checksums remain valid even if a package or image is moved.

??? info "How?"

    - Cite software with its PID in reference lists, including the version used.
    - When using an RRID for a generic tool, state the version separately.
    - Record dependencies with exact versions, for example in lock files, and container images with the registry, image name, tag and full image digest.
    - For reproducibility packages that combine code, data and documentation, register a DOI for the package and link it to the SWHID of the code and the DOIs of the data.
    - For hosted applications used in research, register a DOI with a landing page that describes the application and its versions.

See also: [Research software and models](../../landscape-analysis/software-models.md) · [RRID](../../data-on-pids/rrid.md) · [SWHID](../../data-on-pids/swhid.md)
