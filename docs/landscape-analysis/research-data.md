# Research data

_Last updated: 2026-06-25_

[TODO: Add references]: #

Research data is one of the most central PID use cases in the research lifecycle. Data may be reused, cited, combined, indexed, transferred between repositories, connected to publications and assessed as a research output in its own right. In all of these cases, stable identifiers are needed to distinguish one dataset, data record, collection, release or metadata record from another.

Examples of research data benefitting from being identified with PIDs include:

* Datasets published in general-purpose or institutional data repositories
* Dataset versions and releases
* Collections or aggregations of datasets
* Metadata-only records describing restricted, sensitive or otherwise unavailable data
* Supplementary datasets associated with publications
* Large-scale observational, experimental, survey or computational data products
* Data deposited in domain-specific repositories
* Individual data records in curated disciplinary databases
* Data packages connected to software, workflows, instruments, projects and publications
* etc.

Identifying research data with PIDs serves several core needs in the research ecosystem such as providing information on:

* Citation and attribution of research data as a research output
* Version-specific references to the data used in a publication, analysis or assessment
* Discovery and indexing in repositories, catalogues, search services and knowledge graphs
* Provenance and relationships between data, people, organisations, funders, projects, instruments, software and publications
* Long-term access to metadata, even when access to the underlying data is restricted or the files are no longer available
* Tracking reuse, citations and other forms of impact
* Machine-actionable exchange of metadata between repositories, publishers, funders, CRIS systems and other infrastructures
* Disambiguation between similar datasets, derivative datasets and successive versions
* etc.

The importance of research data PIDs is closely related to the FAIR principles. In particular, FAIR findability requires that data and metadata are assigned globally unique and persistent identifiers. Data citation principles also require that data citations include a persistent method for identification that is machine-actionable, globally unique and widely used by the relevant community.

Research data is rarely a single stable object. It may be corrected, expanded, split, combined, reprocessed, subsetted, migrated between systems or placed under new access conditions. A PID policy for research data therefore needs to clarify what is identified, when a new PID is assigned, how versions and parts are related, what metadata must be maintained, and what persistence commitments are made by the repository or PID manager.

A research data PID also does not necessarily imply open access to the data files themselves. For sensitive, confidential, personal, commercially restricted or security-sensitive data, the PID may identify a landing page, metadata record, access request page or other controlled access point. In these cases, the metadata should remain findable and should clearly state access conditions, legal restrictions and contact or request mechanisms.

## International PIDs and identifiers

### DOI

Active

[DOI](../data-on-pids/doi.md) is the dominant international PID system for published research data and other citable research outputs. For research data, DOI assignment is most often handled through DataCite, either directly by repositories and institutions or through consortia and service providers.

A DOI is particularly well suited for datasets that should be cited, discovered and connected to other research outputs. DataCite metadata supports rich descriptions of data resources, including creators, titles, publishers, publication years, resource types, funding information, related identifiers, versioning information and rights information. These metadata relationships make DOI-based dataset records useful for linking data to publications, researchers, organisations, funders, software, instruments and other outputs.

For research data, DOI assignment should normally resolve to a landing page rather than directly to a downloadable file. The landing page should provide enough metadata for discovery, citation and reuse, as well as information about access conditions. This is especially important for restricted or sensitive data, where the PID may identify a metadata record or access point rather than openly downloadable files.

<!-- Versioning practices vary between repositories, but DOI use for research data should distinguish between references to a specific version and references to a dataset concept or collection when both are relevant. Version-specific citation is especially important when data have been used as evidence in a publication or analysis. Major changes to data should generally result in a new PID, while metadata should connect related versions using relation types such as `IsNewVersionOf`, `IsPreviousVersionOf`, `HasVersion` and `IsVersionOf`. -->

DOIs should not be assigned simply because a file exists. They are most valuable when the assigning organisation can maintain the landing page and metadata, has responsibility for the content, and can describe what the DOI refers to with sufficient precision. Ordinary working files, temporary exports and unstable draft datasets should not normally receive public DOIs unless the repository has a clear publication and versioning model.

### Handle

Active

[Handle](../data-on-pids/handle.md) is a generic PID infrastructure for digital objects. It is also the underlying resolution infrastructure used by DOI. Handles may be used directly by repositories or infrastructures that need persistent identifiers but do not require the full DOI registration and metadata ecosystem.

Handle-based identifiers can be useful for internal repository objects, metadata records, file packages, restricted-access resources or other digital objects that need stable resolution. However, because Handle itself does not prescribe a rich metadata schema or citation-oriented registration workflow, direct Handle use normally requires strong local governance by the repository or infrastructure.

For nationally coordinated research data services, Handle-based systems may be relevant where a service already participates in a Handle federation or where identifiers are needed for objects that are not intended to be cited externally as standalone research outputs.

### ePIC PID

Active

The [ePIC PID service](https://www.pidconsortium.net/) is a Handle-based PID infrastructure used in several European research data and high-performance computing contexts. ePIC identifiers are often used for data objects, collections and other digital resources that need persistent resolution inside distributed research infrastructures.

In a research data context, ePIC PIDs may be appropriate for machine-actionable references between data management systems, storage systems and repository layers. They may also support workflows where large volumes of objects need persistent identifiers before, during or after publication.

Compared with DOI, ePIC is usually less visible as a citation identifier in scholarly publishing. For data that should be cited in publications and indexed broadly across the scholarly communication ecosystem, DOI will normally be the more appropriate primary PID. ePIC PIDs may still be valuable as complementary identifiers in technical infrastructure, data processing and preservation workflows.

### ARK

Active

[ARK](https://arks.org/) (_Archival Resource Key_) is a persistent identifier scheme used by archives, libraries, museums, data centres and other memory organisations. ARKs can identify digital, physical or conceptual objects, and may be used for research data where the maintaining organisation wants a flexible identifier scheme under its own namespace.

ARKs are designed to support persistence commitments and metadata access patterns controlled by the assigning organisation. They can be suitable for data collections, archival material and repository objects where long-term stewardship is handled by an institution with an established preservation mandate.

ARK may be relevant for institutions managing archival, cultural heritage or collection-based research data, or for cases where a repository needs a local PID scheme that can persist independently of a specific platform. Where data should be cited in scholarly literature and indexed in common research data discovery workflows, DOI will often be more recognisable to researchers and publishers.

<!--
### Accession numbers and domain-specific repository identifiers

Active

Many domain repositories assign accession numbers or other repository-specific identifiers to submitted data. These are especially common in life sciences, astronomy, environmental sciences, crystallography, social sciences and other disciplines with mature international data infrastructures. Examples include sequence accession numbers, protein database accessions, crystallographic identifiers, survey study identifiers and identifiers for observational or experimental data products.

Accession numbers often function as the authoritative identifiers within a scientific community. They may be required by journals, used in domain-specific search services and embedded in disciplinary standards. Their persistence depends on the governance and long-term commitments of the repository or consortium that assigns them.

For national PID recommendations, accession numbers should be treated as important community identifiers rather than replaced by generic PIDs. Where a dataset also receives a DOI, metadata should connect the DOI and the accession number using related identifier fields. The DOI can then support citation and cross-domain discovery, while the accession number continues to support disciplinary retrieval and interpretation.
-->

<!--
### Compact identifiers and identifier resolution services

Active

Compact identifiers are structured identifiers consisting of a namespace prefix and a local accession, for example patterns such as `namespace:accession`. In life science and related domains, services such as [Identifiers.org](https://identifiers.org/) provide resolution patterns for many established databases and accession schemes.

Compact identifiers are not always PIDs in the same governance sense as DOI, Handle or ARK. Their usefulness depends on the authority and persistence of the underlying database, namespace and resolver. They are nevertheless important in machine-actionable metadata because they make domain identifiers easier to exchange across systems, APIs and linked-data environments.

For research data recommendations, compact identifiers should be recognised as a practical way to express disciplinary identifiers in metadata, especially where a repository or knowledge graph needs to connect data to biological entities, protocols, instruments, repositories, controlled vocabularies or other domain resources.
-->

<!--
## Swedish national level PIDs and identifiers

There is no separate Swedish PID syntax that should be preferred for all research data. At the national level, the main issue is instead how Swedish research organisations, repositories and infrastructures should apply internationally recognised PID systems in a coordinated way, and which organisations provide practical routes to PID assignment, resolution, metadata management and repository publication.

The actors and services named below are examples of current Swedish or Sweden-facing access routes. They should not be read as an exhaustive catalogue or as a recommendation to use one repository over a more appropriate disciplinary repository.
-->

### DataCite DOI services in Swedish repositories and infrastructures

Active

For published, citable research datasets, DataCite DOI should normally be considered the primary generic PID when no domain-specific identifier has stronger community authority. Swedish universities, authorities, infrastructures, repositories and research groups may encounter DataCite DOI through several organisational routes: direct membership in DataCite, a national or international consortium arrangement, an institutional repository, a shared repository service, a Swedish research infrastructure service or an international domain repository.

At the service level, [DataCite](https://datacite.org/) provides the international DOI registration and metadata infrastructure used for research data. DataCite DOIs and metadata can be registered and managed through DataCite services such as Fabrica and APIs by members, consortia, consortium organisations and repositories.

In Sweden, the [Swedish National Data Service (SND)](https://snd.se/en/services/datacite-doi) provides a DataCite DOI service for Swedish research organisations and research infrastructures through the Swedish DataCite consortium. This is an access route for organisations that need to assign and manage DOIs for research data and other digital objects, but the national recommendation should still focus on governance requirements rather than on a single service provider.

Swedish repositories and infrastructures may also assign DOIs through organisational arrangements under a DataCite member or consortium organisation, including cases where a repository uses a DOI prefix administered through the Swedish DataCite consortium. Such repositories should not be treated as independent national DOI providers only because they mint or expose DOIs. There is a distinction between the actor operating the repository, the actor administering the DOI prefix, and the actor responsible for long-term metadata and landing-page maintenance.

The assignment route is less important than the governance. A Swedish organisation assigning or managing data DOIs should be able to maintain landing pages, metadata, version relationships, rights and access information, contributor information, organisational identifiers, funder information and tombstone metadata if the dataset is withdrawn or no longer available. Repository services that assign DOIs on behalf of researchers should make clear who owns the DOI prefix or repository account, who may update metadata and landing pages, what happens if the service changes platform, and how versions are represented.

### ePIC PID service routes

Active

For Handle-based ePIC identifiers, Swedish organisations may access services through infrastructures that participate in the ePIC ecosystem. [SND's ePIC PID service](https://snd.se/en/services/epic-pid) offers organisations the possibility to assign ePIC identifiers to research data and other digital objects through API-based integration. The international [ePIC Consortium](https://www.pidconsortium.net/) provides the underlying Handle-based service model for registering, storing and resolving ePIC PIDs for the research community.

ePIC PIDs may be useful where Swedish infrastructures need persistent, machine-actionable identifiers inside technical data workflows, for example between storage, processing and repository layers. Because ePIC does not provide the same citation-oriented metadata ecosystem as DataCite DOI, ePIC should normally be treated as complementary to DOI for published, citable datasets rather than as a general replacement.

### URN:NBN

Active

[URN:NBN](../data-on-pids/nbn.md) is primarily used for publications and certain other digital objects in national bibliography contexts. It is not normally the preferred PID for published research datasets, where DOI is more widely supported by repositories, publishers and data citation workflows.

For Swedish organisations, [the National Library of Sweden (KB)](../pid-actors-sweden/kb.md) administers the `urn:nbn:se` namespace and provides the national URN:NBN service. URN:NBN may be relevant for documentation, reports, theses, data management plans, deposited publications or other textual material associated with research data. If used together with research data, metadata should make clear whether the URN:NBN identifies a publication, a data management document, supplementary material or the dataset itself.


<!--
### Domain repository identifiers used by Swedish researchers

Active

Swedish researchers frequently deposit data in international disciplinary repositories that assign accession numbers, database identifiers or other community identifiers. In many fields, these identifiers are the expected way to retrieve, verify and cite the data.

In such cases, repository or archive accession identifiers may be the primary community identifiers, while DOI-based metadata records may still be useful for broader citation, discovery or institutional reporting depending on repository policy.

National recommendations should therefore avoid assuming that a Swedish repository DOI is always the best primary identifier. If a domain repository identifier is the community-authoritative reference, it should be preserved and exposed in local metadata, publication references, CRIS records and assessment contexts. If a DOI is also assigned, the metadata should connect the identifiers and clarify whether the DOI refers to the same object, a collection, a derived dataset, a metadata record or a publication package.
-->

<!--
### Local repository identifiers

Active

Many Swedish universities, infrastructures, public authorities and research groups manage local repositories, storage systems, data portals or administrative systems. These systems often assign local identifiers, database keys, URLs or record numbers. Such identifiers may be useful for administration, but they should not be assumed to be persistent or globally unique unless they are governed as PIDs and supported by a persistence policy.

Local identifiers may still be important as secondary identifiers in metadata. They can support migration, auditing, internal workflows and links between local systems. When local identifiers are exposed externally, they should be connected to a primary PID such as DOI, Handle, ePIC PID, ARK or a domain-specific accession number whenever possible.
-->

<!--
### Administrative and legal identifiers in data metadata

Active

Some identifiers that appear in research data metadata are not PIDs for the dataset itself. Examples may include ethical approval numbers, permit numbers, clinical trial identifiers, local project numbers, archive references, legal case numbers, data access committee identifiers or Swedish organisation numbers for data-holding bodies.

These identifiers may be essential for provenance, compliance and accountability, but they should not be used as substitutes for research data PIDs. National recommendations should encourage repositories to capture them in appropriate metadata fields while keeping a clear distinction between the PID identifying the dataset and identifiers describing related administrative, legal or organisational entities.
-->

<!--
## Issues for national recommendations

Research data PIDs should not be considered in isolation. A dataset PID becomes most valuable when metadata connects it to other PIDs in the research graph, including ORCID iDs for contributors, ROR IDs for organisations, grant identifiers for funding, DOIs for publications and software, and identifiers for instruments, projects and research infrastructures.

The following issues are especially important for national recommendations:

* Define DOI as the preferred generic PID for published, citable research datasets when no domain-specific PID has stronger community authority.
* Treat domain-specific accession numbers and repository identifiers as authoritative community identifiers where that is the established disciplinary practice.
* Identify which Swedish service routes are available for DOI, ePIC PID, URN:NBN and disciplinary repository identifiers, while keeping the recommendation focused on governance, persistence and metadata quality rather than on a single repository choice.
* Require repositories to maintain landing pages and metadata after data files have moved, been restricted, withdrawn or become unavailable.
* Distinguish clearly between dataset concepts, dataset versions, collections, subsets, files, metadata-only records and access request records.
* Define when a new PID must be assigned, especially for major data changes, corrections, reprocessing, new releases and dynamic datasets.
* Ensure that sensitive or restricted data can still be identified through persistent metadata records and clear access information, following the principle that research data should be as open as possible and as restricted as necessary.
* Encourage repositories to expose machine-readable metadata using recognised schemas and related identifier relations.
* Require metadata to include clear citation recommendations, version information, rights information, access conditions and responsible organisations.
* Encourage Swedish research organisations to document their local PID policies, including assignment, versioning, tombstoning, metadata maintenance, transfer of responsibility and long-term stewardship.
* Require repository services and infrastructures that assign PIDs on behalf of researchers to document responsibility for prefix ownership, metadata updates, landing page persistence, service migration and decommissioning.
* Avoid using ordinary URLs, database keys or local record numbers as substitutes for PIDs in external citation and discovery contexts.
* Avoid PID duplication by checking whether identical content has already been assigned a PID elsewhere, and use relation metadata where related objects need to be distinguished.
* Support bidirectional linking between research data and related entities such as people, organisations, funders, projects, publications, software, instruments and infrastructures.
* Clarify how dataset PIDs should be represented in publication reference lists, data availability statements, repository exports, CRIS systems and research assessment workflows.
-->