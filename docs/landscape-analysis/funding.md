# Funding

_Last updated: 2026-08-21_

Information about how research is funded is one of the most requested, and most fragmented, pieces of research metadata. Funding information ties together several other entities already covered in this landscape analysis: the [organisations](organisations.md) that provide funding, the [research activities](projects-activities.md) that are funded, and the [publications](publications.md) and other outputs that resulted from that funding. Reliable identification of funding is therefore a key enabler for evaluating research impact, tracing public spending on research, and building open, machine-readable [PID graphs](../pid-concepts/pid-ecosystem.md).

## Identifying the funder, or the grant?

Two related but distinct entities are commonly conflated under the heading "funding":

* The **funder** — the organisation providing the funding, such as a research council, foundation or company. Funders are a type of [organisation](organisations.md) and are typically identified using the same PIDs used for organisations in general, such as [ROR ID](organisations.md#ror-id) or the [Open Funder Registry ID / Crossref Funder ID](organisations.md#open-funder-registry-id-crossref-funder-id).
* The **grant** (or award) — the specific funding decision, i.e. a defined amount of money awarded to a recipient for a specific purpose, often tied to a [research activity](projects-activities.md) such as a project. Unambiguous identification of the grant itself is more recent and considerably less consistent internationally than identification of the funder.

This page focuses primarily on identifiers for the grant/award itself, since funder identification is already covered under [Organisations](organisations.md).

## International PIDs and identifiers

### Crossref Grant ID (Grant Linking System)

🟢 Active

The [Grant Linking System](https://www.crossref.org/services/grant-linking-system/) (GLS), operated by Crossref, allows research funders to register individual grants and obtain a unique, resolvable Crossref Grant ID for each one. Like other Crossref identifiers, a Grant ID takes the form of a DOI, distinguishing it from the DOI-like [Crossref Funder ID](organisations.md#open-funder-registry-id-crossref-funder-id) which identifies the funding organisation rather than an individual grant.

For example, the DOI `10.35802/107769` identifies a specific Wellcome Trust grant and resolves to a landing page describing the award, its recipient and its funder: <https://doi.org/10.35802/107769>. Grant DOIs may in turn be included in the metadata of resulting outputs (such as article or dataset DOIs), creating an explicit machine-readable relation between funding and outputs.

The GLS became operational in 2019, following a 2017 Crossref board decision to prioritise funding metadata, and was developed together with the Funder Advisory Group and partners such as Europe PMC. As of the system's fifth anniversary, over 35 funders were participating, including Wellcome, the European Research Council, NWO (Dutch Research Council), the Austrian Science Fund (FWF) and the Japan Science and Technology Agency (JST), together registering well over 100,000 grants.

Coverage remains dependent on individual funders actively registering their grants; many funders, including the major Swedish research funders, do not currently participate.

### CORDIS project identifier

🟢 Active

[CORDIS](https://cordis.europa.eu) (Community Research and Development Information Service) is the European Commission's repository of information on projects funded under the EU's framework programmes for research and innovation, from FP1 through to Horizon Europe. Each funded project is identified by its **Grant Agreement Number**, assigned when the grant agreement is signed, and resolvable through CORDIS, e.g. <https://cordis.europa.eu/project/id/101137734>.

From Horizon 2020 onwards, each project is in addition assigned a DOI following the pattern `10.3030/<grant agreement number>`, minted and maintained by the Publications Office of the European Union, and resolvable through the standard DOI resolver: <https://doi.org/10.3030/101137734>. This makes EU-funded projects one of the few categories of grants with a globally resolvable, DOI-based identifier assigned by the funder itself rather than by a third-party aggregator.

CORDIS project records commonly appear as the funding source referenced from other entities described in this landscape analysis, such as [OpenAIRE Graph Project](projects-activities.md#openaire-graph-project) entries and article-level funding metadata.

## Other funding databases

These actors do not mint PIDs for grants themselves in the same sense as the Grant Linking System or CORDIS, but aggregate and index funding information at large scale, often assigning their own internal, non-persistent identifiers.

### Dimensions

🟢 Active

[Dimensions](https://www.dimensions.ai), maintained by the company Digital Science, is a proprietary research information platform that aggregates global funding data alongside publications, patents and clinical trials. It indexes several million grants sourced from funder websites, reports and other public disclosures, linking each grant to the publications and other outputs it is associated with where such relations can be established.

Because grants are sourced and normalised from many disparate sources rather than registered directly by funders, Dimensions' internal grant identifiers are not persistent identifiers in the same sense as a Crossref Grant ID or a CORDIS DOI. Free-tier access to Dimensions is available, with full functionality requiring a paid subscription.

### NIH RePORTER

🟢 Active

[NIH RePORTER](https://reporter.nih.gov) (Research Portfolio Online Reporting Tools Expenditures and Results) is a publicly searchable database of research projects funded by the US National Institutes of Health and other Public Health Service agencies. Each funded project is identified by a **Core Project Number**, such as `R01ES028615`, encoding the activity code, awarding institute and a serial number, with a further suffix indicating the specific budget/fiscal year of a multi-year award.

While Core Project Numbers are consistently used to reference NIH funding in publications and other US federal reporting, they are not a globally interoperable PID scheme and are specific to the NIH/PHS funding context. NIH RePORTER metadata is also available through a public API.

### NIH CRISP database

🔴 Inactive

CRISP (Computer Retrieval of Information on Scientific Projects) was NIH's original public database of federally funded biomedical research projects, covering awards back to 1972 and for many years serving as the primary public tool for looking up NIH-funded grants.

CRISP was retired on 31 October 2009 and replaced overnight by NIH RePORTER, which retained the underlying Core Project Number identifiers while adding new query fields and links to resulting publications and patents. Legacy CRISP-era data remains accessible through the NIH ExPORTER data feeds.

## Swedish national level PIDs and identifiers

Sweden currently has no equivalent to the Crossref Grant ID or CORDIS project DOI, i.e. no nationally coordinated, persistent and openly resolvable identifier assigned to individual grants awarded by Swedish research funders.

### SweCRIS

🟢 Active

[SweCRIS](https://www.vr.se/swecris.html) is a national database showing how participating Swedish research funders have distributed funding to researchers, covering awards from 2008 onwards. It is maintained by the [Swedish Research Council](../pid-actors-sweden/index.md) on behalf of the Swedish government, in line with the requirement, shared across EU member states, to report public research funding data to the EU's e-infrastructure for research information.

Participating funders include Vetenskapsrådet (Swedish Research Council), Forte, Formas, Vinnova, Riksbankens Jubileumsfond and the Swedish Environmental Protection Agency, among others. SweCRIS allows funded projects and researchers to be searched and filtered, and exposes an API, but it does not assign persistent identifiers to the grants themselves; the person identifiers it creates for researchers are also explicitly not guaranteed to remain stable over time.

### Prisma

🟢 Active

[Prisma](https://prisma.research.se/) is the joint application and case management system used by several major Swedish funders, including Vetenskapsrådet, Forte and Formas, as well as Karolinska Institutet, the Swedish Space Agency and others, for handling grant applications, decisions and reporting. Within Prisma, each case is tracked using a **diarienummer** (registration/case number) assigned by the responsible funder.

While a diarienummer uniquely identifies a case within its issuing authority, and is commonly used as a de facto reference when citing Swedish funding, it is not a globally unique or openly resolvable persistent identifier: formats differ between funders, numbers may be reused across authorities, and there is no shared resolver. This mirrors the situation described for the [Swedish organisation number](organisations.md#swedish-organisation-number-organisationsnummer), which likewise serves as a practical fallback identifier in the absence of a dedicated PID.
