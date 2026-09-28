# Organisations, funders and research infrastructures

_Last updated: 2026-09-28_

These recommendations concern the identification of organisations in the research sector, including research funders in their role as organisations and research infrastructures. The identification of individual grants is covered in [Research activities, funding and grants](activities.md). For the scope of the scope-specific recommendations and how PID systems are preferred, see [Scope-specific recommendations](index.md).

## Use ROR IDs for research organisations and funders

_Applies to: research organisations, funders, publishers, repositories and research information systems._

!!! quote ""

    Use ROR IDs as the primary PIDs for universities, research institutes, funders, research infrastructures and other organisations in the research sector. Review your organisation's ROR record and request additions and corrections when needed.

??? question "Why?"

    Affiliations and funding sources are used in reporting, research assessment and scientometric analyses. Organisation names are often ambiguous: they are translated, abbreviated and changed over time, and smaller funders may lack established names in other languages.

    ROR is the organisation identifier supported in Crossref, DataCite, ORCID and RAiD metadata. A ROR record holds names in several languages, organisation types, location, relationships to parent, child, related, predecessor and successor organisations, and links to other identifiers for the same organisation. The registry is openly available through an API and as data dumps, and it is curated through an open, community-based process in which anyone can suggest changes that are then reviewed by curators.

    ROR has superseded GRID, and Crossref is phasing out its Funder Registry in favour of ROR. The same ROR ID can therefore identify an organisation both as an affiliation and as a funder.

??? info "How?"

    - Store and exchange ROR IDs in their canonical resolver form, for example `https://ror.org/03zttf063`.
    - Use ROR IDs in affiliation, publisher, repository, project and funding metadata.
    - Identify a funder with its ROR ID, separately from the identifiers of individual grants.
    - Map existing Crossref Funder IDs and GRID IDs in local systems to ROR IDs.
    - Review your organisation's ROR record regularly, including names in Swedish and English, relationships to parent organisations and facilities, and links to other identifiers. Submit changes through the ROR curation process.
    - Record the Swedish organisation number as a secondary, legal identifier alongside the ROR ID, and use it as a fallback only for organisations that are not in scope for ROR.

See also: [Organisations](../../landscape-analysis/organisations.md) · [Funding and grants](../../landscape-analysis/funding-grants.md) · [ROR ID](../../data-on-pids/ror.md)

## Identify research infrastructures at the right level

_Applies to: research infrastructures, their host organisations and repositories._

!!! quote ""

    Define exactly what is being identified before assigning a PID, such as the infrastructure as an organisation, a facility, a core facility or a digital research infrastructure, and use the PID system whose scope matches each of them: ROR IDs for infrastructures that act as organisations or facilities, RRIDs for core facilities cited as research resources, and re3data and FAIRsharing records for data repositories and databases.

??? question "Why?"

    The same infrastructure name may refer to a legal organisation, a distributed consortium, a national node, a core facility or a digital research infrastructure. Identifying them with one PID merges things that should be kept apart, and makes attribution, impact tracking and long-term curation unreliable. A research infrastructure may therefore need a small graph of linked PIDs rather than a single PID.

    The registries for these different parts of an infrastructure offer metadata that makes infrastructures part of the wider research graph. ROR includes a facility type and relationships to host organisations. re3data describes repositories, including their certificates, licences, access conditions and use of PIDs, as openly licensed metadata. FAIRsharing interlinks databases with the standards and policies they implement, and lets organisations become verified maintainers of their records.

??? info "How?"

    - Use a ROR ID when the infrastructure appears as an affiliation, operator, publisher or funder, and express its relationships to its host organisation and to any distributed infrastructure it is part of.
    - Do not request ROR IDs for every internal service or core facility. Use an [RRID](resources.md#use-rrids-for-research-resources-where-they-are-established-practice) for core facilities that are cited in methods sections and acknowledgements, where this is established practice.
    - Register data repositories in re3data and databases in FAIRsharing, and keep the records up to date as their maintainer.
    - For distributed infrastructures, identify the consortium, national nodes, host organisations and services separately, and state the type of each relationship, such as hosting, operation, membership or funding.
    - In data catalogues following DCAT-AP-SE, the Swedish organisation number identifies the publishing organisation, not the infrastructure itself. Use it for that purpose alongside the infrastructure's own PIDs.

See also: [Research infrastructures](../../landscape-analysis/research-infrastructures.md) · [ROR ID](../../data-on-pids/ror.md) · [RRID](../../data-on-pids/rrid.md) · [FAIRsharing](../../data-on-pids/fairsharing.md)

## Keep other organisational identifiers as linked cross-references

_Applies to: research organisations, libraries and research information systems._

!!! quote ""

    Record other identifiers for organisations, such as the Swedish organisation number, ISNI, Libris authority identifiers and Wikidata identifiers, as cross-references linked to the ROR ID, and map legacy identifiers to ROR IDs.

??? question "Why?"

    Different contexts rely on different identifiers. Legal and administrative processes use the Swedish organisation number, while library systems use ISNI, VIAF and Libris authority identifiers, which may also describe subdivisions and historical names. Wikidata, maintained through collective curation, brings many identifiers for the same organisation together and connects research information to other knowledge graphs. Older metadata may contain identifiers that are no longer maintained, such as GRID IDs, or proprietary identifiers such as Ringgold IDs.

??? info "How?"

    - Store the Swedish organisation number alongside the ROR ID in research information systems, but do not present it as a research PID.
    - Maintain your organisation's Wikidata item, including its ROR ID, and make sure that the ROR record links to the Wikidata item and ISNI where they exist.
    - Map legacy identifiers, such as GRID IDs and Crossref Funder IDs, to ROR IDs, and do not introduce proprietary organisation identifiers in new implementations.

See also: [Organisations](../../landscape-analysis/organisations.md) · [ROR ID](../../data-on-pids/ror.md)
