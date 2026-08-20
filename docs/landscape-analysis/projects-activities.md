# Research projects and research activities

_Last updated: 2026-08-20_

Deciding on what makes up a research project may seem like a trivial issue, but this has proven to pose a considerable challenge in the modern digital research landscape. Difficulties arise when attempting to interlink research outputs, contributions and events as clusters of research activities. Historically, the creation of such connections has been relying on citations in reference lists, mentioning grants and acknowledging support from various actors, or creating manual descriptions of projects within publications or on websites. However, interlinking of related materials are now increasingly done using CRIS/RIMS systems and modern publication tools.

## _Project_, or _activity_?

Because of the various activity types encountered in research globally, it may be misleading to only consider **research projects** when working with identification and delimitation of research contexts. In many cases, the **project** concept is also strongly tied to specific [funding and grants](funding.md), sometimes even in a manner that disqualifies activities without external funding.

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

A review of [entities indexed to date](https://explore.openaire.eu/search/find/projects) will reveal a nearly exclusive focus on externally funded projects. This means that currently, the entity is in practice more closely related to the [funding and grants](funding.md) concept.

However, in the [OpenAIRE Guidelines for CRIS Managers](https://openaire-guidelines-for-cris-managers.readthedocs.io/en/latest/), the infrastructure is supporting the CERIF _Project_ metadata model and entity, where metadata on funding is optional. Therefore, it appears that the OpenAIRE infrastructure has committed to support a more inclusive research activity concept for future development and indexing.