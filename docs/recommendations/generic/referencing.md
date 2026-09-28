# Referencing entities with PIDs

_Last updated: 2026-09-28_

These recommendations concern how PIDs are used in references, how they are recorded in systems, and how they are linked to each other. PIDs may identify digital objects, such as publications and datasets, as well as phenomena represented by metadata, such as people, organisations and samples. The recommendations apply to everyone who uses PIDs, not only to the organisations that register them.

## Use the PID as the primary reference

_Applies to: all PID Users._

!!! quote ""

    When something has a PID, use the PID to refer to it in citations, links, metadata and system integrations, rather than a URL to its current location, a title string or a local identifier.

??? question "Why?"

    PIDs are designed to stay the same when a digital object moves or changes hosting service, or when a person or organisation changes name. URLs, titles and local identifiers change or break over time, while a reference made with the PID keeps working and is redirected to the current PID target. A PID also identifies what it refers to unambiguously, for people as well as for software.

    A PID does not, however, say anything about the quality of what it identifies. It shows that something can be persistently referenced, not that it has been reviewed, validated or is fit for any particular purpose.

??? info "How?"

    - Link to the PID in its actionable resolver form, for example `https://doi.org/10.12345/abc-xyz`, and not to the URL the resolver currently redirects to.
    - Display PIDs in full and as clickable links on web pages, landing pages and in reference lists.
    - Complement the PID with human-readable information such as a name, title or traditional reference style, but let the PID carry the reference.
    - Do not use the presence of a PID as an indicator of quality, for example in research assessment.

See also: [What is a PID?](../../pid-concepts/what-is-pid.md) · [Persistence](../../pid-concepts/persistence.md) · [Resolvability](../../pid-concepts/resolvability.md)

## Reuse existing PIDs before minting new ones

_Applies to: all PID Users and PID Managers._

!!! quote ""

    Before registering a new PID, check whether what you want to identify already has one, and reuse it. Assign new PIDs deliberately, to digital objects and phenomena that are expected to be referenced over time or across organisational boundaries.

??? question "Why?"

    Parallel PIDs for the same publication, dataset or organisation split citations, links and usage between identifiers, and make it harder for people and systems to see that they concern the same thing. The organisation responsible for what is identified is usually best placed to maintain its PID. Each registered PID also comes with a lasting commitment to maintain its target and metadata, so PIDs that nobody will reference add cost without adding value.

??? info "How?"

    - Reuse the PID assigned by the responsible organisation, such as the publisher of a publication, the repository holding a dataset or the funder of a grant, rather than minting a parallel identifier.
    - Assign PIDs as part of the workflow that produces or publishes the digital object, rather than as an afterthought.
    - When several PIDs legitimately exist for the same digital object or phenomenon, for example one from an international system and one from a national or disciplinary system, record all of them, state explicitly that they are equivalent, and define which one is preferred in your context.
    - Use kernel metadata to express that the duplicate PID identifies the same thing, with an explicit relation type such as **is identical to**.
    - Never present two equivalent PIDs as if they identified different things.

See also: [Uniqueness](../../pid-concepts/uniqueness.md)

## Use a PID designed for what is being identified

_Applies to: all PID Users and organisations selecting PID services._

!!! quote ""

    Identify objects and phenomena such as people, organisations, outputs, projects, grants, instruments and samples with separate PIDs, each from a PID system whose [scope](../../pid-concepts/usage-scope.md) covers what is being identified. Connect them in structured metadata rather than letting one identifier stand in for another.

??? question "Why?"

    People, organisations, outputs and activities have different lifecycles, metadata and relationships, and PID systems are designed around what is within their scope. Using one identifier as a substitute for another hides the real relationships between them. As an example, a grant identifier should not be used as the general identifier for a research project: a project may receive several grants, and one grant may support several projects.

??? info "How?"

    - Before assigning or recording a PID, decide exactly what is being identified: a digital object, such as a dataset or a publication, or a phenomenon represented by metadata, such as a person, an instrument or a research activity.
    - Choose a PID system whose scope covers it. The [landscape analysis](../../landscape-analysis/index.md) describes PID systems available for each scope, and the [scope-specific recommendations](../scope-specific/index.md) point out which ones are advantageous to use.
    - Keep identifiers for related but distinct things separate. For example:
        - a grant identifier is not a project identifier;
        - a dataset identifier is not an instrument identifier;
        - a user account name is not a person identifier.
    - Link them with explicit relation types (see [Express relationships between PIDs as links with explicit relation types](#express-relationships-between-pids-as-links-with-explicit-relation-types)).

See also: [Usage scope](../../pid-concepts/usage-scope.md) · [Coverage](../../pid-concepts/coverage.md) · [Landscape analysis](../../landscape-analysis/index.md)

## Record PIDs in a normalised, typed and validated form

_Applies to: all PID Users and PID Managers._

!!! quote ""

    Store PIDs so that both people and software can interpret them without guessing: typed with their PID scheme, normalised according to the rules of that scheme, validated against the authoritative registry, and specified with a resolver when possible.

??? question "Why?"

    A bare string such as `0000-0002-1825-0097` or `10.12345/abc` is ambiguous outside the system that recorded it: it is not obvious which PID system it belongs to, how it is resolved or whether it is valid. PIDs entered as free text often contain errors, and a single wrong character may make a PID resolve to something else or not at all. Some PID systems are case sensitive and others are not, so changing the case or characters of a PID can break it.

??? info "How?"

    - Store the PID scheme or type together with the identifier value and its canonical resolver URL.
    - Normalise values according to the rules of each PID system; see [Data on PIDs](../../data-on-pids/index.md) for each system's rules. Do not change the case or characters of a PID from a case-sensitive system.
    - Validate PIDs against the authoritative registry when they are entered. Prefer registry lookups, APIs and authenticated workflows over free-text entry.
    - Keep local, legacy and former identifiers, and record how they relate to the preferred PID.
    - Do not describe an identifier as persistent or globally resolvable if it is not.

See also: [Interpretability](../../pid-concepts/interpretability.md) · [Data on PIDs](../../data-on-pids/index.md)

## Express relationships between PIDs as links with explicit relation types

_Applies to: all PID Users and PID Managers._

!!! quote ""

    Record relationships between entities as links with explicit relation types between their PIDs, and include the PIDs of related entities in all metadata you create.

??? question "Why?"

    PIDs deliver most of their value when they are connected. Linking PIDs with explicit relation types makes it possible to follow a researcher to their outputs, an output to its funding, or a dataset to the instrument that produced it, without manually matching names and titles. Together, such links form a graph of research information that can be reused for discovery, attribution, reporting and follow-up across organisations.

??? info "How?"

    - Use the dedicated relation types of the metadata schema in use, for example:
        - a person **is creator of** an output;
        - an organisation **is affiliation of** a person;
        - a grant **funds** a project;
        - a project **produced** an output;
        - an output **is version of**, **is part of**, **is derived from** or **cites** another output;
        - an output **was produced using** an instrument or a sample.
    - Include PIDs for related entities in the metadata, not only the PID of what is being described: contributors, affiliations, funders, grants, projects, related outputs and licences.
    - Use a resolvable licence URI or a recognised licence identifier.

See also: [Kernel metadata](../../pid-concepts/kernel-metadata.md) · [Landscape analysis](../../landscape-analysis/index.md)