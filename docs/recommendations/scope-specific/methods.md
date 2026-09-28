# Methods, protocols and study preregistrations

_Last updated: 2026-09-28_

These recommendations concern the identification of methodological resources, such as questionnaires, scales and protocols, study preregistrations, and output management plans, such as data management plans and software management plans. For the scope of the scope-specific recommendations and how PID systems are preferred, see [Scope-specific recommendations](index.md).

## Identify protocols, questionnaires and other conceptual instruments with DOIs

_Applies to: researchers, repositories and publishers._

!!! quote ""

    Publish reusable protocols, questionnaires, scales, interview guides and similar conceptual instruments with DOIs, with metadata that makes clear what kind of instrument it is. Identify each version, translation and adaptation separately, and link them to each other.

??? question "Why?"

    Conceptual instruments shape the data collected with them, and different versions, translations and adaptations may lead to different results. DOIs are commonly used for such instruments, but metadata and relations to other entities may be lacking. This makes the instruments hard to recognise and to connect to the data and publications that use them. Precise resource types and relations make conceptual instruments visible in the PID graph.

??? info "How?"

    - Choose the most specific resource type available in the DOI provider's metadata schema, and describe the kind of instrument in the metadata.
    - Register a new DOI for each version, translation and adaptation, relate them to the original, and use a concept DOI to group versions (see [Use concept PIDs to group versions and collections](../generic/assigning.md#use-concept-pids-to-group-versions-and-collections)).
    - Cite the specific version or translation used, and relate datasets to the instruments used to collect them.
    - For established instruments that are only published in a book or manual, cite alternative identifiers such as ISBN if a DOI is not available.

See also: [Instruments](../../landscape-analysis/instruments.md) · [DOI](../../data-on-pids/doi.md)

## Register studies in recognised registries and link the preregistrations

_Applies to: researchers and research organisations._

!!! quote ""

    Register studies in the registry required or recognised in the field, such as registries for clinical trials, or a registry that assigns DOIs for other kinds of study preregistrations. Link the preregistration identifiers to the resulting data, publications and research activities.

??? question "Why?"

    Registering a study in advance increases transparency and reduces the risk of bias, and it is mandatory for certain studies such as clinical trials. Clinical trial registries provide structured, versioned metadata and identifiers that can be reliably resolved, even when they do not provide full PIDs. For other kinds of studies, non-trial registries may assign DOIs to preregistrations. When preregistrations are linked to the data and publications that follow, the PID graph shows what was planned and what was done.

??? info "How?"

    - Register clinical trials of medicinal products in CTIS as required by EU regulation, and other clinical studies in ClinicalTrials.gov or another WHO primary registry.
    - As a research organisation, provide support for preregistration, such as a local administrator for the registries that require one.
    - For other kinds of studies, use a registry that assigns DOIs to preregistrations, and choose a resource type that identifies the record as a study preregistration.
    - Cite preregistration identifiers in resolvable form in publications and in the metadata of data and research activities, and add links to results in the registry when the study is completed.

See also: [Preregistrations](../../landscape-analysis/preregistrations.md) · [DOI](../../data-on-pids/doi.md)

## Register DOIs for published output management plans

_Applies to: researchers, research organisations, funders and providers of tools for data management plans._

!!! quote ""

    When output management plans such as data management plans and software management plans are published, register them with DOIs, and use PIDs within the plans to link them to the people, organisations, grants, research activities, repositories and datasets they concern.

??? question "Why?"

    Data management plans describe how data will be collected, managed and shared, and they are often required by funders. Software management plans describe how research software will be created, shared and maintained. When a published plan has a DOI, it can be cited and linked to the research activity and the data it describes, so that plans and outcomes can be compared. Plans that use PIDs for people, organisations, funding and repositories can also be processed by machines, for example to prepare repository deposits or to follow up what was planned.

??? info "How?"

    - Register DataCite DOIs for published data management plans and software management plans, using the resource type for output management plans.
    - Use ORCID iDs, ROR IDs, grant PIDs and RAiDs in the plan, and identify planned repositories and standards with their re3data and FAIRsharing records.
    - Register a new version when a plan is updated, and relate the plan to the datasets and software artifacts it has led to.
    - Prefer tools that support machine-actionable plans, for example following the RDA DMP Common Standard.
    - Keep confidential information out of published plans.

See also: [Research data](../../landscape-analysis/research-data.md) · [Research software and models](../../landscape-analysis/software-models.md) · [DOI](../../data-on-pids/doi.md)

