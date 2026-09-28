# Researchers and other contributors

_Last updated: 2026-09-28_

These recommendations concern the identification of researchers and other people who contribute to research, such as research engineers, technicians, data stewards and doctoral students. For the scope of the scope-specific recommendations and how PID systems are preferred, see [Scope-specific recommendations](index.md).

## Use ORCID iDs for researchers and other contributors

_Applies to: researchers, research organisations, funders, publishers, repositories and research information systems._

!!! quote ""

    Use ORCID as the primary PID for researchers and other contributors. Collect ORCID iDs through authenticated workflows.

??? question "Why?"

    People are hard to identify reliably by name. Researchers share names with others, change names, use different abbreviations and move between organisations. ORCID is the established international PID for contributors to research, and it is already required or supported by most publishers, funders, repositories and research information systems.

    An ORCID iD is more than an identifier. The ORCID record holds kernel metadata according to the ORCID Record Schema, such as names and name variants, affiliations, works, funding and peer review activities. Public information in ORCID records is openly available through an open API, and the records connect people to the PIDs of organisations, outputs and grants. This makes ORCID one of the main hubs of the PID graph for research.

    ORCID is run by a non-profit organisation with community governance. Swedish research organisations can use its organisational features through the Swedish ORCID consortium maintained by [Sunet](../../pid-actors-sweden/sunet.md).

??? info "How?"

    - Store and exchange ORCID iDs in their canonical resolver form, for example `https://orcid.org/0000-0002-1825-0097`.
    - Collect ORCID iDs by letting people sign in with ORCID, rather than by typing them into forms. This ensures that the iD belongs to the person.
    - Support researchers in registering and using an ORCID iD.
    - Use ORCID iDs as public, cross-organisational personal identifiers in workflows where they are accepted.
    - Include ORCID iDs in all metadata about people's contributions, such as DOI metadata for publications, data and software, grant metadata, RAiD metadata and research information systems.
    - If your organisation is connected to [SWAMID](../../landscape-analysis/researchers-contributors.md#swamid-eduperson-and-edupersonprincipalname-eppn), make ORCID iDs available as an identity attribute for your users.

See also: [Researchers and other contributors](../../landscape-analysis/researchers-contributors.md) · [ORCID](../../data-on-pids/orcid.md) · [Sunet](../../pid-actors-sweden/sunet.md)

## Add verified information to ORCID records

_Applies to: research organisations, funders, publishers and repositories._

!!! quote ""

    With the permission of the individual, add verified information to ORCID records through the ORCID member API, such as affiliations identified with ROR IDs, and works and grants identified with their PIDs.

??? question "Why?"

    ORCID records that are maintained only by the individual are often incomplete or out of date. Information added by the organisation that knows it best, such as an employer adding an affiliation, a funder adding a grant or a publisher adding a publication, is shown in the record together with its source. This makes the record more reliable for everyone who reads it, and reduces the effort needed from researchers.

    ORCID is thereby maintained through collective curation. When organisations write verified information to ORCID and read it back into their own systems, the same information can be reused across applications, reports and research information systems instead of being entered again.

??? info "How?"

    - Ask for the individual's permission through ORCID's authorisation workflow before reading limited information or adding information to a record.
    - As an employer, add employments and other affiliations, identifying your organisation with its ROR ID, and keep end dates up to date.
    - Add outputs from repositories and research information systems, and grants from funders' systems, identified with their DOIs or other PIDs.
    - Read information from ORCID records, with permission, instead of asking researchers to enter it again.
    - Raise awareness of the benefits of collective curation of ORCID records, and advocate for removal of unnecessary restrictions on the visibility of ORCID entries.
    - Use the member API through the Swedish ORCID consortium or an individual ORCID membership.

See also: [Researchers and other contributors](../../landscape-analysis/researchers-contributors.md) · [ORCID](../../data-on-pids/orcid.md) · [Sunet](../../pid-actors-sweden/sunet.md)

## Link ORCID iDs to other identifiers for people

_Applies to: research organisations, libraries and research information systems._

!!! quote ""

    Record other identifiers for people, such as ISNI, Libris authority identifiers, VIAF identifiers and Wikidata identifiers, as linked identifiers alongside the ORCID iD, and use them for people that ORCID does not cover.

??? question "Why?"

    ORCID does not cover everyone. Historical researchers, deceased researchers and contributors who never registered an ORCID iD may still need to be identified. Library authority files, such as the Libris authority file maintained by the [National Library of Sweden](../../pid-actors-sweden/kb.md), ISNI and VIAF, have long coverage and curated metadata, and are linked to each other.

    Wikidata is an openly licensed knowledge graph maintained through collective curation. A Wikidata item for a person can bring together many identifiers for the same person, which makes it useful for cross-referencing and for connecting research information to other knowledge graphs.

    Proprietary author identifiers are generated in closed bibliographic databases. They may be created algorithmically, duplicated for the same person, and their metadata is not openly available, which makes them unsuitable as primary identifiers.

??? info "How?"

    - Record ISNI, Libris authority, VIAF and Wikidata identifiers as alternate identifiers linked to the ORCID iD where they exist.
    - Use ISNI or Libris authority identifiers for people who have no ORCID iD, for example in retrospective registration of older publications.
    - Take part in collective curation: correct and complete the Wikidata items of affiliated researchers where appropriate, including their ORCID iDs, and report errors in authority files to their maintainers.
    - Keep proprietary author identifiers, such as Scopus Author IDs and Web of Science ResearcherIDs, only as secondary identifiers for matching.

See also: [Researchers and other contributors](../../landscape-analysis/researchers-contributors.md) · [National Library of Sweden](../../pid-actors-sweden/kb.md)
