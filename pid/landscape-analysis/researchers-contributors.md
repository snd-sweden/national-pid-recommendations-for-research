# Researchers and other contributors

_Last updated: 2025-10-06_

Identification of researchers and other contributors has emerged as one of the most critical use cases of persistent identifier systems. 

The use of unambiguous identifiers for researchers will prevent misidentification in many situations. Ambiguity may often be caused by researchers sharing names with other individuals within their fields, changing names during their careers, using various abbreviation patterns, changing institutional affiliations or performing work within multiple disciplinary clusters. 

Many actors and infrastructures such as publishers, research organisations and funders have transitioned from using simple lists of individuals with plaintext affiliation or contact details into requiring an unambiguous PID for each individual. 

Full PID systems for identifying researchers and contributors may enable continuous updating of PID kernel metadata such as personal details, affiliations and relations to works and other entities.

## International PIDs and identifiers

### ORCID

🟢 Active

[ORCID](https://orcid.org) (Open Researcher and Contributor ID) is a PID for researchers and other contributors active in the research sector.

The format of an ORCID consists of sixteen digits in groups of four, i.e.:
`0000-0002-1825-0097`  
It is also commonly expressed as a resolvable link using the ORCID resolver, leading to a corresponding ORCID profile page: [https://orcid.org/0000-0002-1825-0097](https://orcid.org/0000-0002-1825-0097)

An ORCID record may contain basic information about the individual, such as their first and last names along with any name variants, affiliations and employments and contact information.
It may also contain metadata describing related research activities such as publications and other works, research grants, along with other professional activities such as peer review activity, memberships and positions.
Metadata on education, degrees and qualifications may be added as well as details on past employments, research interests and other biographical information. This means that a well-populated ORCID record will have many similarities to a traditional researcher profile, personal bibliography or CV.

The ORCID concept gives emphasis to the individual being in control of the information that is being shared. A researcher may freely add or edit metadata in their ORCID record. They may also change the visibility of their record to be private or only shared with certain parties, although this will negate most of the benefits of ORCID, since only the name of the individual will be visible.

ORCID is run as a service by the non-profit organisation ORCID, Inc. Creating and maintaining an ORCID record for oneself is completely free of charge for individuals. However, organisations and consortia may become institutional members of ORCID, which provides access to additional administrative features. This requires a member fee, which in turn helps maintaining the service.

In addition to individual record pages on the web, ORCID metadata is machine-readable using a public API.
While the basic idea is that individuals will create metadata for their individual records, organisational members and consortium members may optionally update metadata for their affiliated researchers and contributors using the ORCID member API. This means that a research organisation may ensure that metadata on current affiliations in faculty or staff records stays up to date, or that a publisher may add new publications to the records of their authors using automated workflows.

### ISNI

🟢 Active

ISNI (_International Standard Name Identifier_) is since 2012 an ISO standard (ISO 27729) for providing unambiguous identifiers referring to individuals as well as organisations, with the main purpose being to identify contributors. ISNI keeps track of name variants as well as related entities. A lookup service is available at isni.org, but alternative resolvers are also available. ISNI is in widespread use throughout many sectors.

ISNI is managed through the ISNI International Agency (ISNI-IA) in the UK, while regional or national organisations may become ISNI Registration Agencies or ISNI Members. While anyone may suggest modifications to ISNI entries, only ISNI RAs and Members have direct access to editing entries.

In Sweden, the [National Library](../pid-actors-sweden/kb.md) is an ISNI Member.

### VIAF

🟢 Active

VIAF (_Virtual International Authority File_) is a database with the main purpose of acting as an international source of authority control (i.e. disambiguation of agents) for library services. VIAF IDs may identify individual contributors and authors as well as organisations. The database is populated through sourcing and harmonising authority metadata from various library systems internationally, as well as other metadata sources such as ISNI.

VIAF IDs may be accessed through permalinks. A VIAF ID is clustered and may have several related names.

Because of its origins, VIAF is mainly used to support library infrastructures, but other systems may make use of it as an additional identifier and metadata source.

The VIAF Consortium was formed in 2003 and the VIAF infrastructure is hosted by OCLC. The [National Library of Sweden](../pid-actors-sweden/kb.md) is a VIAF Contributor.

### Wikidata Q identifier

🟢 Active

[Wikidata](https://www.wikidata.org/) is an international knowledge graph containing metadata describing items (entities) with formal relationships to other items using relational expressions (semantic triples). It serves as a data source for Wikipedia and many other infrastructures worldwide.

Since Wikidata may be used to describe various objects and entities, an individual may also be described as a Wikidata item with an identifier beginning with the letter Q (Q-ID). Wikidata entries may be enriched with other relevant information about an individual. Metadata describing the individual may be created in many ways using relevant Wikidata properties and items, such as PIDs and other identifiers. This makes Wikidata entries useful for cross-referencing PIDs and other information associated with the individual.

For example, the neuroscientist Arvid Carlsson (1923-2018) has the Wikidata Q identifier `Q298045` which may be resolved at: https://www.wikidata.org/wiki/Q298045

Wikidata is maintained by the Wikimedia Foundation and its contents may be edited by volunteers. The accuracy is generally high, but because of its open nature, metadata may need additional verification or curation. Research organisations will benefit from active maintenance and quality control of Wikidata item entries describing affiliated individuals, such as updating or correcting related identifiers and other metadata within the entry.

## Swedish national level PIDs and identifiers

### Libris authority metadata

🟢 Active

The [National Library of Sweden](../pid-actors-sweden/kb.md) maintains Libris, the national library catalogue. In parallel, they also govern the Libris authority file used for unambiguous identification of works, individuals and organisations. The authority file is built upon the RDF-based BIBFRAME standard. Authority metadata is created by individual libraries and will populate VIAF entries after curation.

Researchers and contributors may be indexed as individual Agent entries in the Libris authority file, obtaining unique identifiers. Individual Agents in the authority file are linked to ISNI and VIAF identifiers. Entries may be interacted with through the web or by downloaded structured metadata files.

Individual Agent entries will be assigned an unique author ID number together with to an unique string. For example, the neuroscientist Arvid Carlsson (1923-2018) has a Libris authority ID of `180301` and a unique ID string, `hftwwpc100ql11x`. These may be resolved online, both leading to the same human-readable entry also available in machine-readable formats: http://libris.kb.se/resource/auth/180301 and 
https://libris.kb.se/hftwwpc100ql11x

### Swedish personal identification number

🟢 Active

The Swedish personal identification number (_personnummer_) is a unique 10 or 12-digit number [assigned to everyone in the Swedish Population Register](https://skatteverket.se/servicelankar/otherlanguages/englishengelska/individualsandemployees/livinginsweden/personalidentitynumbers) by the Swedish Tax Agency, consisting of a birthdate (YYMMDD) or (YYYYMMDD) followed by four additional digits, with the last digit being a checksum.

It is rarely used in public research communication but may be used to verify records, accounts and authentication methods along with other credentials.

### Institutional user account names

🟢 Active

While rarely used in public communications as an identifier, institutional user account names play an important role in the identification of an individual, especially in the case of federated identity providers used by many research infrastructures and services. 

In some cases they may be used when cross-referencing researcher contributions, such as acting as a fallback identifier for authors in the Swedish national publication index [SwePub](https://swepub.kb.se) maintained by the National Library of Sweden.

### SWAMID, eduPerson and eduPersonPrincipalName (ePPN)

🟢 Active

While not being commonly used in public communication, identities registered with federated identity providers is widely used for authorization and disambiguation of researchers and contributors.

In Sweden, most research performing organisations have their users registered with [SWAMID](https://wiki.sunet.se/display/SWAMID), the Swedish Academic Identity Federation. SWAMID acts as an identity provider using several common protocols, allowing cross-organisational identity checking. SWAMID is also connected to the international identity federation [eduGAIN](https://edugain.org). SWAMID registers metadata on the individual corresponding to the LDAP-compatible [eduPerson](https://wiki.refeds.org/display/STAN/eduPerson) schema maintained by the REFEDS group.

In the eduPerson schema, the eduPersonPrincipalName (ePPN) value is used to provide a unique, human-readable identifier for the individual. the ePPN is created using the pattern `localaccount@organisation.se`. This means that the user `anettez` at Stockholm University, `su.se`, will receive the ePPN `anettez@su.se`. While looking similar, the ePPN is not an e-mail adress. However, some organisations may still opt to make it resolve to a mailbox. 

## Proprietary identifiers

### Scopus Author ID

🟢 Active

A Scopus Author ID will be generated for new individuals listed as authors and contributors in entries indexed in Elsevier's proprietary bibliographic database, Scopus.

The Scopus Author ID may be created upon creating a user account, or is generated algorithmically based on name, email, affiliation, subject area, citations and co-authors once a publication has been indexed. It is typically a 11-digit number. 

For example, the neuroscientist Arvid Carlsson (1923-2018) has the Scopus Author ID: `35509103000`. This will resolve to a Scopus Author Profile with related publications, in this case: https://www.scopus.com/authid/detail.uri?authorId=35509103000

Algorithmically generated Scopus Author IDs may be claimed by the author after proving their identity. Since the Scopus Author ID may be generated automatically, disambiguation sometimes fails and multiple IDs may be generated for the same individual, based on f.e. name variations. In this case, individuals with Scopus accounts may request a merge of profiles using the "Request to merge authors" button.

### Web of Science ResearcherID

🟢 Active

A Web of Science ResearcherID will be generated for new individuals listed as authors and contributors in entries indexed in Clarivate's proprietary databases in the Web of Knowledge product family.

The ResearcherID is generated after creating a user account or is generated algorithmically once a publication with the contributor has been indexed.

For example, the neuroscientist Arvid Carlsson (1923-2018) has the Web of Science ResearcherID: `MJA-8149-2025` and an associated numeric ID: `69266209`. They will both resolve to a Web of Science Author Profile with related publications, in this case: https://www.webofscience.com/wos/author/record/MJA-8149-2025 and https://www.webofscience.com/wos/author/record/69266209

Algorithmically generated ResearcherIDs may be claimed by the author after proving their identity. Since the ResearcherID may be generated automatically, disambiguation sometimes fails and multiple IDs may be generated for the same individual, based on f.e. name variations. In this case, individuals with Web of Science accounts may request a merge of profiles using the "Delete/merge account" function.