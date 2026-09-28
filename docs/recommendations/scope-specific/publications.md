# Publications and citations

_Last updated: 2026-09-28_

These recommendations concern the identification of scholarly publications, such as journal articles, books, chapters, conference papers, reports and theses, and the representation of citations between research outputs. For the scope of the scope-specific recommendations and how PID systems are preferred, see [Scope-specific recommendations](index.md).

## Use DOIs with rich metadata for scholarly publications

_Applies to: publishers, repositories, research organisations and researchers._

!!! quote ""

    Use DOIs as the primary PIDs for scholarly publications, registered by the publisher or repository responsible for the publication. Register rich metadata, including contributors' ORCID iDs, affiliations' ROR IDs, funding, licence, references and relations to other outputs.

??? question "Why?"

    DOIs are the most widely used PIDs for scholarly publications, and they are recognised by publishers, libraries, research information systems and citation indexes worldwide. Each DOI comes with kernel metadata registered with its provider. DataCite DOI and Crossref DOI metadata is designed for publishing workflows and covers references, funding, licences and relations between publications and other outputs.

    Both major DOI providers make their metadata openly available through open APIs, and it is harvested by aggregators such as the OpenAIRE Graph and OpenAlex. Rich DOI metadata therefore links a publication to its authors, organisations, funding and underlying data automatically, and makes it part of scientific knowledge graphs without further registration.

??? info "How?"

    - Use DataCite DOIs or Crossref DOIs for journal articles, books, chapters and conference proceedings issued by publishers, including university presses and journals run by Swedish organisations.
    - Likewise, use DOIs for reports, theses and other publications issued through institutional repositories that do not already have a DOI.
    - Include ORCID iDs, ROR IDs, funder ROR IDs and grant PIDs, a licence URI and an abstract in the metadata, and deposit reference lists with their PIDs.
    - As a publisher, collect research activity information with RAiD and funding information with funder ROR IDs and grant PIDs at submission, and keep it through production into the registered metadata.
    - Link preprints, accepted manuscripts and versions of record to each other with explicit relations.
    - Store and display DOIs in their resolver form, for example `https://doi.org/10.xxxx/xxxxx`.

See also: [Publications](../../landscape-analysis/publications.md) · [Citations](../../landscape-analysis/citations.md) · [DOI](../../data-on-pids/doi.md)

## Use URN:NBN as a complement for Swedish digital publications

_Applies to: research organisations with publication repositories._

!!! quote ""

    Use URN:NBN for Swedish digital publications that need a PID but have no DOI or other primary PID, and as a complementary identifier in national bibliographic and preservation workflows. Where a publication should be discovered, cited and linked across the research information landscape, prefer a DOI as the primary PID and record the URN:NBN as an alternate identifier.

??? question "Why?"

    URN:NBN is well established in Swedish publication repositories and in the national bibliographic infrastructure, and Swedish URN:NBNs are resolved by the national resolver of the [National Library of Sweden](../../pid-actors-sweden/kb.md). It is particularly used for reports, theses, student essays and similar publications issued by research organisations.

    URN:NBN does not have kernel metadata, so the description of each publication depends entirely on the repository that holds it. URN:NBNs are also less visible than DOIs in citation practice and in international aggregators, which limits how well the publication is linked to other research information.

??? info "How?"

    - Keep assigning URN:NBNs in established repository workflows.
    - When a publication also has a DOI, keep the DOI as the primary PID and record the URN:NBN as an alternate identifier for the same publication, not as an identifier of a different object.
    - Make sure that the repository landing page provides machine-readable metadata, since URN:NBN has no kernel metadata of its own.
    - Store and display URN:NBNs with the national resolver, for example `https://urn.kb.se/resolve?urn=urn:nbn:se:lnu:diva-80554`.

See also: [Publications](../../landscape-analysis/publications.md) · [URN:NBN](../../data-on-pids/nbn.md) · [National Library of Sweden](../../pid-actors-sweden/kb.md)

## Keep publication-specific identifiers as linked alternate identifiers

_Applies to: repositories, research information systems and publishers._

!!! quote ""

    Record ISBNs, ISSNs, PMIDs and other publication-specific identifiers as alternate or related identifiers linked to the publication's primary PID. Distinguish preprint identifiers from identifiers for an accepted and published article.

    Do not use the identifiers of entries in bibliographic databases as substitutes for PIDs with kernel metadata such as DOIs, but make use of deduplication identifiers created by research output aggregators for cross-referencing.

??? question "Why?"

    Publication-specific identifiers identify particular aspects of publications, such as an edition of a book, a journal or series, a preprint server record or an entry in a disciplinary database, and they are used in many disciplinary workflows. Most of them have no global resolver or kernel metadata of their own, so their value lies in being linked to a metadata-rich PID.

    Research output aggregators may help with research output tracking by indexing and deduplicating references to research outputs. Identifiers of entries in proprietary bibliographic databases identify the bibliographic records rather than the publications themselves.

??? info "How?"

    - Use ISBNs for editions of books and ISSNs for serials, as assigned by the [National Library of Sweden](../../pid-actors-sweden/kb.md) for Swedish publications, and DOIs for individual chapters and articles.
    - Link preprint identifiers, such as arXiv or bioRxiv identifiers, to the DOI of the version of record, and show both as related but separate objects.
    - Record PMIDs and PMCIDs as related identifiers for publications indexed in PubMed and PubMed Central.
    - Keep deduplication identifiers from research output aggregators and proprietary bibliographic database identifiers for matching and analysis.

See also: [Publications](../../landscape-analysis/publications.md)

## Make citations open and based on PIDs

_Applies to: publishers, repositories, research organisations and researchers._

!!! quote ""

    Express citations as relations between the PIDs of the citing and cited works, make reference lists available as open metadata, and support open citation indexes.

??? question "Why?"

    Citation data is used to follow scholarly influence, to assess research and to build scientific knowledge graphs. Citation indexes that require subscriptions limit who can use and verify this information. Open citation indexes, such as OpenCitations, the OpenAIRE Graph and OpenAlex, depend on reference lists and citation relations that are registered as open metadata with PIDs.

    When data, software and other outputs are cited with their PIDs, they also become visible in citation data. An Open Citation Identifier may identify a citation relationship itself, but it does not replace the PIDs of the works involved.

??? info "How?"

    - As a publisher, deposit complete reference lists, including the PIDs of cited works, as open metadata.
    - As a repository, record citation relations in DOI metadata, such as Cites and IsCitedBy, and relations between publications and their underlying data, such as IsDerivedFrom.
    - As a researcher, cite data, software and other outputs with their PIDs in reference lists, not only in the text.
    - As a research organisation, prefer open citation data where it serves the purpose of an analysis, and report errors in open citation data to the services concerned.

See also: [Citations](../../landscape-analysis/citations.md) · [DOI](../../data-on-pids/doi.md) · [Express relationships between PIDs as links with explicit relation types](../generic/referencing.md#express-relationships-between-pids-as-links-with-explicit-relation-types)
