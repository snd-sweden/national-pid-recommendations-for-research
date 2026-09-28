# Shared priorities and requirements

_Last updated: 2026-09-28_

These recommendations concern shared national priorities for PID systems, minimum metadata requirements, common PID requirements from research funders and in publisher agreements, and harmonised reporting of research outputs.

## Agree on national priorities and address gaps jointly

_Applies to: national actors._

!!! quote ""

    Agree nationally on which PID systems to prioritise for each scope, such as people, organisations, publications, research data and research activities, and address gaps in the PID landscape jointly rather than through parallel local solutions.

??? question "Why?"

    When organisations choose PID systems independently, the same kind of output, actor or activity may be identified in incompatible ways across the sector, and each organisation carries the cost of evaluating and implementing new systems on its own. For some scopes, PID practices are still emerging. Shared priorities make it easier for organisations, funders and system vendors to invest in the same solutions, and national follow-up shows where coordination works and where support is needed.

??? info "How?"

    - Use the [landscape analysis](../../landscape-analysis/index.md) to identify scopes that lack suitable PIDs or consistent practices in Sweden.
    - Discuss the adoption of emerging PID systems at the national level before they are introduced locally, and coordinate pilots.
    - Agree on common criteria for selecting PID systems and services, building on the criteria in the [generic recommendations](../generic/choosing.md#assess-pid-systems-and-providers-against-explicit-criteria).
    - Align national registries and research information systems, such as national publication and grant indexes, with the prioritised PID systems and with international metadata standards (see [Harmonise research output reporting workflows around PIDs](#harmonise-research-output-reporting-workflows-around-pids)).
    - Follow up PID adoption nationally with shared indicators, building on those that organisations use to monitor their own PID work.

See also: [Landscape analysis](../../landscape-analysis/index.md)

## Agree on national minimum requirements for PID metadata

_Applies to: national actors and research organisations._

!!! quote ""

    Agree nationally on minimum requirements for the metadata of research outputs registered with PIDs, such as affiliations, contributor identifiers, relations, citations and access statements, and support them with shared terminology and validation.

??? question "Why?"

    The technical prerequisites for traceable research outputs are in place in Sweden, but they are still used inconsistently. When each repository, organisation or individual decides on its own what to register, outputs cannot be reliably found, attributed or followed up across the sector.

    Shared minimum requirements, with common terminology and standardised relation types, make metadata comparable across services, and validation makes the requirements easy to meet. Requirements are most likely to be met when the infrastructure, guidance and incentives to meet them are already in place.

??? info "How?"

    - Define the minimum information to include when citing research outputs, and in statements about access restrictions.
    - Define minimum requirements for affiliation metadata, including ROR IDs, and for identifying contributors with ORCID iDs.
    - Define minimum metadata for outputs registered in designated repositories and publication services, including relations to publications, data, software and research activities.
    - Harmonise terminology and relation types, building on the metadata schemas of the PID systems in use (see [Express relationships between PIDs as links with explicit relation types](../generic/referencing.md#express-relationships-between-pids-as-links-with-explicit-relation-types)).
    - Provide validation tools and checklists, so that repositories and researchers can check metadata before registration.

See also: [Research data](../../landscape-analysis/research-data.md)

## Align PID requirements across research funders and policy makers

_Applies to: research funders, organisations negotiating agreements with publishers, and other national actors._

!!! quote ""

    Agree on common requirements for PIDs in funding applications, reporting and national research information, and apply them consistently across funders, policy makers and national services.

??? question "Why?"

    Funder requirements are an important driver of PID adoption, but differing requirements from different funders and services add to the burden on researchers and organisations.

    Consistent requirements based on the same PID systems and metadata standards allow organisations to build one set of workflows, and make it possible to reuse information across applications, reports and national follow-up instead of entering it again.

    Agreements with publishers are a similar lever: publishers are a main source of metadata about publications, and national agreements with them can require that this metadata is open and complete.

??? info "How?"

    - Agree on which PIDs to request for people, organisations, grants and outputs in applications and reporting, in line with the national priorities (see [Agree on national priorities and address gaps jointly](#agree-on-national-priorities-and-address-gaps-jointly)).
    - Let applicants and organisations provide information by PID, and retrieve the associated metadata from PID registries instead of asking for it to be entered again.
    - Make funding information available with PIDs and machine-readable metadata, building on shared Swedish standards for grant metadata; see [Funding and grants](../../landscape-analysis/funding-grants.md).
    - Ask grant holders to acknowledge funding with a standardised statement that includes the funder's name and the grant PID, and coordinate the wording with other funders.
    - Include requirements for open, PID-rich metadata, such as ORCID iDs, ROR IDs, grant PIDs and open reference lists, in national licence negotiations and agreements with publishers.
    - Announce new requirements well in advance and coordinate them with other policy makers, funders and research organisations, so that research organisations and system vendors can prepare.

See also: [Funding and grants](../../landscape-analysis/funding-grants.md)

## Harmonise research output reporting workflows around PIDs

_Applies to: national actors and research organisations._

!!! quote ""

    Harmonise the workflows for reporting research outputs locally and nationally, with PIDs as a core tool for identifying and linking outputs, people, organisations, projects and grants. Align local current research information systems (CRIS systems) and project indexes with international standards, and work towards a unified national PID-driven CRIS system that supplements existing national services.

??? question "Why?"

    Information about research outputs is often reported several times: in local research information systems, to funders, to national indexes and for evaluations, each with its own formats and requirements. This adds to the burden on researchers and support staff, and makes information from different sources hard to combine. When outputs and the people, organisations, projects and grants connected to them are identified with PIDs, the same information can be reported once, matched reliably across systems and reused wherever it is needed.

    International research information standards make this possible without separate national solutions. Local systems aligned with these standards can exchange information with each other and with European and international infrastructures.

    At the Swedish national level, indexing services exist for research publications and research data. Comprehensive national aggregation would require a research information model in which several other entities are also indexed with PIDs of their own in a national PID-driven CRIS system.

??? info "How?"

    - Use PIDs as the primary keys when research outputs are reported, and include the PIDs of related people, organisations, projects and grants, so that information can be matched and reused across local, national and international systems.
    - Align local CRIS systems and project indexes with international standards, such as the [CERIF](https://eurocris.org/services/main-features-cerif/) data model, the OpenAIRE Guidelines, for example the [OpenAIRE Guidelines for CRIS Managers](https://openaire-guidelines-for-cris-managers.readthedocs.io/en/latest/), and the metadata schema of [RAiD](../../data-on-pids/raid.md) for research projects and activities and all entities they relate to.
    - Agree on a common national application profile for exchanging research information, based on these standards, so that local systems can deliver the same data to national and international services.
    - Record relations between outputs, people, organisations and research activities when outputs are registered, rather than trying to reconstruct them afterwards.
    - Work towards a national PID-driven CRIS system that:
        - identifies outputs, people, organisations, projects, grants and research infrastructures with established PIDs, rather than with identifiers of its own;
        - records the relationships between these entities as links with explicit relation types between their PIDs;
        - retrieves metadata from local systems and PID registries instead of collecting the same information again;
        - makes its data openly available through APIs, and exchanges data with European aggregators such as OpenAIRE.

See also: [Research projects and research activities](../../landscape-analysis/projects-activities.md) · [Publications](../../landscape-analysis/publications.md) · [Funding and grants](../../landscape-analysis/funding-grants.md) · [RAiD](../../data-on-pids/raid.md) · [Research data](../../landscape-analysis/research-data.md)