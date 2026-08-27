# Research infrastructures

_Last updated: 2026-08-25_

Research infrastructures are facilities, resources and services used by research communities to conduct research and foster innovation. In the PID landscape, this category can include centralised, distributed and virtual infrastructures, such as large-scale facilities, core facilities, service platforms, data repositories, databases, knowledgebases, data portals, scientific collections, archives, or computing resources.

Examples of research infrastructure entities that may be in scope for PID assignment include:

* national and international research facilities;
* independent infrastructure organisations, observatories, laboratories, archives and data centres;
* distributed infrastructures and national nodes where the node is itself an identifiable infrastructure entity;
* university or institute core facilities that are cited or acknowledged as research infrastructure resources;
* research data repositories, databases, knowledgebases and data portals operated as infrastructures.

Research infrastructures are challenging PID targets, because the same name may refer to several different entities: a legal organisation, a distributed consortium, a national node or a service unit. Some of the PID principles and needs for research infrastructures may overlap with [research organisations](organisations.md) in general. PID assignment should therefore begin by defining the infrastructure entity that is being identified. A single infrastructure may need several complementary identifiers when different infrastructure-level entities need to be distinguished.

## International PIDs and identifiers

### ROR ID

🟢 Active

A [ROR ID](../data-on-pids/ror.md) may be used to identify a research infrastructure when the infrastructure is represented as a research organisation or facility. This is relevant for national laboratories, international facilities, observatories, archives, data centres and other infrastructure entities that appear in research metadata as affiliations, operators, publishers, repository hosts, [funders](funding-grants.md) or organisational contributors.

ROR metadata includes organisation types and relationships. The [ROR schema](https://ror.readme.io/docs/ror-data-structure) includes `facility` as one organisation type, and ROR guidance distinguishes facilities in ROR from core facilities in RRID. ROR is therefore appropriate when the PID target is an organisational or facility-level research entity, especially one that is functionally distinct from a parent university or agency[@web-UnderstandingRRIDROR-24].

A ROR ID should normally _not_ be used to identify every internal service, platform or core facility within a larger organisation. In such cases, the parent organisation may have a ROR ID, while the specific infrastructure entity is identified with a more appropriate PID, such as an RRID for a core facility.

**Example:** _National Bioinformatics Infrastructure Sweden_ has been assigned the ROR ID **00enajs79** which may be resolved at: <https://ror.org/00enajs79>

### RRID

🟢 Active

A [RRID](../data-on-pids/rrid.md) (Research Resource Identifier) identifies various subtypes of research resources. RRIDs may be used for identification of a research infrastructure, especially a core facility that needs to be cited or acknowledged consistently in publications. In practice, the RRID system is mainly used within the life sciences and the physical sciences.

RRID and ROR have overlapping but distinct scopes for facilities. RRID is useful when a core facility should be identified as a research resource in methods sections, acknowledgements or reporting workflows. ROR is useful when the entity is an organisation or facility represented as an affiliation or organisational actor. A university-based microscopy, sequencing, imaging or mass spectrometry core facility may therefore have an RRID, while the parent university has a ROR ID[@web-UnderstandingRRIDROR-24].

RRIDs should not be used as a general substitute for organisation identifiers, and it should not be interpreted as a PID for all resources that a research infrastructure operates. In this context, the RRIDs are limited to core facilities and comparable infrastructure entities that are within the RRID subtype scope.

**Example:** The _Lund University Cell and Gene Technologies Core Facility_ has been assigned: **RRID:SCR_028619** which may be resolved at: <https://n2t.net/RRID:SCR_028619>

### re3data

🟢 Active

[re3data.org](https://www.re3data.org/) is a global registry of data repositories. The scope of re3data includes research data repositories, data portals, databases or other services for depositing, preserving, finding and accessing research data[@jrnl-Re3dataIndexingGlobal-23].

A re3data record identifies and describes a research data repository. The re3data record metadata includes repository names, URLs, subjects, keywords, contacts, repository types, certificates, access conditions, data upload conditions, data licences, metadata standards, repository languages and information on whether the repository provides persistent identifiers for deposited objects. The record will be assigned an internal identifier as well as a DOI suitable for citing and referencing. re3data record metadata is available as open metadata under CC0 through structured records and the re3data API.

For Swedish research infrastructures, re3data can support international discovery and policy compliance by making general and domain specific repositories visible in a global registry. The PID target is the repository record and the repository it describes, not the operator organisation, not the datasets deposited in the repository and not the entire research infrastructure if the repository is only one component of it.

**Example:** The _KTH data repository_ has been assigned the repository identifier **r3d100014787** which corresponds to the re3data registry DOI: <https://doi.org/10.17616/R31NJNWJ>

### FAIRsharing

🟢 Active

[FAIRsharing](../data-on-pids/fairsharing.md) is a curated registry describing and interlinking standards, databases, and policies. The FAIRsharing **databases** category allows records that identify research infrastructures providing data resources, such as databases and data repositories[@jrnl-FAIRsharingCommunityApproach-19].

A FAIRsharing record identifies the registry description of a database, repository or similar resource and makes that description discoverable and citable through FAIRsharing record DOIs. FAIRsharing records can connect resources to maintainers, standards, policies, organisations and lifecycle status.

FAIRsharing should be treated as complementary to re3data. re3data is primarily a registry of research data repositories, while FAIRsharing covers standards, databases/repositories and policies and emphasises interlinking between them. For a research infrastructure providing a data-related service, it may be appropriate to maintain both a re3data record and a FAIRsharing record. FAIRsharing curation is handled both centrally and by external contributors, and individual users may become verified maintainers of FAIRsharing records.

**Example:** The _Karolinska Institutet Data Repository (KI DR)_ has a FAIRsharing _database_ type record at: <https://doi.org/10.25504/FAIRsharing.e7a6b5>

## Swedish national level identifiers

### Swedish organisation number (organisationsnummer)

🟢 Active

Swedish organisation numbers are relevant for Swedish data-related research infrastructures, since [Sveriges dataportal](https://dataportal.se) uses them as the basis for recommended URIs for organisations publishing data. 

In DCAT-AP-SE metadata, the publishing organisation is expressed with `dcterms:publisher`. This specifically identifies the responsible publishing organisation in the data portal context, not the research infrastructure, repository, database or data service as an infrastructure entity. When the Swedish organisation number identifies a parent organisation, a suffix may provide a venue for disambiguation.

To avoid duplicate actor records when the same publisher is harvested from several catalogues, Sveriges dataportal recommends a URI using the form `http://dataportal.se/organisation/SE<orgnr>[-suffix]`, where `<orgnr>` is the 10-digit Swedish organisation number (without spaces or hyphens), while the optional suffix may be used to distinguish subdivisions of an organisation [@web-SkordningsspecifikationSverigesDataportal].

<!-- TODO: anpassa till rekommendationsdel snarare än analys

(organisationsnummer) should not replace an infrastructure-level PID. The infrastructure itself should still be identified according to the relevant entity type, for example ROR for an infrastructure organisation or facility, RRID for a core facility, and re3data and/or FAIRsharing for research data repositories, databases and related infrastructure data services.

## Common identifier patterns for research infrastructures

A research infrastructure may need a PID graph rather than a single PID. Typical infrastructure-level patterns include:

* The infrastructure as an independent organisation or facility: use ROR ID where the entity is in scope.
* A university or institute core facility cited in publications: use RRID where the facility is in scope.
* A data repository, database, knowledgebase or data portal operated by the infrastructure: use re3data and/or FAIRsharing records where the service is in scope.
* A distributed infrastructure: identify each distinguishable infrastructure entity at the right level. The consortium, host organisation, national node, repository, core facility and data service may each need different identifiers.

When several identifiers exist for the same or related entities, metadata should clearly express whether the relationship is identity, ownership, hosting, funding, membership, access provision, acknowledgement or citation. Ambiguous identifier use can otherwise merge distinct entities and make impact tracking, attribution and long-term curation unreliable.
-->
