# Organisations

_Last updated: 2025-10-06_

[TODO: Add references]: # 

With the rapid digitisation of the research sector, unambiguous identification of organisations have emerged as one of the most important use cases for PIDs.

Examples of organisations benefitting from being identified with PIDs include:

* Universities and colleges
* Research institutes
* Hospitals performing research
* Government agencies performing research
* Commercial entities performing research
* Research funders
* Organisations providing research infrastructures
* Registries and other data providers
* etc.

Identifying organisations with PIDs serve several core needs in the research ecosystem such as providing information on:

* Affiliations of researchers and other contributors
* Legal responsibilities and accountability
* Funding sources
* Provenance of data and other materials
* Individual parties to agreements
* etc.

Since research information is often subject to large-scale automated processing, the existence or absence of an unambiguous organisational PID may in many cases affect critical processes. An example of this is affiliational metadata, directly affecting scientometric analyses, research assessment, indicators and rankings.



## International PIDs and identifiers

### ROR ID 

🟢 Active

Since 2019, the Research Organisation Registry maintains [ROR ID](../data-on-pids/ror.md), which serves as an international index and PID for organisations associated with the research lifecycle.

It has quickly developed into a PID system in widespread use by core actors and systems such as publishers, funders, grant trackers, data repositories, CRIS systems and many others.

Examples of metadata tied to a ROR ID is official names in different languages, abbreviations, country of origin and other PIDs and identifiers describing the same entity.

ROR is maintained as a collaborative initiative by Crossref, DataCite and the California Digital Library. The assignment of ROR IDs and their associated metadata is handled through active curation on Github, taking well-sourced external suggestions into account. New releases of the registry are published in rapid intervals.


### ISNI

🟢 Active

ISNI (_International Standard Name Identifier_) is since 2012 an ISO standard (ISO 27729) for providing unambiguous identifiers referring to organisations as well as individuals, with the main purpose being to identify contributors. ISNI keeps track of name variants as well as related entities. A lookup service is available at isni.org, but alternative resolvers are also available. ISNI is in widespread use throughout many sectors.

ISNI is managed through the ISNI International Agency (ISNI-IA) in the UK, while regional or national organisations may become ISNI Registration Agencies or ISNI Members. While anyone may suggest modifications to ISNI entries, only ISNI RAs and Members have direct access to editing entries.

In Sweden, the [National Library](../pid-actors-sweden/kb.md) is an ISNI Member.

### VIAF

🟢 Active

VIAF (_Virtual International Authority File_) is a database with the main purpose of acting as an international source of authority control (i.e. disambiguation of agents) for library services. VIAF IDs may identify organisations as well as individual contributors and authors. The database is populated through sourcing and harmonising authority metadata from various library systems internationally, as well as other metadata sources such as ISNI.

VIAF IDs may be accessed through permalinks. A VIAF ID is clustered and may have several related names, such as organisational sub-divisions or historical names.

Because of its origins, VIAF is mainly used to support library infrastructures, but other systems may make use of it as an additional identifier and metadata source.

The VIAF Consortium was formed in 2003 and the VIAF infrastructure is hosted by OCLC. The [National Library of Sweden](../pid-actors-sweden/kb.md) is a VIAF Contributor.

### Ringgold ID

🟢 Active

Ringgold ID is a proprietary identifier for organisations that has been maintained since 2003 by the company Ringgold. It was originally created to respond to publishers' needs to disambiguate organisational subscribers, for example to determine publishing fees for authors.  A new Ringgold ID for a yet unregistered organisation may be requested free of charge. There is no open resolver, but the Ringgold Identify Database may be searched with rate-limited guest access after registering an account, and full access can be obtained with a paid subscription. Individual Ringgold IDs are connected to ISNI identifiers.

The use of Ringgold IDs has been waning in research sector, with major infrastructures such as ORCID discontinuing support for Ringgold ID (2023).

### Open Funder Registry ID / Crossref Funder ID

🟢 Active

Crossref has been maintaining the Open Funder Registry (formerly FundRef) since 2013. The explicit purpose has been to assign unambiguous identifers, OFR IDs, to research funders. They are also called Crossref Funder IDs.

OFR IDs are related to research outputs using Crossref DOIs as well as other identifiers. Lookups may be performed using the Crossref API or web search interfaces.

While adoption of OFR IDs have formerly been widespread, especially in publisher infrastructures, Crossref has recently identified that the adoption rate of ROR ID is much higher. To avoid unnecessary efforts spent on maintaining several organisational identifiers, Crossref has initiated a roadmap to sunset OFR IDs in favour of using ROR ID (2024).

### Wikidata Q identifier

🟢 Active

Wikidata is an international knowledge graph containing metadata describing items (entities) with formal relationships to other items using relational expressions (semantic triples). It serves as a data source for Wikipedia and many other infrastructures worldwide.

Since Wikidata may be used to describe various objects and entities, an organisation may also be described as a Wikidata item with an identifier beginning with the letter Q (Q-ID). Wikidata entries are often very useful as a metadata hub to find various information about an organisation. Metadata describing the organisation may be created in many ways using relevant Wikidata properties and items, such as PIDs and other identifiers. This makes Wikidata entries especially useful for cross-referencing various organisational identifier systems.

For example, Lund University has the Wikidata Q identifier `Q218506` which may be resolved at: https://www.wikidata.org/wiki/Q218506

Wikidata is maintained by the Wikimedia Foundation and its contents may be edited by volunteers. The accuracy is generally high, but because of its open nature, metadata may need additional verification or curation. Research organisations will benefit from active maintenance and quality control of their respective Wikidata item entries.

### GRID ID

🔴 Inactive 

GRID ID (_Global Research Identifier Database_) was a PID system active between 2015-2021, set up by the company Digital Research. It served a purpose similar to ROR ID.

Since 2021, ROR has incorporated all entities formerly assigned a GRID ID, formally superseding it as a PID system. GRID ID:s may be searched for in the ROR registry to find a corresponding ROR record, but the old GRID ID resolver has been discontinued.

## Swedish national level PIDs and identifiers

### Swedish organisation number (organisationsnummer)

🟢 Active

In Sweden, a legal person such as a government agency, association or company should be identifiable using a Swedish organisation number (also called registration number, company registration number). This includes many organisational entities such as research-performing organisations and funders. The number is obtained through registering the organisation with the responsible agency, such as Statistics Sweden for governmental agencies, the Swedish Tax Agency for foundations and the Swedish Companies Registration Office  for companies.

Because of legal requirements, the organisation number may serve as a fall-back identifier for Swedish research organisations not yet having been assigned an international organisational PID for the research sector, such as ROR ID.

### Libris authority metadata

🟢 Active

The [National Library of Sweden](../pid-actors-sweden/kb.md) maintains Libris, the national library catalogue. In parallel, they also govern the Libris authority file used for unambiguous identification of works, individuals and organisations. The authority file is built upon the RDF-based BIBFRAME standard. Authority metadata is created by individual libraries and will populate VIAF entries after curation.

Research organisations and funders may be indexed as Agent entries in the Libris authority file, obtaining unique identifiers. Organisational Agents in the authority file are linked to ISNI and VIAF identifiers and may contain relations to subdivisions of the organisation. Entries may be interacted with through the web or by downloaded structured metadata files.

Organisational Agent entries will be assigned an unique ID number together with to an unique string. For example, Lund University has a Libris authority ID of `122845` and a unique ID string, `97mpmc9t38pfj80`. These may be resolved online, both leading to the same human-readable entry also available in machine-readable formats: http://libris.kb.se/resource/auth/180301 and 
https://libris.kb.se/97mpmc9t38pfj80
