# Citations

_Last updated: 2025-09-01_


The availability of structured metadata describing citations is important for accurately mapping citation networks, tracking scholarly influence and research impact, and enhancing scientometric analyses across the research landscape. 

It is used in the construction of scientific knowledge graphs (SKGs), a concept where open research information is used to create a graph network describing the relations between entities in the scientific ecosystem.

Active indexing of citations is performed by proprietary indexes as well as freely accessible alternatives created by open initiatives. While proprietary databases currently may offer more authoritative citation information, emerging open access indexing is increasing in coverage and accuracy.

## Citation identifiers

Unlike persistent identifiers such as DOIs, which uniquely identify specific works, citation identifiers are designed to explicitly represent the _relationship_ between works and what they cite or refer to. They contain metadata referring to each work involved and establish a clear, unambiguous link indicating what object is citing and which object is being cited, such as another publication or dataset. 

### Open Citation Identifier (OCI)

🟢 Active  
[Open Citation Identifiers](https://doi.org/10.6084/m9.figshare.7127816.v2) (OCIs) are identifiers that represent individual citations. They are created through metadata aggregation in the [OpenCitations](https://opencitations.net) infrastructure.[@jrnl-OpenCitationsInfrastructureOrganization-20]

OCI is a globally unique, machine-readable persistent identifier assigned to citations indexed in open bibliographic sources. It features a simple structure, beginning with `oci:`, followed by two sequences of numbers separated by a dash. The first sequence encodes the citing resource, while the second encodes the cited resource. Both sequences include a prefix indicating the source database, such as Wikidata, Crossref, Dryad or OpenCitations. 

For example, `oci:0606622742-06190834283` identifies a citation between two resources: The publication with the DOI `10.1186/1756-8722-6-59` has been cited by the publication with the DOI `10.2174/0113816128337881241016064641`. This OCI may be resolved through: <https://w3id.org/oc/index/ci/0606622742-06190834283> or using the API: <https://api.opencitations.net/index/v2/citation/0606622742-06190834283>

In addition to OCIs, the OpenCitations infrastructure also creates identifiers called OMIDs (OpenCitations Meta Identifiers). These are used for identification and description of specific entities used in the bibliographic indexing, such as articles or authors, within the OCI infrastructure and metadata entries. For example, the article being cited in the example above has been assigned: `omid:br/06190834283`. OMIDs should, however, not be confused with OCIs themselves.

An OCI is created when a citational relation is identified between two objects in the OpenCitations Corpus, resulting in an entry within the OpenCitations Indexes. There are several OpenCitations Indexes, segmented by source. Examples include _OpenCitations Index of Crossref open DOI-to-DOI citations (COCI)_ and _Crowdsourced Open Citation Index (CROCI)_. COCI identifies the citing and the cited entities by their unique identifiers (DOIs). Unlike COCI, CROCI focuses on incorporating user-contributed citation data to enhance the completeness and diversity of open citation indexes. 

## Citation relations in PID kernel metadata

Some PIDs for digital objects, such as [DOIs](../data-on-pids/doi.md) created by DataCite and Crossref, store unique [kernel metadata](../pid-concepts/kernel-metadata.md) for each object, making it possible to express what the object cites or what it has been cited by. An example of this is the user-definable `Cites` and `IsCitedBy` relation types of the DataCite Metadata Schema. This citation metadata is also reused by citation indexing services. The citation metadata may be updated by the [PID Manager](../pid-concepts/pid-ecosystem.md) but also in certain automated processing by the [PID Provider](../pid-concepts/pid-ecosystem.md).

## Other citation indexing

These actors and infrastructures do not specifically create PIDs for the citations themselves, but store metadata about related citations together with the information on the digital objects (works) that are indexed.

### OpenAIRE Graph

🟢 Active  
[OpenAIRE Graph](https://graph.openaire.eu) is a bibliographic database and scientific knowledge graph. It aggregates open research information from various sources. It is maintained by [OpenAIRE](https://www.openaire.eu/) (Open Access Infrastructure for Research in Europe), an NPO coordinating a European network of repositories, archives and journals that support Open Access policies.

OpenAIRE Graph tracks entities that may be classified as a Research product, Organization, Data Source, or Project. For Research products, OpenAIRE Graph records metadata on citations from different sources. 

Each indexed work (Research product) has a corresponding OpenAIRE ID, such as the article with the DOI `10.1001/jamaneurol.2019.4914` being assigned the OpenAIRE ID `doi_dedup___::67a034cfee43803ebba60ddc448d88ca`.

At the time of writing, full citation relations from OpenAIRE Graph are only accessible through the [ScholeXplorer](https://graph.openaire.eu/docs/apis/scholexplorer/api/) API. 

### OpenAlex

🟢 Active  
[OpenAlex](https://openalex.org) is a bibliographic database maintained by the NPO [OurResearch](https://ourresearch.org). It builds upon the bibliographic data originally collected by Microsoft Academic Graph.

OpenAlex stores citations as relations between individual works. For example, the article `10.1001/jamaneurol.2019.4914` has been assigned a work identifier within OpenAlex: `w3013207020`. To find other works with citations of this article, a lookup may be made using `cites:w3013207020` [through the web interface](https://openalex.org/works?page=1&filter=cites:w3013207020) or [using the OpenAlex API](https://api.openalex.org/works?page=1&filter=cites:w3013207020). 

### Microsoft Academic Graph

🔴 Inactive  
Microsoft Academic Graph was a bibliographic database maintained by Microsoft. It was sourced from Microsoft Academic / Microsoft Academic Search metadata, including citation relations. It was actively updated from 2016 to 2021.

The metadata from Microsoft Academic Graph was released under an open license and merged into OpenAlex.

### Web of Science

🟢 Active  
The [Web of Science](https://clarivate.com/webofsciencegroup/) (WoS) by Clarivate contains a multidisciplinary proprietary database that tracks publications such as scholarly articles and book chapters. When a publication cites another within the database, WoS records this link, creating a network of citation relationships. 

The citation metadata is also used within the separately packaged [Science Citation Index](https://clarivate.com/academia-government/scientific-and-academic-research/research-discovery-and-referencing/web-of-science/web-of-science-core-collection/science-citation-index-expanded/).

Access to the Web of Science is not free; it is a subscription-based service typically available through academic institutions, libraries, or research organizations.

### Scopus

🟢 Active  
[Scopus](https://www.elsevier.com/solutions/scopus) is a multidisciplinary abstract and citation database developed by Elsevier that indexes peer-reviewed literature, including scientific journal articles, conference papers and books. Its citation index tracks references within indexed documents. 

Like Web of Science, access to Scopus is a paid service, typically available for end users through institutional subscriptions.