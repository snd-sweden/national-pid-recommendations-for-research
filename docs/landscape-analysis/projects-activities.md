# Research projects and research activities

<<<<<<< HEAD
_Last updated: 2026-08-18_

Research projects and research activities are time-bounded endeavours that bring together people, organisations, funding, infrastructure, methods and research outputs in order to achieve a defined aim. Unlike a publication or dataset, a project is not normally fixed at a single publication event. Its title, participants, organisational responsibility, funding, scope and outputs may change during the research lifecycle.

Examples of research projects and activities benefitting from being identified with PIDs include:

* Externally funded research projects
* Internally funded or unfunded research projects
* Collaborative projects and consortia
* Subprojects, work packages and defined project phases
* Field campaigns, expeditions and field seasons
* Experiments, observational studies and other time-bounded investigations
* Research activities making use of one or more research infrastructures
* Long-running studies divided into separately managed activities or waves

Identifying projects and activities serves several core needs in the research ecosystem, such as:

* Distinguishing projects with identical, similar or changing titles
* Linking researchers and contributors, organisations, grants, infrastructures, instruments and outputs to the activity in which they participated
* Preserving provenance and a history of changes throughout the activity lifecycle
* Expressing relationships between programmes, projects, subprojects and related activities
* Supporting discovery, administration, reporting, assessment and impact analysis
* Allowing project information to be exchanged between funder systems, CRIS systems, repositories and other research information infrastructures

A research project should be distinguished conceptually from the funding that supports it. A grant or award is something a researcher or organisation receives, while a project or activity is something they carry out. One project may be supported by several grants, and one grant may support several projects. Project PIDs and grant identifiers should therefore be linked rather than treated as interchangeable. Identifiers for grants and awards are discussed in the [funding landscape analysis](funding.md).

This analysis concerns identifiers for the project or activity entity itself. Identifiers for outputs, [preregistrations](preregistrations.md), [protocols](protocols.md), research infrastructures and other related entities are covered in their respective landscape analyses.


## International PIDs and identifiers

### RAiD (Research Activity Identifier)

🟢 Active

[RAiD](https://www.raid.org/) is a PID and global registry designed specifically for research projects and activities. It is governed by [ISO 23527:2022, Information and documentation — Research activity identifier (RAiD)](https://www.iso.org/standard/75931.html). The Australian Research Data Commons (ARDC) acts as the ISO Registration Authority and coordinates a federated model in which RAiD Registration Agencies provide services for particular regions or constituencies.

RAiD is intended to identify a time-bounded research endeavour independently of any particular grant, output, institution or information system. It may be assigned near the beginning of an activity and remain unchanged when project metadata develops over time. Related RAiDs can be used to connect projects, subprojects and other associated activities. Durable organisational units such as departments and laboratories should instead be identified using an organisational PID such as ROR ID.

A RAiD is expressed as a resolvable URL in the form `https://raid.org/prefix/suffix`. RAiD uses [DataCite DOI infrastructure](https://support.datacite.org/docs/raids), meaning that a RAiD is also a valid DOI and that a core subset of its metadata is registered with DataCite. The full, project-specific metadata record is maintained by the RAiD service. RAiD should therefore be understood as a specialised project PID system and registry built on DOI infrastructure, rather than merely a conventional DOI assigned to a project landing page.

The [RAiD metadata schema](https://metadata.raid.org/) is designed for information that changes during a project lifecycle. It can describe titles, dates, descriptions, contributors and their roles, participating organisations, related objects, alternate identifiers, related RAiDs and access conditions. Other PIDs can be connected to the record, including ORCID iDs for contributors, ROR IDs for organisations, grant identifiers and DOIs for publications, data, software and other outputs. The service also preserves a change history and supports more than one authorised party maintaining a record.

RAiD records are intended for project information that can ultimately be made public. [Temporary embargo](https://metadata.raid.org/en/latest/core/access.html) is supported, but confidential or security-sensitive project information should not be placed in the public registry. This is important for projects involving commercially sensitive information, protected research, personal data or national-security considerations: the PID record should contain only metadata suitable for the intended access level.

RAiD is operational, but international adoption is still developing. The service is established in Australia and New Zealand, while European provision is being developed through [SURF](https://www.surf.nl/en/services/publishing/raid). During 2026, SURF describes its implementation as a pilot, while the RAiD website identifies SURF as the Registration Agency for Europe. No Swedish Registration Agency or Swedish RAiD Service Point was identified in the [public RAiD information](https://www.raid.org/) reviewed for this analysis. Swedish organisations interested in early adoption would therefore need to clarify onboarding and service conditions with the European or global RAiD service.

RAiD has the strongest direct semantic fit among the systems reviewed here because it identifies the research activity itself and is designed for changing, relational project metadata. Its value depends, however, on integration with local systems and clear metadata stewardship. A Swedish implementation would need to determine when a RAiD is minted, which organisation is responsible for the record, how project boundaries and subprojects are defined, how records are maintained after project closure, and how RAiDs are linked to SweCRIS, funder identifiers and local project IDs.


### DataCite DOI for projects

🟢 Active

A generic [DataCite DOI](../data-on-pids/doi.md) may be registered directly for a project. The DataCite Metadata Schema includes `Project` as a value for `resourceTypeGeneral`, defined for a planned endeavour or activity intended to achieve a particular aim using allocated resources. DataCite explicitly distinguishes the project itself from a project report, protocol, study registration or other output, which should be assigned the resource type appropriate to that object. See [DataCite's guidance on project tracking and identification](https://support.datacite.org/docs/project-tracking-and-identification).

A project DOI can connect the project to contributors, organisations, funding and outputs through DataCite relationship metadata and the DataCite PID Graph. [DataCite Metadata Schema 4.7](https://schema.datacite.org/meta/kernel-4.7/) also recognises `RAiD` as a related identifier type, enabling explicit links between DataCite records and RAiDs.

A conventional DataCite project DOI is a lighter and more flexible implementation than the full RAiD service. It can provide global resolution, kernel metadata and links to related entities, but it does not by itself provide the RAiD-specific metadata model, federated registry, authenticated multi-party editing or project change history. The organisation registering the DOI must maintain the landing page, target URL and metadata for the required persistence period.

RAiD and a generic DataCite project DOI are therefore not different underlying identifier technologies: RAiD itself uses a DataCite DOI. They represent different service and governance models. Registering a conventional project DOI may be appropriate where a responsible organisation has a well-defined project registry and long-term metadata stewardship but does not require the full RAiD functionality. Coordinated practice is needed to avoid assigning an unlinked generic project DOI and a RAiD to the same project.


### CORDIS project DOI and Grant Agreement ID

🟢 Active

[CORDIS](https://cordis.europa.eu/) is the European Commission's information service for EU research and development projects. CORDIS project records include the project acronym and title, Grant Agreement ID, programme, dates, funding, participating organisations and links to results.

Each CORDIS project funded from Horizon 2020 onwards is assigned a DOI in the form `10.3030/{Grant Agreement ID}`. For example, the OPUS project with Grant Agreement ID `101058471` has the DOI <https://doi.org/10.3030/101058471>. The DOI is displayed as the project's DOI in CORDIS and provides a persistent, globally resolvable reference to the CORDIS record.

The European Commission registers these identifiers as grant DOIs through the Publications Office of the European Union and [Crossref's Grant Linking System](https://www.crossref.org/blog/from-commitment-to-connection-200000-grants-in-the-scholarly-record/). Their identity is consequently tied closely to the EU grant agreement or funded action. [Crossref's grant metadata model](https://www.crossref.org/documentation/schema-library/markup-guide-record-types/grants/) may describe one or more projects, but the DOI is assigned at grant level. The CORDIS DOI should therefore not be assumed to represent a generic project PID independent of funding in every context.

CORDIS DOIs are important identifiers for Swedish participation in Horizon 2020 and Horizon Europe projects. Their scope is nevertheless limited to projects represented in CORDIS, and they do not cover unfunded activities, institutionally funded projects or project subdivisions that do not have separate EU grant agreements. Where a project also has a RAiD, the CORDIS DOI or Grant Agreement ID should be retained as a related funding or alternate identifier rather than replaced.


## Swedish national level PIDs and identifiers

### SweCRIS Project-ID

🟢 Active

[SweCRIS](https://www.vr.se/swecris) is a national database containing information supplied by participating public and private research funders about research funding in Sweden. It is managed by the Swedish Research Council on behalf of the Swedish Government and contains records from 2008 onwards. The service distinguishes the funding period from the period in which the project is carried out and follows the CERIF research information model as far as possible.

Each project record has a `Project-ID`, visible in SweCRIS and used by the [SweCRIS API](https://www.vr.se/swecris/swecris-api.html). In many records, the value combines an award or project number with a funder suffix. An example is [`2015-04611_VR`](https://www.vr.se/swecris?project=2015-04611_VR). The identifier supports retrieval and linking within the SweCRIS data environment and is valuable when exchanging or reconciling records from participating funders.

The SweCRIS Project-ID is not documented as a globally resolvable PID with an independent persistence policy. Its namespace and semantics are tied to SweCRIS and the identifiers received from participating funders. Coverage is also funding-centred: it includes projects and other supported activities reported by participating funders, but not all research activities performed in Sweden. SweCRIS records may represent several types of support besides project grants, such as career support, research environments, research infrastructures and international collaboration.

SweCRIS is nevertheless the main existing national aggregation point identified here for funded-project information. Its Project-IDs should be preserved as alternate identifiers when corresponding records are assigned a global project PID. A future RAiD implementation could use SweCRIS and funder identifiers as authoritative sources for funding relationships while allowing the RAiD to represent the research activity independently of a single award.


### Institutional and funder-specific project identifiers

🟢 Active

Swedish universities, research organisations and funders assign project numbers, award numbers, case numbers and internal database identifiers in grant-management systems, financial systems, CRIS systems and project registries. These identifiers are essential for local administration and may remain stable within the system that issued them.

Such identifiers normally have a limited namespace, are not globally resolvable and may identify different entities in different systems: an application, administrative case, financial account, contract, award or research project. The same project may consequently accumulate several local identifiers, while an award number is sometimes used as a proxy for the project itself.

Local identifiers should be retained and exposed as alternate identifiers where possible, together with the issuing organisation and identifier type. They are important for reconciliation and provenance, but should not be treated as substitutes for a globally unique project PID unless the issuing system provides documented persistence, resolution and metadata stewardship.


## Current Swedish landscape

No coordinated Swedish PID service dedicated specifically to research projects and research activities was identified at the time of this analysis. The present landscape relies mainly on funder and institutional identifiers, with SweCRIS providing national aggregation for projects and other activities supported by participating funders. CORDIS DOIs add a globally resolvable identifier for EU-funded projects, but their scope is limited to the corresponding EU grant agreements.

RAiD is the most purpose-specific international option and is designed to complement rather than replace grant identifiers, SweCRIS Project-IDs or local project numbers. A generic DataCite project DOI offers a technically simpler alternative but provides less project-specific governance and lifecycle functionality. Whichever model is used, the project PID should be linked to existing identifiers and to PIDs for contributors, organisations, funding and outputs.

Before coordinated Swedish adoption, the following issues require common definitions and governance:

* The minimum criteria for an entity to be considered a project or research activity
* The appropriate granularity for programmes, projects, subprojects, work packages and recurring activity phases
* The event that triggers PID registration and the organisation responsible for doing so
* Responsibility for metadata updates during the project and after closure
* Relationships between the project PID, SweCRIS Project-ID, funder award IDs, local project numbers and CORDIS DOIs
* Handling of duplicate records, project transfers, mergers, splits and title changes
* Minimum public metadata and procedures for sensitive or temporarily embargoed projects
* Sustainable national or European service provision, costs and technical integration with CRIS, funder and repository systems
=======
_Last updated: 2026-08-20_

Deciding on what makes up a research project may seem like a trivial issue, but this has proven to pose a considerable challenge in the modern digital research landscape. Difficulties arise when attempting to interlink research outputs, contributions and events as clusters of research activities. Historically, the creation of such connections has been relying on citations in reference lists, mentioning grants and acknowledging support from various actors, or creating manual descriptions of projects within publications or on websites. However, interlinking of related materials are now increasingly done using CRIS/RIMS systems and modern publication tools.

## _Project_, or _activity_?

Because of the various activity types encountered in research globally, it may be misleading to only consider **research projects** when working with identification and delimitation of research contexts. In many cases, the **project** concept is also strongly tied to specific [funding and grants](funding-grants.md), sometimes even in a manner that disqualifies activities without external funding.

For this reason, some initiatives have started using the **research activity** concept as a broader and more inclusive term. 

## Examples of research activities

There is a need for PIDs enabling unambiguous identification and clustering of a wide range of such research activities, including but not limited to:

* Research projects with external funding
* Research projects with no specific funding
* Research programmes with several related projects over time
* Independent work packages within large projects
* Related activities recurring over long periods of time, such as continuous seasonal archeological excavations of the same site
* Spontaneous collaborations between researchers resulting in data collection, analysis and publication of results
* Ongoing citizen science projects coordinated by researchers
* Research evaluation activities relating to specific projects, infrastructures, teams or research groups

## Making use of research activity clustering through PIDs 

The various outputs, individuals, organisations etc. related to a research activity may often be expressed with PIDs themselves. This means that identifying a research activity will also, in most cases, create a need to reference such PIDs to give a better picture of what the activity encompasses and produces. Moreover, creating explicit relations between a research activity and relevant PIDs will enable unambiguous machine readability of the context.

Systematic clustering of research activities using PIDs is quickly becoming a core mechanism of research metrics and monitoring. The concept of traversing interlinked PID metadata to gain understanding of how research and research outputs are related has been conceptually described in the concepts of _Scientific Knowledge Graphs_ or _PID Graphs_.

## International PIDs and identifiers

### RAiD

🟢 Active

[RAiD](../data-on-pids/raid.md) (Research Activity Identifier) is a PID for identifying research activities, such as research projects, programmes or collaborations. It contains [kernel metadata](../pid-concepts/kernel-metadata.md) based on the [RAiD Metadata Schema](https://metadata.raid.org/en/latest/), identifying core information about the research activity, such as the researchers involved, the organisations responsible for the research, and the publications and other outputs created within the activity. This relies heavily on referring to other PIDs within the kernel metadata, such as [ORCID](../data-on-pids/orcid.md), [DOI](../data-on-pids/doi.md) or [ROR ID](../data-on-pids/ror.md).
RAiD has been codified by the ISO standard ISO 23527:2022.

RAiD follows the standard Handle/DOI pattern, with a real world example of a research project RAiD being `10.26259/ff442000`. Using the global resolver, the full RAiD may be accessed at: <https://raid.org/10.26259/ff442000>  

From the kernel metadata of this RAiD, we can see that this is a research project with the title `Breathlessness Rapid Evaluation And THErapy (BREATHE)` conducted at the research organisation with the ROR ID <https://ror.org/02stey378>, which is _The University of Notre Dame Australia_. Furthermore, an individual has been designated as a _Principal or Chief Investigator_ (PI), with the ORCID <https://orcid.org/0000-0002-4582-7728>. 

From the relational metadata, it is clear that this project is derived from an earlier research activity performing process evaluation, in turn having its own RAiD (`10.26259/5ed6f934`). When the project starts publishing outputs, they may also be referenced from the kernel metadata using relations, f.e. to each new article or dataset DOI.

In this manner, RAiD acts as a core PID for providing interoperable and open research information. As soon a research organisation ensures workflow compatibility with the metadata schema, RAiDs may be integrated in the standard functions of local CRIS/RIMS systems. It may be then used as a basis for institutional as well as national research tracking and evaluation workflows.

RAiDs are created and managed through _RAiD Service Points_ that may be set up to serve specific communities, such as a discipline-specific research infrastructures, research institutes or universities. These Service Points are administered by regional _RAiD Registration Agencies_. At the moment, Registration Agencies are being created in the EU, UK and US, while the Oceanian region is already up and running.

RAiD was created by the [Australian Research Data Commons](https://ardc.edu.au/), a NPO formed through the National Collaborative Research Infrastructure Strategy (NCRIS). ARDC is currently developing the RAiD standard as well as acting as the global _RAiD Registration Authority_, registering and onboarding new _RAiD Registration Agencies_.


## Other related entities

### CERIF _Project_

🟢 Active

In the [CERIF](https://eurocris.org/services/main-features-cerif/) (Common European Research Information Format) metadata standard created for modeling research in CRIS/RIMS systems, the **Project**, or **cfProj**, entity corresponds to a research project or activity in the [CERIF data model](https://eurocris.github.io/CERIF-DataModel/released/Tables.html).

While not being a PID in itself, the structured and interoperable metadata created when working within CERIF compliant tools and systems will facilitate responsible reuse of research information and active implementation of research activity PIDs such as RAiD.

### OpenAIRE Graph _Project_

🟢 Active

The [OpenAIRE](https://explore.openaire.eu) infrastructure performs large-scale indexing of research outputs. It aims to enable analysis by implementing the _Scientific Knowledge Graphs_ paradigm through OpenAIRE Graph. 

As a part of the OpenAIRE data model, the **Project** entity is in theory encapsulating research projects and activities. A Project identified and indexed by OpenAIRE will receive an internal OpenAIRE Project identifier, such as: `fwf_________::0276f19f569783c6d1976ee3f09b408b`  

The corresponding OpenAIRE Graph entry will then be available at: <https://explore.openaire.eu/search/project?projectId=fwf_________::0276f19f569783c6d1976ee3f09b408b>

A review of [entities indexed to date](https://explore.openaire.eu/search/find/projects) will reveal a nearly exclusive focus on externally funded projects. This means that currently, the entity is in practice more closely related to the [funding and grants](funding-grants.md) concept.

However, in the [OpenAIRE Guidelines for CRIS Managers](https://openaire-guidelines-for-cris-managers.readthedocs.io/en/latest/), the infrastructure is supporting the CERIF _Project_ metadata model and entity, where metadata on funding is optional. Therefore, it appears that the OpenAIRE infrastructure has committed to support a more inclusive research activity concept for future development and indexing.
>>>>>>> 2f0d61bfda5a8d4541f425aecc2d66e263a05674
