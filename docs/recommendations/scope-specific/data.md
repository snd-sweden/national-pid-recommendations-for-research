# Research data

_Last updated: 2026-09-28_

These recommendations concern the identification of research data, including datasets, collections, versions, metadata records for restricted data and data objects within processing workflows. For the scope of the scope-specific recommendations and how PID systems are preferred, see [Scope-specific recommendations](index.md).

## Use DataCite DOIs for citable research data

_Applies to: repositories, research infrastructures and research organisations._

!!! quote ""

    Use DataCite DOIs as the primary PIDs for published, citable research data. Register rich metadata that links the data to the people, organisations, funding, instruments, software, publications and research activities involved.

??? question "Why?"

    DOIs are the dominant PIDs for research data, and DataCite is the main DOI provider for data. Many repositories and infrastructures create DataCite DOIs in their data publishing workflows. The DataCite Metadata Schema supports creators and contributors identified with ORCID iDs, affiliations identified with ROR IDs, funding references, rights information, version information and typed relations to other PIDs. DataCite metadata is openly available and harvested by discovery services and aggregators, and the relations between DOIs make up a large part of the PID graph for research outputs.

    A DataCite DOI does not require the data itself to be openly available. For sensitive or otherwise restricted data, the DOI can identify a metadata record with information on access conditions, which keeps the data findable and citable. In Sweden, [SND](../../pid-actors-sweden/snd.md) provides DataCite DOIs to research organisations and research infrastructures through the Swedish DataCite consortium.

??? info "How?"

    - Register DOIs through the Swedish DataCite consortium or services already integrated with DataCite.
    - Deposit data in a repository that registers DOIs, rather than only as supplementary files to journal articles.
    - Fill in the metadata beyond the mandatory fields: ORCID iDs, ROR IDs, funder ROR IDs and grant PIDs, a licence URI, and relations to publications, software, instruments, samples and research activities.
    - Always identify the affiliations of creators with ROR IDs.
    - For restricted data, register a DOI for a public metadata record that describes the data and how access can be requested (see [Keep PIDs and descriptive metadata open, even when access is restricted](../generic/choosing.md#keep-pids-and-descriptive-metadata-open-even-when-access-is-restricted)).
    - Register new DOIs for new versions and use concept DOIs to group them (see [Use concept PIDs to group versions and collections](../generic/assigning.md#use-concept-pids-to-group-versions-and-collections)). Do not register DOIs for temporary working files or unstable drafts.
    - For data held in databases and registers, delimit and fix the extract or contribution that was used, for example as a versioned dataset, so that it can be cited with its own DOI.
    - Report data publications to the researcher's organisation, so that they are recorded alongside other outputs (see [Agree on national minimum requirements for PID metadata](../national/priorities.md#agree-on-national-minimum-requirements-for-pid-metadata)).

See also: [Research data](../../landscape-analysis/research-data.md) · [DOI](../../data-on-pids/doi.md) · [SND](../../pid-actors-sweden/snd.md)

## Use ePIC PIDs for fine-grained and workflow-level data objects

_Applies to: research infrastructures, repositories and data services._

!!! quote ""

    Use ePIC PIDs for fine-grained, intermediate or workflow-level data objects that need stable, machine-actionable references, and link them to the DOI of the citable dataset they belong to. Introduce standalone Handle services only for a clearly defined infrastructure need.

??? question "Why?"

    DOIs are best suited for data that is cited and discovered as a research output. Data infrastructures also need persistent references to large numbers of objects that are not cited individually, such as files, intermediate processing results and objects in storage and preservation systems.

    ePIC PID is a Handle-based PID service with consortium governance, a common API and support for typed information stored with each PID, such as checksums, content types, version relations and links to richer metadata. This machine-actionable information makes ePIC PIDs more useful than basic Handles. In Sweden, [SND](../../pid-actors-sweden/snd.md) provides an ePIC PID service. A standalone Handle service, by contrast, has no kernel metadata and requires the organisation to take long-term responsibility for prefixes, resolution and targets.

??? info "How?"

    - Assign ePIC PIDs through SND's ePIC service, integrated in data management and processing systems through its API.
    - Store typed information, such as checksums, content types and links to metadata, using registered PID information types.
    - Link ePIC PIDs to the DOI of the dataset they are part of (see [Prefer PID systems with kernel metadata](../generic/choosing.md#prefer-pid-systems-with-kernel-metadata)).
    - Use test prefixes for objects that do not need persistent identification.

See also: [Research data](../../landscape-analysis/research-data.md) · [ePIC](../../data-on-pids/epic.md) · [Handle](../../data-on-pids/handle.md) · [SND](../../pid-actors-sweden/snd.md)

## Link domain-specific accession numbers to the wider PID graph

_Applies to: researchers, repositories and publishers._

!!! quote ""

    Where a discipline has established repositories that assign accession numbers, deposit data there and cite the accession numbers in resolvable form when possible. Link them to the PIDs of related outputs, so that they become part of the wider PID graph.

??? question "Why?"

    In many disciplines, such as the life sciences, astronomy and the environmental sciences, accession numbers from community repositories are the authoritative identifiers for data, and journals may require them. Their persistence depends on the repositories that assign them, and many of them lack kernel metadata and may lack a common resolver. When possible, use compact identifiers resolved through services such as identifiers.org, and let relations from DOIs of publications and datasets connect them to the rest of the research information landscape.

??? info "How?"

    - Cite accession numbers in resolvable form, for example as compact identifiers through identifiers.org or through the repository's stable URL.
    - Record accession numbers as related identifiers in the metadata of related objects such as research activities, data or publications.

See also: [Research data](../../landscape-analysis/research-data.md)
