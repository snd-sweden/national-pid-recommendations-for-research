# Research data

_Last updated: 2026-06-27_

[TODO: Add references]: #

The identification of research data is one of the most central PID use cases in the research lifecycle. Data may be reused, cited, combined, indexed, transferred between repositories, connected to publications and assessed as research outputs in their own right. In all of these cases, stable identifiers are needed to distinguish one dataset, data record, collection, release or metadata record from another.

There are many definitions of what can be considered research data, although most assume that it must somehow be actively used in research. However, many of the use cases described below may also be relevant for _prospective_ research data, i.e. materials that have been produced or curated by an actor and are considered being of possible relevance for use in _future_ research.

## Examples of research data

Examples of research data entities benefitting from being identified with PIDs include:

* Datasets published in general-purpose or institutional data repositories
* Data deposited in domain-specific repositories
* Metadata-only records describing restricted data, or data that is not directly downloadable for other reasons
* Datasets used as inputs in research activities, such as pre-existing or collected data
* Datasets underlying results published in research publications
* Datasets required by replication packaging (i.e. source code or other tools enabling independent reproduction of results)
* Collections or aggregations of datasets
* Specific dataset versions and releases
* Large-scale observational, experimental, survey or computational data products
* Individual data records in curated disciplinary databases
* Delimited selections of larger data entities, such as a subsets of a database, registry or collection
* Formal descriptions of how to reconstruct data, such as future-proof and reproducible database, registry or API queries
* Meta-referencing datasets, such as comprehensive machine-readable reference lists of materials used as research data
* Datasets otherwise connected to software, workflows, instruments, projects and publications
* etc.

## Needs for identifying and describing research data

Identifying research data with PIDs serves several core needs in the research ecosystem:

* Citation and attribution of research data, i.e. re-used datasets as well as data as new research outputs
* Clear distinction of data as independently addressable research outputs
* Version-specific references to the data used in a publication, analysis or assessment
* Sunsetting the practice where data becomes semi-hidden "supplementary files" in journal CMS systems
* Discovery and indexing in repositories, catalogues, search services and knowledge graphs
* Provenance and relationships between data, people, organisations, funders, instruments, software, publications and research activities
* Long-term access to metadata, even when access to the underlying data is restricted or the files are no longer available
* Tracking reuse, citations and other forms of impact
* Machine-actionable exchange of metadata between repositories, publishers, funders, CRIS systems and other infrastructures
* Disambiguation between similar datasets, derivative datasets and successive versions
* Identifying data at various stages of a processing workflow
* etc.

## FAIR research data

The importance of research data PIDs is closely related to the FAIR principles[@jrnl-FAIRGuidingPrinciples-16]. In particular, FAIR _findability_ underlines the need for data and metadata to be assigned globally unique and persistent identifiers.

A research data PID does not necessarily imply open access to the data files themselves. For sensitive, confidential or commercially restricted data, the PID may identify a metadata record, access request page or other controlled access point described by a [landing page](../pid-concepts/landing-pages.md). In these cases, the metadata should remain findable and should clearly state access conditions, legal restrictions and contact or request mechanisms to be aligned with the FAIR concept of _accessibility_.

Research data are rarely single, stable objects. Data may be corrected, expanded, split, combined, reprocessed, subsetted, migrated between systems or placed under new access conditions. To facilitate FAIR data practices, PID policies for research data may help with clarification of what is identified, when a new PID is assigned, how versions and parts are related, what metadata must be maintained, and what persistence commitments are made by the repository or PID manager.

## International PIDs and identifiers

### DOI

🟢 Active

[DOI](../data-on-pids/doi.md) is the dominant PID system for published research data and many other types of citable research outputs. For research data, DOI assignment is most often handled through [DataCite](https://www.datacite.org), either directly by repositories and institutions or through consortia and service providers. Some data-related DOIs are created through Crossref or certain infrastructure-specific DOI providers.

A DOI is particularly well suited for datasets that should be cited, discovered and connected to other research outputs. DataCite [kernel metadata](../pid-concepts/kernel-metadata.md) supports rich descriptions of data resources, including creators, titles, publishers, publication years, resource types, versioning information and rights information. Formal relations to other PIDs are qualified by specific relation types and likewise expressed in the DOI metadata. Such relations enable linking data to publications, researchers, organisations, research activities, grants, software, instruments and other outputs. 

For datasets, DOI assignment will normally resolve to a landing page rather than directly to a downloadable file. The landing page is meant to provide sufficient metadata for discovery, citation and reuse. In the case of open access data, this is typically accompanied by links for downloading data. When data are restricted, further details on access conditions and access points will be provided.

Versioning practices vary between repositories, but DOI makes it possible to distinguish between references to a specific version of a dataset and references to a canonical [concept PID](../pid-concepts/concept-pids.md), representing the sum of all versions. Such DOIs may also represent collections, and will then act as parent PIDs related to several different child objects.

DOIs should not be assigned simply because a file exists. They are most valuable when the assigning organisation can maintain the landing page and metadata over time, is responsibile for the content, and can describe what the DOI refers to with sufficient precision. Temporary working files and unstable draft datasets should not normally receive public DOIs unless the repository has a clear publication and versioning model, such as publishing data from each stage of a workflow.

In Sweden, the [Swedish National Data Service (SND)](../pid-actors-sweden/snd.md) provides a [DataCite DOI service](https://snd.se/en/services/datacite-doi) for Swedish research organisations and research infrastructures through the Swedish DataCite consortium.

**Example:** The dataset _Neutron study of the topological flux model of hydrogen ions in water ice_ has been assigned the DataCite DOI `10.5442/ND000001` which is is resolvable at: <https://doi.org/10.5442/ND000001>  
Rich metadata is available on the landing page as well as in the DataCite kernel metadata, accessible at: <https://api.datacite.org/dois/10.5442/ND000001>

This example uses DOI kernel metadata to expresses formal relations between the dataset and the instrument that collected the data, a publication describing the instrument, and a publication citing the dataset, identified by their respective (non-dataset) DOIs. It also employs ORCID to identify several of the contributors. However, affiliations and other organisational metadata are only listed as free-text strings, and there is no funder information. Such metadata could be expressed with ROR IDs. Metadata may be added or updated through interacting with the DataCite DOI service or a tool communicating with it.

### Handle

🟢 Active

The [Handle](../data-on-pids/handle.md) system is a generic PID infrastructure for digital objects. It is also the underlying infrastructure used by DOI and several other PID systems. 

Handle-based identifiers can be useful for internal repository objects, metadata records, file packages, restricted-access resources or other digital objects that need stable resolution. Handles may be used by repositories or infrastructures that need persistent identifiers, but do not require a global registration and metadata ecosystem. However, because Handle itself does not prescribe a rich metadata schema or citation-oriented registration workflows, direct Handle use normally requires careful local governance by the repository or infrastructure. Depending on the implementation, other means of providing metadata in the PID target may supplement the lack of PID kernel metadata.

For research data services, Handle-based systems may more often be relevant where a service already participates in a Handle federation or where identifiers are needed for objects that are not intended to be cited externally as standalone research outputs.

**Example:** The dataset _Data for the study "Physiological assessment of the psychological flow state using wearable devices"_ has been assigned the Handle `21.15109/ARP/968SUZ` resolvable at <https://hdl.handle.net/21.15109/ARP/968SUZ>

While the Handle system itself contains no kernel metadata, the PID target is served by an instance of the Dataverse repository software, enabling multiple standardised access methods to rich metadata.

### ePIC PID

🟢 Active

The [ePIC PID](../data-on-pids/epic.md) service is a Handle-based PID infrastructure used in several European research data and high-performance computing contexts. ePIC identifiers are often used for data objects, collections and other digital resources that need persistent resolution inside distributed [research infrastructures](research-infrastructures.md).

In a research data context, ePIC PIDs may be appropriate for machine-actionable references between data management systems, storage systems and repository layers. They may also support workflows where large volumes of objects need persistent identifiers before, during or after publication. Other use cases for ePIC PIDs include transient data, specific processing stages of data, and other systematic PID assignment workflows where it is not clear which objects may be of interest to cite or refer to in the future.

Compared with DOI, ePIC is usually less visible as a citation identifier in scholarly publishing. For data that should be cited in publications and indexed broadly across the scholarly communication ecosystem, DOI will normally be the more appropriate primary PID. ePIC PIDs are valuable complementary identifiers in technical infrastructure, data processing and preservation workflows.

In Sweden, the [ePIC PID service](https://snd.se/en/services/epic-pid) provided by the [Swedish National Data Service (SND)](../pid-actors-sweden/snd.md) offers organisations the possibility to assign ePIC identifiers to research data and other digital objects through API-based integration.

**Example:** The data file `OCR-D-OCR_MTAwOTE3OTA2_page-0003.xml` in the DARIAH-DE repository has been assigned the ePIC PID `21.11113/a83e8846-aad6-4bf1-acb6-8626b0614f6c` which may be resolved using the standard Handle resolver: <http://hdl.handle.net/21.11113/a83e8846-aad6-4bf1-acb6-8626b0614f6c>

This is partial data from attempts to extract various petroleum-related mentions using OCR processing of a dataset of scanned journals. The XML data assigned an ePIC PID is output from a specific stage of the OCR processing.

### ARK

🟢 Active

[ARK](https://arks.org/) (_Archival Resource Key_) is a PID system used by archives, libraries, museums, government agencies and many other organisations and infrastructures. It has seen widespread use in cultural heritage institutions, but is not limited in scope to them. ARKs can identify digital or conceptual objects as well as physical objects, and may be used for research data where the maintaining organisation wants a flexible identifier scheme under its own namespace and optionally its own resolver.

ARKs are designed to support persistence commitments and metadata access patterns controlled by the assigning organisation. They can be suitable for data collections, archival material and repository objects where long-term stewardship is handled by an institution with an established preservation mandate.

ARK may be especially relevant for institutions managing archival, cultural heritage or collection-based research data, or for cases where a repository needs a local PID scheme that can persist independently of a specific platform. Where data should be cited in scholarly literature and indexed in common research data discovery workflows, DOIs will often be more recognisable to researchers and publishers.

**Example:** The archaeological dataset _Geometric data for tumuli in Dhar Tagant, Mauritania_ has been assigned the ARK `ark:/29072/ora_777409284f32478c924d09ceeb61f75d` which is resolvable using the globally routing resolver: <https://n2t.net/ark:/29072/ora_777409284f32478c924d09ceeb61f75d>

## Accession numbers and other domain-specific repository identifiers

Many domain-specific infrastructures assign accession numbers or similar identifiers to submitted data. These are especially common in life sciences, astronomy, environmental sciences and other disciplines with long-established international data infrastructures. Examples include sequence accession numbers, protein database accessions, crystallographic identifiers and identifiers for observational or experimental data products.

Accession numbers often function as the authoritative identifiers within a scientific community. They may be required by journals, used in domain-specific search services and embedded in disciplinary standards. Their persistence depends on the governance and long-term commitments of the repository or consortium that assigns them.

Compact identifiers are structured identifiers consisting of a namespace prefix and a local accession, for example patterns such as `namespace:accession`. This is a common method of referring to accession numbers. Compact identifiers are not always PIDs in the same governance sense as DOI, Handle or ARK. A resolver must be configured to handle the specific namespace for a compact identifier to be directly resolvable.

### Resolving accession numbers and compact identifiers

An accession number may be resolvable using a dedicated resolver, and may thus qualify as a PID. A common resolver infrastructure handling many accession numbers using compact identifiers is found at: <https://identifiers.org>. The entity identified by the accession number may also have been assigned a PID using another system, serving as an alternative means of identification.

Some accession numbers rely on specific legacy access paths, such as registry searches, database queries or other lookup procedures. These may not always be directly resolvable as PIDs.

**Example:** `pdb:2gc4` is an accession number assigned by the _Protein Data Bank (PDB)_, identifying an experimentally determined three-dimensional macromolecular structure. It may also be reliably resolved as a PID using: <https://identifiers.org/pdb:2gc4>

**Example:** `GSE10072` is an accession number for a functional-genomics dataset, assigned by the database _NCBI Gene Expression Omnibus (GEO)_. A lookup can be performed using the NCBI [GEO accession display tool](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi). This reveals that it may be reliably accessed using the URL: <https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE10072>  
For this accession number, identifiers.org will be able to resolve it if the appropriate namespace prefix `GEO:` is provided: <http://identifiers.org/GEO:GSE10072>

**Example:** `CM970576` is an accession number for a gene mutation, assigned by the database _Human Gene Mutation Database (HGMD)_. It does not have an obvious web resolver, but a lookup can be performed after registering for database access at [HGMD](https://www.hgmd.cf.ac.uk/). This will reveal a landing page at: <https://www.hgmd.cf.ac.uk/ac/gene.php?gene=GALNS&accession=CM970576>  
As opposed to its mutation, the parent gene is resolvable with the compact identifier `HGMD:GALNS` using: <http://identifiers.org/HGMD:GALNS>

<!-- TODO: keep for reference, recommendation section
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