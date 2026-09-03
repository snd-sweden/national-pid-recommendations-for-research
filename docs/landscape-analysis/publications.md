# Publications

_Last updated: 2026-08-31

Persistent identifiers for publications uniquely and permanently identify scholarly works such as journal articles, books and other academic works in the digital environment. They ensure consistent access, accurate citation and facilitate research sharing and collaboration.

The PID landscape for traditional research publications may be considered quite mature compared to other digital objects in research. However, because of historical reasons, some identifiers for publications do not have global online resolvers or independently readable kernel metadata.

## Generic PIDs for digital publications

### DOI

🟢 Active  

A [DOI (Digital Object Identifier)](../data-on-pids/doi.md) is a unique and persistent alphanumeric string that may be assigned to digital publications such as journal articles, books, research reports and many other scholarly works. 

DOIs take the form of a string of numbers, letters and symbols prefixed with `10.` followed by a registrant code and a suffix, such as `10.1234/abcde.5678`. The full DOI is often presented as a URL link including a DOI resolver, such as: <https://doi.org/10.1234/abcde.5678>, ensuring an unambiguous link to a publication. 

DOIs also contain a [kernel metadata](../pid-concepts/kernel-metadata.md) package with information about the target publication, maintained and stored independently in the PID system itself. This metadata is fetched and reused for many purposes, such as tracking publications or creating references. Besides basic metadata such as titles and contributors, it may store metadata on citations or other relationships between different publications, organisations and individuals.  

It should be noted that the usage scope of DOIs is wider than just publications and, depending on the implementation, a DOI may also refer to many other types of digital objects.  

There are several [PID Providers](../pid-concepts/pid-ecosystem.md) for DOIs. For research publications such as journal articles and book chapters, the most common global PID Provider is CrossRef.

### Handle

🟢 Active  

A [Handle](../data-on-pids/handle.md) is a basic persistent identifier providing redirection to an object. Handles are assigned to diverse publications such as journal articles, technical reports and books. They are widely adopted in many research sectors, such as in the cultural heritage sector and humanities.

A Handle consists of a prefix issued by the Handle.net registry and a suffix that uniquely identifies the handle under that prefix, for example `20.500.12703/5377`. It will be registered in the Global Handle Registry and will be able to generate a persistent link with the appropriate resolver: <https://hdl.handle.net/20.500.12703/5377>

The core Handle system is also used to provide the base infrastructure of many other PID systems. While such systems may use the Handle system internally, they often extend the Handle infrastructure considerably and should be considered unique PID systems of their own.

### ARK

🟢 Active

[ARK](../data-on-pids/ark.md) (_Archival Resource Key_) is a PID system used by archives, libraries, museums, government agencies and many other organisations and infrastructures. ARKs can identify digital objects as well as physical objects and is thus very wide in scope. ARKs may be used for research publications, but are more commonly used for source materials and digitised objects, such as archival or cultural heritage materials.

Creating ARK-based workflows may be relevant for an organisation that wants a to run a flexible identifier scheme by itself, while still enabling global PID resolution. Implementing ARK requires setting up and maintaining a local PID infrastructure. 

ARK may be especially useful for institutions managing collection-based materials, where the maintainer wants to define unique identifier patterns or hierarchies. It supports custom patterns within the ARK core identifier, or the creation of object subdivisions using ARK qualifiers.

An organisation wanting to use ARK will register for a NAAN (Name Assigning Authority Number), acting as the root namespace for the organisation in the ARK scheme. It may then implement core identifier patterns for its specific use case. 

**Example:** The NAAN `ark:29072` has been registered by the _Bodleian Library_ of the University of Oxford, and `ark:/29072/ora_724ce67f51034b649ccb953d1e81b540` is an ARK referring to a bibliographic journal article entry in the _Oxford University Research Archive_. It may be resolved using the global ARK resolver: <https://n2t.net/ark:/29072/ora_724ce67f51034b649ccb953d1e81b540>




### National Bibliography Number (URN:NBN)

🟢 Active  

[NBN](../data-on-pids/nbn.md) (_National Bibliography Number_) is a generic PID for digital publications. 
It uses the [URN scheme](https://en.wikipedia.org/wiki/Uniform_Resource_Name) and is therefore commonly referred to as **URN:NBN**.

URN:NBN has been implemented in several European countries as part of an effort to give identifiers to all publications included in the national bibliographic cataloguing of a country, most often coordinated by the respective national libraries. NBNs may be systematically assigned to new publications in certain infrastructures, and is also often used to retroactively provide a resolvable PID for digital publications not already having been assigned identifiers, such as an ISBN or a DOI.

Each country using NBN has their own national namespace, meaning that all NBN identifiers associated with the country will have the same initial pattern preceding the unique parts of the identifier. NBN identifiers from the Swedish namespace will always start with: `urn:nbn:se`. 

There may also be sub-namespaces, providing additional capabilities for organisations and infrastructures to create a unique namespace context. For example, Linnaeus University maintain their own sub-namespace at: `urn:nbn:se:lnu`.

The final and unique part of the NBN comes after any namespaces, making up a full NBN such as `urn:nbn:se:lnu:diva-100838`. The target object may be accessed through a resolver for URN:NBN such as: <https://nbn-resolving.org/urn:nbn:se:lnu:diva-100838>

In Sweden, URN:NBN sub-namespaces for `urn:nbn:se` are [assigned by the National Library of Sweden (KB)](https://www.kb.se/isbn-och-utgivning/urnnbn.html).


## Preprints and manuscripts

### arXiv ID
🟢 Active  
The arXiv IDs are identifiers for articles in the open-access repository [arXiv](https://arxiv.org), which is mostly used in physics, mathematics, computer science and related fields. The articles uploaded in arXiv are mainly manuscripts and pre-prints being considered for publication in f.e. academic journals.

The canonical form of arXiv identifiers is `arXiv:YYMM.number`, with a 4-digit or 5-digit integer number for records before or after January 2015, respectively. Specific versions are indicated by appending a version number, e.g. `arXiv:1501.00001v1` or `arXiv:0706.0001v2`. 

### medRxiv and bioRxiv ID
🟢 Active  

The open-access pre-print repositories medRxiv and bioRxiv serve a similar purpose to arXiv, but in the medical and life sciences respectively. They are both built upon the same infrastructure.

medRxiv and bioRxiv identifiers will be generated when uploading new pre-prints and manuscripts to the repositories.
They follow the pattern `YYYY.MM.DD.number`, with number being a 6-digit integer number for records.

The medRxiv and bioRxiv identifiers are also used in the generation of DOIs pointing to the objects.
Thus, `bioRxiv:2025.08.06.668887` will correspond to the resolvable DOI: <https://doi.org/10.1101/2025.08.06.668887>

## Monographs (books)

### ISBN and eISBN
🟢 Active  
An ISBN (International Standard Book Number) is a unique code identifying a specific book, an edition of a book, audiobook or other monographic publication, facilitating cataloging, citation and distribution as well as distinguishing one edition from another.
An ISBN can refer to a physical (ISBN) or digital object (eISBN) and consists of 10 or 13 digits (e.g. `9780857936936`). 

The different segments of the ISBN number correspond to various information such as region information, the registrant organisation minting the ISBN and checksumming. To make the segments easier to distinguish for human readers, an ISBN may sometimes be expressed including hyphens following the official hyphenation scheme (e.g. `978-0-85793-693-6`), however, only the numbers themselves make up the significant parts of an ISBN.

It should be noted that objects being assigned ISBNs may also have other assigned identifiers, such as an e-book being assigned an eISBN, with each book chapter also having been assigned a unique DOI.

The ISBN system was designed in the 1960s and as a result, the infrastructure for the identifiers is decentralised and based on print media paradigms. ISBNs do not have a single mandated global resolution service, and ISBN metadata is governed by various agencies and publishers.

In Sweden, ISBN identifiers for research publications may be [assigned by the National Library of Sweden (KB)](https://www.kb.se/isbn-och-utgivning/isbn.html).

## Serials (journals, book series)

### ISSN and eISSN
🟢 Active  
An ISSN (International Standard Serial Number) identifies a serial publication, such as an academic journal or book series.
It is an 8-digit number prefixed with `ISSN:`, such as `ISSN:1234-5678` or `eISSN:` for electronic versions, e.g. `eISSN:1234-5678`.

In Sweden, ISSN identifiers for research publications may be [assigned by the National Library of Sweden (KB)](https://www.kb.se/isbn-och-utgivning/issn-.html). 

## Bibliographic database entries
These are not identifiers for the digital publications themselves, but for bibliographic entries in databases describing the publications. Since they are providing further details on the actual publication, they may sometimes be used in reference entries.

### PMID and PMCID
🟢 Active  
PMIDs (PubMed IDs) are specific to articles indexed in [PubMed](https://pubmed.ncbi.nlm.nih.gov), and are commonly used for reference and citation of biomedical and life sciences research. PubMed is an open bibliographic database provided by the US National Institutes of Health.
A PMID is composed of digits only, f.e. `31771602`, and will uniquely identify a bibliographic entry in PubMed.

While many entries are strictly bibliographic, note that PubMed also includes PubMed Central (PMC) as a subset, which is a digital repository containing full text articles and manuscripts. PMC entries will have an additional PMCID identifier, such as `PMC6878689`, while also retaining a PMID. A PMID pointing to a PMC entry will thus refer to a copy of the full text or submitted manuscript within PMC, but the article proper will most often be published in another journal or infrastructure. 

Following the above example, the article proper is published in a journal, having been assigned the DOI: `10.1186/s12992-019-0499-1`.

### Web of Science Accession Number
🟢 Active  
Web of Science (WoS) accession numbers or IDs are unique identifiers for Clarivate's proprietary bibliographic database entries on journal articles, conference papers, book chapters and similar works within the Web of Science collection, used for referencing and retrieval. They consist of a series of alphanumeric characters, starting with `WOS:`, such as `WOS:000123456789`.

### Scopus EID
🟢 Active  
Scopus EID is an unique identifier for entries in Elsevier's proprietary bibliographic database, Scopus. It is used to refer to the bibliographic entry of each object (articles, book chapters etc.) indexed in Scopus. An example of a Scopus EID is  `2-s2.0-105009003666`, with `2-s2.0-` being a prefix for the current version of Scopus EID and `105009003666` being the unique identifier string for the bibliographic entry.