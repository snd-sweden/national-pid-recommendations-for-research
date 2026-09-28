# Assigning and maintaining PIDs

_Last updated: 2026-09-28_

These recommendations concern how PID Managers design, register and maintain PIDs throughout the lifecycle of what they identify.

## Keep PID strings opaque and free from meaning

_Applies to: PID Managers._

!!! quote ""

    Do not encode information that may change in the PID string, such as organisation or department names, titles, subject areas, dates or storage locations. Use generated, opaque strings for the local part of the PID and describe what is identified in metadata instead.

??? question "Why?"

    Organisations merge and are renamed, individuals change names, and digital objects move between collections and services, while a PID must remain unchanged. A PID that carries such information therefore sooner or later becomes misleading. Information in metadata can be corrected and updated; information in the PID string cannot.

??? info "How?"

    - Use a limited, unambiguous character set and one consistent case, also in systems that are case insensitive.
    - Create separate prefixes or namespaces only for lasting operational reasons, not to mirror organisational structure.
    - Keep PIDs reasonably short when they are likely to be read, typed or cited by people, while allowing for future growth in numbers.

See also: [Interpretability](../../pid-concepts/interpretability.md)

## Let PIDs resolve to informative landing pages

_Applies to: PID Managers._

!!! quote ""

    Let each PID resolve to a landing page describing what it identifies, rather than directly to a file download, and make the information on the landing page available in machine-readable form as well.

??? question "Why?"

    A landing page tells the person or software following the PID what has been identified, how it relates to other entities, under which conditions it may be used and how it can be accessed, before anything is downloaded. It also provides a stable place for this information when a digital object consists of several files, is restricted or has been withdrawn. Machine-readable metadata on the landing page makes it interpretable by search engines, aggregators and other services worldwide.

??? info "How?"

    - Include at least:
        - a description of what is identified, for example bibliographic information;
        - the PID itself, clearly displayed;
        - access to the digital object, or information on how access can be requested;
        - the licence and relationships to other entities, using their PIDs.
    - Embed the same information as machine-readable metadata, for example using [Schema.org](https://schema.org/).
    - Where possible, use content negotiation to offer alternative representations of the digital object and its metadata, and signposting in HTTP headers to point machines to them.
    - For phenomena that have no digital form of their own, such as physical objects and concepts, the landing page and its metadata are their digital representation. Make them complete enough to distinguish each phenomenon from similar ones.

See also: [Landing pages](../../pid-concepts/landing-pages.md) · [Interpretability](../../pid-concepts/interpretability.md)

## Ensure metadata quality with standards, vocabularies and validation

_Applies to: PID Managers._

!!! quote ""

    Describe what each PID identifies with metadata that follows recognised metadata standards, is validated before it is registered, and uses controlled vocabularies and authority data where they exist.

??? question "Why?"

    The value of a PID depends on the quality of its metadata. Completeness, consistency and machine-readability determine whether what is identified can be found, attributed, reused and followed up. Free-text values for resource types, subjects, affiliations and contributor roles are ambiguous for software, and lead to isolated metadata that cannot be compared with other entries or combined across systems.

    Controlled vocabularies and authority data give values that people, research information systems and AI-based services can interpret in the same way. Validation catches errors before they are registered and spread to the services that harvest PID metadata, where they are much harder to correct.

??? info "How?"

    - Follow the metadata schema of the PID system, and use community or disciplinary extensions where the schema is not detailed enough.
    - Use controlled vocabularies for resource types, subjects, contributor roles and relation types, and PIDs or authority data for people, organisations, places and concepts, such as ORCID iDs, ROR IDs and authority files.
    - Validate metadata automatically before registration, against the schema and against agreed minimum requirements (see [Agree on national minimum requirements for PID metadata](../national/priorities.md#agree-on-national-minimum-requirements-for-pid-metadata)).
    - Correct errors in the source system and update the PID metadata from there, rather than correcting only the registered copy.

See also: [Kernel metadata](../../pid-concepts/kernel-metadata.md) · [Interpretability](../../pid-concepts/interpretability.md)

## Define rules for granularity and versions

_Applies to: PID Managers._

!!! quote ""

    Decide and document at which level digital objects are assigned PIDs, and how changes to what is identified are handled.

??? question "Why?"

    Without explicit rules, similar digital objects are identified at different levels in different cases, and users cannot know whether a PID refers to a collection, an item or a file, or to fixed or changing content. For citation and reproducibility, it must be clear exactly which content a PID refers to. At the same time, some phenomena, such as organisations or instruments, change over time while remaining the same.

??? info "How?"

    - Decide whether PIDs are assigned to collections, individual items or files, whether different formats of the same content share a PID, and what counts as a new version.
    - Assign a new PID when content changes in a way that matters for citation or reproducibility. Do not change the content behind an existing PID for digital objects that are expected to be stable, such as published datasets supporting research results.
    - Link each version to its preceding and following versions, and group versions of the same logical object under a concept PID (see [Use concept PIDs to group versions and collections](#use-concept-pids-to-group-versions-and-collections)).
    - Link parts and wholes explicitly, for example files to datasets or chapters to books.
    - For phenomena that change over time while remaining the same, such as an organisation or an instrument, keep the PID and record significant changes in metadata.
    - Document the rules in your PID policy (see [Adopt a PID policy with clear responsibilities](organisation.md#adopt-a-pid-policy-with-clear-responsibilities)).

See also: [Concept PIDs](../../pid-concepts/concept-pids.md) · [Uniqueness](../../pid-concepts/uniqueness.md)

## Use concept PIDs to group versions and collections

_Applies to: all PID Users and PID Managers._

!!! quote ""

    Use a [concept PID](../../pid-concepts/concept-pids.md) to group PIDs that belong together, whether they identify versions of the same logical object or a collection of different objects. The concept PID identifies the group as a whole, while each version or member keeps its own PID.

??? question "Why?"

    People often need to refer both to a logical object as a concept and to one exact version of it. A software package, a regularly updated dataset or a report issued in several editions may be cited for its content in general, or for the specific version used in an analysis. A concept PID gives a stable reference to the whole that always leads to the current version, while the version PIDs keep references to specific content exact. Without a concept PID, references to the object as a whole are spread over individual versions, and often point to outdated ones.

    Collections of different objects, such as a series of reports, the outputs of a project or a set of samples, may likewise need to be referenced as one unit without losing the identity of each member.

    A concept PID is itself a unique PID: it identifies the grouping, not any single member of it. It is most useful when it exists from the start, since references that have already been made to a single version cannot later be turned into references to the whole.

??? info "How?"

    - For objects that may get new versions, such as software and evolving datasets, assign a concept PID together with the first version, even if only one version exists so far.
    - Give every version or member its own PID, and do not use the concept PID in their place.
    - Link the concept PID and each version or member with explicit relations in both directions, such as **has version** and **is version of** for versions, or **has part** and **is part of** for collections. Record the relations in kernel metadata where the PID system provides it, and otherwise on the landing pages (see [Prefer PID systems with kernel metadata](choosing.md#prefer-pid-systems-with-kernel-metadata)).
    - Let the concept PID resolve to a landing page with an overview of all versions or members and their PIDs. For versions, this may be the landing page of the latest version, provided that it lists all versions.
    - Make clear in the metadata and on the landing page whether the concept PID groups versions of one logical object or a collection of different objects.
    - When the members of a collection change, update the metadata and landing page of the concept PID accordingly.
    - Cite the version PID when referring to specific content, such as the data or code used in an analysis, and the concept PID when referring to the object as a whole.
    - Document when concept PIDs are assigned and what they group in your PID policy (see [Adopt a PID policy with clear responsibilities](organisation.md#adopt-a-pid-policy-with-clear-responsibilities)).

See also: [Concept PIDs](../../pid-concepts/concept-pids.md) · [Uniqueness](../../pid-concepts/uniqueness.md) · [Interpretability](../../pid-concepts/interpretability.md) · [Landing pages](../../pid-concepts/landing-pages.md)

## Maintain targets and metadata throughout the lifecycle

_Applies to: PID Managers._

!!! quote ""

    Update target URLs whenever digital objects or their descriptions move, and keep metadata correct and complete for as long as the PID exists.

??? question "Why?"

    Persistence depends on active maintenance. A PID system only redirects to the target URL it has been given; if the target moves and the PID is not updated, the PID breaks just like an ordinary link. This typically happens when the system hosting the targets is migrated, replaced or decommissioned. An independent record of registered PIDs makes it possible to verify them and, if needed, to move them to another provider. Errors in PIDs and metadata also affect everyone who relies on them, not only the organisation that registered them.

??? info "How?"

    - Include PID target updates in every plan for migrating, replacing or decommissioning a system that hosts PID targets.
    - Regularly check that your PIDs resolve to the intended targets, and correct broken resolution promptly.
    - Keep your own complete record of every PID you have registered, with its target and metadata, independently of the PID provider.
    - Report errors in other actors' PIDs and metadata to the responsible PID Manager or provider when you find them.

See also: [Persistence](../../pid-concepts/persistence.md) · [PID ecosystem](../../pid-concepts/pid-ecosystem.md#manager)

## Never delete or reassign a PID, and provide tombstone pages

_Applies to: PID Managers._

!!! quote ""

    Never reuse a PID to identify something else, and never delete a registered PID. When a digital object is withdrawn, removed or no longer available, or a phenomenon ceases to exist, let its PID resolve to a tombstone page.

??? question "Why?"

    Once registered, a PID may be cited in publications, recorded in other organisations' systems and linked from metadata all over the world. If it is deleted, those references break; if it is reused, they silently point to something else. Both undermine the trust that makes PIDs useful. A [tombstone page](../../pid-concepts/tombstone-pages.md) keeps references working after what it identified is gone, and lets people and software understand what has happened to it.

    In Sweden, records related to research held by government agencies are generally official documents and are covered by archival legislation, which requires them to be kept in order. PIDs should be maintained after the records have been transferred to an archive, and tombstone pages should be maintained after possible disposal of the records.

??? info "How?"

    - On the tombstone page, state what was identified, when and why it was removed, who made the decision and whether something else replaces it.
    - Provide the same information in machine-readable form, and update the kernel metadata where the PID system has it.
    - Coordinate PID maintenance with records management and archiving, so that PIDs keep resolving to the records, or to tombstone information about them, when records are transferred to an archive or disposed of.

See also: [Tombstone pages](../../pid-concepts/tombstone-pages.md) · [Persistence](../../pid-concepts/persistence.md) · [Uniqueness](../../pid-concepts/uniqueness.md)