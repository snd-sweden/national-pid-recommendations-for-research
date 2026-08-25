# Research infrastructures

_Last updated: 2026-06-26_

Research infrastructures are facilities, resources and services used by research communities to conduct research and foster innovation. In the PID landscape, this category can include centralised, distributed and virtual infrastructures, such as large-scale facilities, core facilities, service platforms, data repositories, databases, knowledgebases, data portals, scientific collections, archives, computing resources and access programmes.

Examples of research infrastructure entities that may be in scope for PID assignment include:

* national and international research facilities;
* independent infrastructure organisations, observatories, laboratories, archives and data centres;
* distributed infrastructures and national nodes where the node is itself an identifiable infrastructure entity;
* university or institute core facilities that are cited or acknowledged as research infrastructure resources;
* research data repositories, databases, knowledgebases and data portals operated by infrastructures.

Research infrastructures are challenging PID targets because the same name may refer to several different entities: a legal organisation, a distributed consortium, a national node, a service unit, a repository, a dataset collection, a project or a funding activity. PID assignment should therefore begin by defining the infrastructure entity that is being identified. A single infrastructure may need several complementary identifiers when different infrastructure-level entities need to be distinguished.

## International PIDs and identifiers

### ROR ID

Active

A [ROR ID](../data-on-pids/ror.md) can identify a research infrastructure when the infrastructure is represented as a research organisation or facility. This is relevant for national laboratories, international facilities, observatories, archives, data centres and other infrastructure entities that appear in research metadata as affiliations, operators, publishers, repository hosts, funders or organisational contributors.

ROR metadata includes organisation types and relationships. The ROR schema includes `facility` as one organisation type, and ROR guidance distinguishes facilities in ROR from core facilities in RRID. ROR is therefore appropriate when the PID target is an organisational or facility-level research entity, especially one that is functionally distinct from a parent university or agency.

A ROR ID should normally not be used to identify every internal service, platform or core facility within a larger organisation. In such cases, the parent organisation may have a ROR ID while the specific infrastructure entity is identified with a more appropriate PID, such as an RRID for a core facility.

### Research Resource Identifier (RRID)

Active

A Research Resource Identifier (RRID) identifies research resources used as inputs to experiments and research workflows. In this analysis, RRID is included only where the identified entity is a research infrastructure entity, especially a core facility that needs to be cited or acknowledged consistently in publications.

RRID and ROR have overlapping but distinct scopes for facilities. RRID is useful when a core facility should be identified as a research resource in methods sections, acknowledgements or reporting workflows. ROR is useful when the entity is an organisation or facility represented as an affiliation or organisational actor. A university-based microscopy, sequencing, imaging or mass spectrometry core facility may therefore have an RRID, while the parent university has a ROR ID.

RRID should not be used as a general substitute for organisation identifiers, and it should not be treated here as a PID for all resources that a research infrastructure operates. Its relevance for this landscape analysis is limited to core facilities and comparable infrastructure entities that are in scope for the RRID registry.

### re3data record DOI and re3data repository identifier

Active

[re3data.org](https://www.re3data.org/) is a global registry of research data repositories. It is not a general register of all research infrastructures, but it is directly relevant for infrastructures that are research data repositories, data portals, databases or other services for depositing, preserving, finding and accessing research data.

A re3data record identifies and describes a research data repository. re3data records include repository names, URLs, subjects, keywords, contacts, repository types, certificates, access conditions, data upload conditions, data licences, metadata standards, repository languages and information on whether the repository provides persistent identifiers for deposited objects. re3data metadata is available as open metadata under CC0 through structured records and an API.

For Swedish research infrastructures, re3data can support international discovery and policy compliance by making national and domain repositories visible in a global registry. The PID target is the repository record and the repository it describes, not the operator organisation, not the datasets deposited in the repository and not the entire research infrastructure if the repository is only one component of it.

### FAIRsharing record DOI and FAIRsharing identifier

Active

[FAIRsharing](https://fairsharing.org/) is a curated resource describing and interlinking standards, databases, repositories and data policies. In this analysis, FAIRsharing is included only for records that identify research infrastructure data resources, such as databases and repositories. Standards and policies may be related FAIRsharing records, but they are not treated here as research infrastructure PID targets.

A FAIRsharing record can identify the registry description of a database, repository or related infrastructure data resource and make that description discoverable and citable. FAIRsharing records can connect resources to maintainers, implemented standards, recommended standards, policy endorsements, organisations and lifecycle status. FAIRsharing record DOIs make it possible to cite the registry record for a database or repository even when the resource itself also has its own local identifier or PID.

FAIRsharing should be treated as complementary to re3data. re3data is primarily a registry of research data repositories, while FAIRsharing covers standards, databases, repositories and policies and emphasises interlinking between them. For a research infrastructure data service, it may be appropriate to maintain both a re3data record and a FAIRsharing record when both services are in scope.

## Swedish national level PIDs and identifiers

No Swedish national PID system is listed here as an active PID system specifically for identifying research infrastructures. Swedish organisation numbers, Swedish Research Council infrastructure records, local service catalogue identifiers and access-management attributes can be useful administrative or operational references, but they are not included as PID systems for research infrastructures in this analysis.

Swedish organisation numbers are nevertheless important in Swedish open-data metadata because Sveriges dataportal uses them as the basis for recommended URIs for publishing organisations. In DCAT-AP-SE metadata, the publishing organisation is expressed with dcterms:publisher. To avoid duplicate actor records when the same publisher is harvested from several catalogues, the dataportal recommends a URI on the form http://dataportal.se/organisation/SE<orgnr>[-suffix], where <orgnr> is the 10-digit Swedish organisation number without spaces or hyphens and the optional suffix is used by agreement when several publishing organisations share the same organisation number. This identifies the publisher/actor in the data portal context, not the research infrastructure, repository, database or data service as an infrastructure entity.

For Swedish research infrastructures that publish metadata through Sveriges dataportal, the organisation-number-based dataportal URI can therefore be used to identify the Swedish publishing organisation responsible for the catalogue or dataset metadata. It should not replace an infrastructure-level PID. The infrastructure itself should still be identified according to the relevant entity type, for example ROR for an infrastructure organisation or facility, RRID for a core facility, and re3data and/or FAIRsharing for research data repositories, databases and related infrastructure data services.

## Common identifier patterns for research infrastructures

A research infrastructure may need a PID graph rather than a single PID. Typical infrastructure-level patterns include:

* The infrastructure as an independent organisation or facility: use ROR ID where the entity is in scope.
* A university or institute core facility cited in publications: use RRID where the facility is in scope.
* A data repository, database, knowledgebase or data portal operated by the infrastructure: use re3data and/or FAIRsharing records where the service is in scope.
* A distributed infrastructure: identify each distinguishable infrastructure entity at the right level. The consortium, host organisation, national node, repository, core facility and data service may each need different identifiers.

When several identifiers exist for the same or related entities, metadata should clearly express whether the relationship is identity, ownership, hosting, funding, membership, access provision, acknowledgement or citation. Ambiguous identifier use can otherwise merge distinct entities and make impact tracking, attribution and long-term curation unreliable.

## Selected references

* [ROR data structure](https://ror.readme.io/docs/ror-data-structure)
* [Understanding RRID and ROR for Facilities](https://ror.org/blog/2024-11-26-rrid-ror-facilities/)
* [Research Resource Identifier](https://www.rrids.org/)
* [re3data.org About](https://www.re3data.org/about)
* [re3data - Indexing the Global Research Data Repository Landscape Since 2012](https://www.nature.com/articles/s41597-023-02462-y)
* [FAIRsharing](https://fairsharing.org/)
* [FAIRsharing as a community approach to standards, repositories and policies](https://www.nature.com/articles/s41587-019-0080-8)
* [Sveriges dataportal: Skördningsspecifikation](https://docs.dataportal.se/dcat/docs/harvesting/)
