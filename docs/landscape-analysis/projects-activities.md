# Research projects and research activities

_Last updated: 2026-08-26_

Deciding on what makes up a research project may seem like a trivial issue, but this has proven to pose a considerable challenge in the contemporary digital research landscape. Difficulties arise when attempting to interlink research outputs, contributions and events as clusters of research activities. Historically, the creation of such connections has been relying on citations in reference lists, mentioning grants and acknowledging support from various actors, or creating free-form descriptions of projects within publications or on websites. However, descriptions of research and interlinking of related materials are now increasingly done using CRIS/RIMS systems and modern publication tools. These have a greater potential of meeting the needs of sharing unambiguous open research information, presenting it for human readers while also distributing it in the form of machine-actionable metadata.

## _Project_, or _activity_?

Because of the various activity types encountered in research globally, it may be misleading to only consider **research projects** when working with identification and delimitation of research contexts. In many cases, the **project** concept is also strongly tied to specific [funding and grants](funding-grants.md), sometimes even in a manner that excludes or disqualifies activities without external funding.

For this reason, several initiatives have started using the **research activity** concept as a broader and more inclusive term. 

## Examples of research activities

Unambiguous identification and clustering is relevant for a wide range of such research activities, including but not limited to:

* Externally funded research projects
* Internally funded or unfunded research projects
* Research programmes with several related projects over time
* Independent subprojects, work packages and defined project phases
* Field campaigns, expeditions and cruises
* Related activities recurring over long periods of time, such as recurring field seasons for a specific archaeological site
* Long-running studies divided into separately managed activities or waves
* Distributed citizen science projects coordinated by researchers
* Spontaneous collaborations between researchers resulting in data collection, analysis and publication of results
* Overarching thematic tracks encapsulating the activities of research groups or the research focus of individual or collaborating researchers
* Research evaluation activities relating to specific projects, infrastructures, teams or research groups

## Needs for identifying and describing research activities

Identifying and describing projects and activities serves several core needs in the research ecosystem, such as:

* Defining clusters of interrelated open research information and research outputs
* Distinguishing projects with identical, similar or changing titles
* Linking researchers and contributors, organisations, grants, infrastructures, instruments and outputs to the activity
* Identifying materials used as inputs in the research activity, such as pre-existing data
* Preserving provenance and a history of changes throughout the activity lifecycle
* Expressing relationships between programmes, projects, subprojects and related activities
* Supporting discovery, administration, reporting, assessment and impact analysis
* Allowing project information to be exchanged between local and national CRIS systems, funder systems, repositories, aggregators, scientometric resources and other open research information infrastructures

A core need is also that this information should be available as machine-readable metadata.

## Enabling research activity clustering through PIDs 

The various outputs, individuals, organisations etc. related to a research activity may often be expressed with PIDs themselves. This means that identifying a research activity will also, in most cases, create a need to reference such PIDs to give a better picture of what the activity encompasses and produces. Moreover, creating explicit relations between a research activity and relevant PIDs will enable unambiguous machine readability of the context.

Systematic clustering of research activities using PIDs is quickly becoming a core mechanism of research metrics and monitoring. The concept of traversing interlinked PID metadata to gain understanding of how research and research outputs are related has been conceptually described in the concepts of _Scientific Knowledge Graphs_ or _PID Graphs_.

## International PIDs and identifiers

### RAiD

🟢 Active

[RAiD](../data-on-pids/raid.md) (Research Activity Identifier) is a PID for identifying research activities, such as research projects, programmes or collaborations. It is intended to identify a time-bounded research endeavour independently of any particular grant, output, institution or information system. 

RAiD contains [kernel metadata](../pid-concepts/kernel-metadata.md) based on the [RAiD Metadata Schema](https://metadata.raid.org/en/latest/), identifying core information about the research activity, such as the researchers involved, the organisations responsible for the research, and the publications and other outputs created within the activity. This relies heavily on referring to other PIDs within the kernel metadata, such as [ORCID](../data-on-pids/orcid.md), [DOI](../data-on-pids/doi.md) or [ROR ID](../data-on-pids/ror.md).
RAiD has been codified by the ISO standard [ISO 23527:2022](https://www.iso.org/standard/75931.html).

A real world example of a research project RAiD is `10.26259/ff442000`. Using the global resolver, the full RAiD may be accessed at: <https://raid.org/10.26259/ff442000>  

From the kernel metadata of this RAiD, we can see that this is a research project with the title `Breathlessness Rapid Evaluation And THErapy (BREATHE)` conducted at the research organisation with the ROR ID <https://ror.org/02stey378>, which is _The University of Notre Dame Australia_. Furthermore, an individual has been designated as a _Principal or Chief Investigator_ (PI), with the ORCID <https://orcid.org/0000-0002-4582-7728>. 

From the relational metadata, it is clear that this project is derived from an earlier research activity performing process evaluation, in turn having its own RAiD (`10.26259/5ed6f934`). When the project starts publishing outputs, they may also be referenced from the kernel metadata using relations, f.e. to each new article or dataset DOI.

In this manner, RAiD acts as a core PID for providing interoperable and open research information. As soon a research organisation ensures workflow compatibility with the metadata schema, RAiDs may be integrated in the standard functions of local CRIS/RIMS systems. It may be then used as a basis for institutional as well as national research tracking and evaluation workflows.

RAiD records are intended for project information that can ultimately be made public. [Temporary embargos](https://metadata.raid.org/en/latest/core/access.html) are supported, but confidential or security-sensitive project information should not be placed in the public registry.

RAiD makes use of the [DataCite DOI infrastructure](https://support.datacite.org/docs/raids), meaning that a RAiD is also a valid DOI and that a core subset of its kernel metadata is registered with DataCite. However, the full RAiD metadata record is maintained by the RAiD service itself. RAiD should therefore be understood as a specialised PID system built on and extending DOI infrastructure, and should not be confused with a regular DOI assigned to a project landing page.

RAiDs are created and managed through _RAiD Service Points_ that may be set up to serve specific communities, such as a discipline-specific research infrastructures, research institutes or universities. These Service Points are administered by regional _RAiD Registration Agencies_. At the moment, Registration Agencies are being created in the EU, UK and US, while the Oceanian region is already up and running.

RAiD was created by the [Australian Research Data Commons](https://ardc.edu.au/), a NPO formed through the National Collaborative Research Infrastructure Strategy (NCRIS). ARDC is currently developing the RAiD standard as well as acting as the global _RAiD Registration Authority_, registering and onboarding new _RAiD Registration Agencies_.

In Finland, the national CRIS system [Research.fi](https://research.fi/) has started employing RAiD for identification of research projects[@jrnl-PilotingUseRAiD-24]. It is also identified as a core infrastructural component for building the European Open Science Cloud (EOSC)[@web-ResearchActivityIdentifier-25].

### DataCite DOI

🟢 Active

A generic [DataCite DOI](../data-on-pids/doi.md) may be registered directly for a project. The DataCite Metadata Schema includes `Project` as a value for `resourceTypeGeneral`, defined for a planned endeavour or activity intended to achieve a particular aim using allocated resources. DataCite explicitly distinguishes the project itself from a project report, protocol, study registration or other output, which should be assigned the resource type appropriate to that object[@web-ProjectTrackingIdentification].

A project DOI can connect the project to contributors, organisations, funding and outputs through DataCite relationship metadata and the DataCite PID Graph. The DataCite metadata schema also recognises `RAiD` as a related identifier type, enabling explicit links between DataCite records and RAiDs.

A DataCite project DOI does not provide the same benefits as using RAiD. It can provide global resolution, kernel metadata and links to related entities, but it does not by itself provide the RAiD-specific metadata model, federated registry, authenticated multi-party editing or project change history.

## Swedish national identifiers

### Institutional identifiers

🟢 Active

Swedish universities and research organisations may assign project numbers or case numbers (_diarienummer_). These may be employed in financial systems, CRIS systems and CMS systems or serve as internal database identifiers. These identifiers are essential for local administration and may remain stable within the system that issued them. They are also commonly referenced in formal documentation and agreements between organisations.

Such identifiers normally have a limited namespace, are not globally resolvable and may identify different entities in different systems: an application, administrative case, financial account, contract, award or research project. The same project may consequently accumulate several local identifiers, while an award number created by a funder is sometimes used as a proxy for the project itself, possibly creating an overlap with [identifiers from grant-management systems](funding-grants.md).

When creating workflows for creating and maintaining globally resolvable research activity PIDs such as RAiD, local identifiers may be exposed as alternate identifiers when relevant, together with the issuing organisation and identifier type.

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


<!-- TODO: possible move to recommendations:
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
-->