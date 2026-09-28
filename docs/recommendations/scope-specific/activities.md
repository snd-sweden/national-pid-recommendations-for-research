# Research activities, funding and grants

_Last updated: 2026-09-28_

These recommendations concern the identification of research projects and other research activities, and of the funding and grants that support them. Research activities are the primary way of clustering the people, organisations, resources and outputs involved in research. Funding and grants are linked to the activities they support. Funders as organisations are covered in [Organisations, funders and research infrastructures](organisations.md). For the scope of the scope-specific recommendations and how PID systems are preferred, see [Scope-specific recommendations](index.md).

## Identify research projects and activities with RAiD

_Applies to: research organisations, research infrastructures and funders._

!!! quote ""

    Identify research projects and other research activities with RAiD, and use each RAiD as the central node that links the activity to its participants, organisations, funding, resources, outputs and related activities. Identify activities separately from the grants that fund them.

??? question "Why?"

    Research is organised in activities: projects, programmes, field campaigns, long-running studies and collaborations, whether externally funded or not. The activity is where people, organisations, funding, instruments, data and publications come together, and identifying it makes it possible to cluster all of them. A project is not the same thing as a grant: a project may be funded by several grants, or by none, and one grant may support several projects.

    RAiD is a PID system designed for this role, standardised as ISO 23527. Its kernel metadata consists largely of references to other PIDs: ORCID iDs for participants and their roles, ROR IDs for organisations, grant PIDs for funding and DOIs for outputs, as well as relations to parent, child and related activities.

    Because it connects to all other kinds of PIDs, RAiD is likely to become the central node for research activities in PID-driven metadata, from which the contributions, funding and outputs of an activity can be followed over time.

??? info "How?"

    - Declare interest in the RAiD service, and create a roadmap for implementing it in your organisational workflows.
    - While RAiD is not yet available, a DataCite DOI with the resource type Project may be used.
    - Register the RAiD when the activity starts, and keep it up to date as participants, funding, resources and outputs are added, so that it serves as the reference point throughout the activity.
    - Identify participants with ORCID iDs and organisations with ROR IDs from the start. Experience shows that organisation PIDs can often be added afterwards, while identifiers for people usually cannot.
    - Link each RAiD to grant PIDs of its funding where available, and record native funder grant IDs as alternate identifiers.
    - Keep confidential project information out of the public registry, and use embargoes where the registry supports them.
    - Integrate RAiD in research information systems and reporting workflows (see [Harmonise research output reporting workflows around PIDs](../national/priorities.md#harmonise-research-output-reporting-workflows-around-pids)).

See also: [Research projects and research activities](../../landscape-analysis/projects-activities.md) · [RAiD](../../data-on-pids/raid.md)

## Relate outputs and resources to their research activities

_Applies to: researchers, research organisations, repositories and publishers._

!!! quote ""

    Refer to the RAiD of the research activity in the metadata of the outputs, data, software, instruments, reused inputs and other resources produced or used in the activity, and add their PIDs to the RAiD metadata.

??? question "Why?"

    A central node is only useful if the links to it are recorded. When outputs refer to their research activity, and the activity refers to its outputs, the activity can be followed in both directions: funders and organisations can see everything an activity has produced, and someone who finds a dataset can also find the publications, software and instruments from the same activity. Reused materials may also be recorded. Reporting can then draw on the activity as a whole, instead of collecting information about each entity separately.

??? info "How?"

    - Record the RAiD as a related identifier in the DataCite metadata of data, software, instruments and other outputs of the activity.
    - Add the PIDs of outputs, instruments and other resources to the RAiD metadata as they are produced or taken into use.
    - Where an output belongs to several activities, relate it to each of them.
    - Link RAiDs to the records of the same activities in research information systems, and use them when reporting outputs.

See also: [Research projects and research activities](../../landscape-analysis/projects-activities.md) · [RAiD](../../data-on-pids/raid.md) · [DOI](../../data-on-pids/doi.md)

## Register grants with PIDs and open metadata

_Applies to: research funders._

!!! quote ""

    Register each awarded grant with a globally unique, resolvable PID with a landing page and open, machine-readable metadata, such as a DataCite DOI or a Crossref Grant ID for an award, and identify the funder in that metadata with its ROR ID.

??? question "Why?"

    Grants show how research is funded rather than how it is organised, and they should be linked to the research activities they support. Information about funding is much requested but fragmented. Grants are often identified by internal grant numbers, project titles or the names of the researchers awarded, which are ambiguous outside the funder's own systems and may collide with other funders' numbers.

    A grant PID with kernel metadata makes funding information machine-readable: the funder, the programme, the lead organisation, the principal investigator, dates and amounts can all be expressed with PIDs and structured values. When research activities, outputs and researchers' ORCID records refer to the grant PID, funding becomes directly linked to its results in the PID graph.

??? info "How?"

    - Register grant PIDs through DataCite DOIs for awards or Crossref's Grant Linking System, directly or through a consortium.
    - Include in the metadata at least the funder's ROR ID, the programme or call, the lead organisation's ROR ID, the principal investigator's ORCID iD, dates and, where public, the amount awarded.
    - Record the internal grant number, such as the diarienummer, as an alternate identifier in the grant metadata.
    - Keep grant metadata up to date during the grant. Relate the grant to the RAiDs of the activities it funds, where known, rather than using the grant PID as the identifier of a project.
    - Make acknowledgement of funding, including the grant PID, a condition of the grant, and give grant holders a standardised funding statement to use.
    - Expose grant PIDs in Swedish grant indexes and funders' APIs alongside existing grant numbers (see [Align PID requirements across research funders and policy makers](../national/priorities.md#align-pid-requirements-across-research-funders-and-policy-makers)).

See also: [Funding and grants](../../landscape-analysis/funding-grants.md) · [DOI](../../data-on-pids/doi.md)

## Reference funding with funder and grant PIDs

_Applies to: researchers, research organisations, publishers and repositories._

!!! quote ""

    Identify funding in the metadata of research activities, outputs and research information systems with the funder's ROR ID and the exact identifier that the funder assigned to the grant. Reuse grant PIDs where they exist rather than creating new identifiers.

??? question "Why?"

    Funding metadata allows tracking of the grants that make research possible, alongside the clustering by research activity. Funding acknowledgements in the text of publications are hard to process and often ambiguous. Structured funding metadata with PIDs lets funders, research organisations and aggregators follow what each grant has led to, without manual interpretation. Reusing the funder's own identifier avoids competing identifiers for the same grant.

??? info "How?"

    - Include the funder's ROR ID and the grant PID in RAiD metadata, in the funding metadata of DOIs for publications, data and software, and in research information systems.
    - For grants from the EU framework programmes, use the grant DOI and keep the grant agreement number.
    - When a grant has no PID, record the funder's grant number exactly as issued together with the funder's ROR ID. Do not present it as a resolvable PID.
    - Mention grant PIDs in the funding statements of publications in addition to the structured metadata.
    - Where possible, state which authors benefited from which grant.
    - When research had no external funding, state this explicitly, so that missing funding information is not ambiguous.

See also: [Funding and grants](../../landscape-analysis/funding-grants.md) · [Organisations](../../landscape-analysis/organisations.md)