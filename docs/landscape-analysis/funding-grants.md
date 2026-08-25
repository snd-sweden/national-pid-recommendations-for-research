# Funding and grants

_Last updated: 2026-08-23_

Information about how research is funded is one of the most requested, and most fragmented, pieces of research metadata. Funding information ties together several other entities already covered in this landscape analysis: the [organisations](organisations.md) that provide funding, the [research activities](projects-activities.md) that are funded, and the [publications](publications.md) and other outputs that resulted from that funding. 

Unambiguous identification of research funding and grants ensures that funders will get attribution, while also making it possible to follow how resources assigned to research activities translate into long-lasting benefits. Reliable identification of funding is therefore a key enabler for evaluating research impact, tracking public spending on research, and building open, machine-readable [PID graphs](../pid-concepts/pid-ecosystem.md). However, challenges for identification of funding and grants remain in many cases. 

The traditional method of providing information on funding and grants is through mentioning them in research publications, typically in a section for declaring acknowledgements or conflicts of interest, and in some cases in a dedicated funding section. The practice of mainly mentioning funding and grants within the text of a research publication may create several vulnerabilities, such as ambiguous names or identifiers of grants and projects, or only being able to name the funding organisation itself.

Funders may have many different ways of granting funding and keeping track of it, and public availability of information on grants is not guaranteed. Funders may not have the resources, staff or technical infrastructure to describe individual grants, such as through maintaining an updated web presence.

Using PIDs to identify both the **funder** and the **specific grant awarded** removes the need for manual cross-checking and interpretation of funding information, and makes the information available as machine-readable metadata for tracking and follow-up analyses.

## Identifying the funder

The organisation or entity providing research funding is often, at a minimum, mentioned or attributed by name in the research context.  However, there are many cases where name-only identification of research funders remains ambiguous. 

The need for correct identification of the research funder and the corresponding solutions for acheiving it will largely be the same as for any other [research organisation](organisations.md). This means that the funding organisation will benefit from being identifiable by widely used PIDs for research organisations, such as [ROR ID](../data-on-pids/ror.md). 

Maintaining a presence in the ROR Registry will give the funder an opportunity to specify canonical name forms in several languages for international use as well as to create metadata on funder country origin and other details. This may prevent common problems such as when smaller research funders, f.e. memorial funds, do not have established international names and are subject to arbitrary name translations by authors.

Other PID systems used for identifying funders, such as Crossref Funder ID (Open Funder Registry) and GRID have officially deprecated themselves in favour of the ROR system, while the older, proprietary Ringgold ID system sees little use in new implementations.

## Grant numbers and names

There are many different conventions on how to delimit, name and address a grant, stipend or award. 

A common convention is creating an internal **grant number** or **grant ID** valid for identifying the grant within the funding organisation. This may be a number or string following a simple pattern like `<year>-<sequential_figure>`, such as `2023-059`. This will most often create conflicts with other grant numbers, causing some funders to assign other patterns such as `<funder>-<year>-<sequential_figure>` to their grant numbers, f.e. `NRC-2023-059`.

Another common pattern is to use the **project title** of a specific research project as the identifier for a grant. Since this most often is the title that the researchers wrote on the grant application when presenting their research proposal, many funders also find it convenient to use for identification of the grant itself.

A third pattern in use is identifying the grant by the **name of the individual researcher** who was awarded the grant. This may be the case for funders who are content with maintaining f.e. annual listings of grant awardees.

In all examples above, grant numbers and names may sometimes only be provided in an in-text mention, or as string-type textual metadata. This ambiguity may be done away with by creating resolvable **grant PIDs** for each logical grant awarded, along with a corresponding [landing page](../pid-concepts/landing-pages.md).

## _Grant_, or _project_?

Many research endeavors are heavily reliant on external funding. Funders may create targeted funding calls with specific objectives, where the grant makes up the entirety of the funding of a specific project. 

This has created a situation where it is relatively common that funders and systems may consider the **grant** entity by itself to be a **research project** entity. The practice of sometimes using research project titles to refer to awarded grants may also enforce this view. Some systems also refer to their grant numbers as **project IDs**.

However, this must be considered a dysfunctional concept that is of limited use outside the funding organisation itself, while not being interoperable with identification and description of [research projects and activities](projects-activities.md) in general. A specific research project may be funded by _several_ different grants and resources at the same time, or it may have _no_ specific external funding assigned to it at all.

Responsible identification of grants as well as their related research projects therefore requires the careful use of PIDs to identify grants as well as projects as separately adressable, well defined individual entities.

## International PIDs and identifiers

### DOI

🟢 Active  

A commonly used PID to refer to individual grants is the [DOI](../data-on-pids/doi.md) system. This will allow for providing detailed funding information on the landing page of the grant DOI, as well as funding metadata embedded in the [kernel metadata](../pid-concepts/kernel-metadata.md) payload distributed using the schema of the DOI [provider](../pid-concepts/pid-ecosystem.md#provider) in use. 

Crossref DOIs are currently in wide-spread use for grant DOIs, having a well developed metadata schema[@web-GrantsMarkupGuide]. Most notably, they are employed in the Crossref GLS as described below. DataCite DOI is also providing good support for grants through its kernel metadata [@web-OpenFundingMetadata-26].

Several specific implementations of DOIs for identifying grants are described below.

### Crossref Grant ID (Grant Linking System)

🟢 Active

The [Grant Linking System](https://www.crossref.org/services/grant-linking-system/) (GLS), operated by Crossref, allows research funders to register individual grants and obtain a unique, resolvable Crossref Grant ID for each one. Like other Crossref identifiers, a Grant ID takes the form of a DOI, distinguishing it from the recently deprecated DOI-based [Crossref Funder ID](organisations.md#open-funder-registry-id-crossref-funder-id) which identifies the funding organisation rather than an individual grant.

For example, the DOI `10.35802/107769` identifies a specific Wellcome Trust grant and resolves to a landing page describing the award, its recipient and its funder: <https://doi.org/10.35802/107769>. Grant DOIs may in turn be included in the metadata of resulting outputs (such as article or dataset DOIs), creating an explicit machine-readable relation between funding and outputs.

The GLS became operational in 2019, following a 2017 Crossref board decision to prioritise funding metadata, and was developed together with the Funder Advisory Group and partners such as Europe PMC. As of the system's fifth anniversary, over 35 funders were participating, including Wellcome, the European Research Council, NWO (Dutch Research Council), the Austrian Science Fund (FWF) and the Japan Science and Technology Agency (JST), together registering well over 100,000 grants.

Coverage remains dependent on individual funders actively registering their grants; many funders, including the major Swedish research funders, do not currently participate.

### CORDIS EU project grants

🟢 Active

[CORDIS](https://cordis.europa.eu) (Community Research and Development Information Service) is the European Commission's repository of information on project grants funded under the EU's framework programmes for research and innovation, from FP1 through to Horizon Europe. Each funded project is identified by its **Grant Agreement Number**, being a grant number assigned when the grant agreement is signed.

From Horizon 2020 onwards, each project grant is in addition assigned a Crossref DOI following the pattern `10.3030/<grant agreement number>`, minted and maintained by the Publications Office of the European Union, and resolvable through the standard DOI resolver: <https://doi.org/10.3030/101137734>. This resolves to the CORDIS landing page, currently at <https://cordis.europa.eu/project/id/101137734>.
This makes EU-funded project grants a good example of grants with a globally resolvable, DOI-based identifier assigned by the funder itself rather than by a third-party aggregator.

When examining the kernel metadata for the grant DOI at <https://api.crossref.org/works/doi/10.3030/101137734>, we can see that rich machine-readable information about the grant is available, such as the size of the grant in EUR, the corresponding funding programme, or the identity of the funder expressed with a PID.

CORDIS project grant records commonly appear as the funding source referenced from other entities described in this landscape analysis, such as [OpenAIRE Graph Project](projects-activities.md#openaire-graph-project) entries and article-level funding metadata.

## Swedish national level identifiers and data sources

### Swecris _Project-ID_

🟢 Active  

The Swedish grant index [Swecris](https://www.vr.se/swecris/) is maintained and provided by the [Swedish Research Council](../pid-actors-sweden/index.md) since 2016, covering awards from 2008 and onwards. 

Swecris lists information on grants awarded by some of the larger public research funders in Sweden (f.e. Formas, Forte, Riksbankens Jubileumsfond, Vinnova and the SRC itself), as well as several others. This in line with the requirement, shared across EU member states, to report public research funding data to the EU's e-infrastructure for research information.

While providing basic metadata about the awarded grant, it also provides certain grant number (here called: **Project-ID**) harmonisation and collision prevention. For example, an older Vinnova grant with the internal Vinnova grant number `2010-02635` has been indexed as `2010-02635_Vinnova` in Swecris . The corresponding entry may be accessed at: <https://www.vr.se/english/swecris.html#/project/2010-02635_Vinnova>

Swecris also provides [API-level access](https://www.vr.se/swecris/swecris-api.html) to the metadata of all grants indexed by the system, where they may be retrieved using their respective grant numbers. However, the Swecris system provides no resolvable PIDs for grants. 

When using the API, some PIDs related to the grants may be extracted, such as [ORCID](../data-on-pids/orcid.md) for the _Principal Investigator_ if available.

### GDP API

🟢 Active  

The [GDP project](https://gdphub.se) (_Gemensamma data-projektet_) is an attempt by Vinnova, Forte, Formas and the Swedish Research Council to create a Swedish standard for disseminating metadata on research grants, grant applications and funding calls through a REST API. This API may then be implemented by individual Swedish research funding organisations.

Read access to the APIs requires registration through the coordinating portal [GDPHub.se](https://gdphub.se).

At the moment, the grant data retrievable using the APIs do not include any PIDs. The grants are indexed using their internal grant numbers (diarienummer), such as `2026-01990`, while funders and research principals are identified by their corresponding [Swedish organisation numbers (organisationsnummer)](organisations.md#swedish-organisation-number-organisationsnummer), such as `202100-3153`.

### Prisma

🟢 Active

[Prisma](https://prisma.research.se/) is the joint application and case management system used by several major Swedish funders, including the Swedish Research Council, Forte and Formas, as well as Karolinska Institutet, the Swedish Space Agency and others, for handling grant applications, decisions and reporting. Within Prisma, each case is tracked using a **diarienummer** (registration/case number) assigned by the responsible funder. This makes Prisma an important ingestion mechanism for funding call and grant metadata.

While a diarienummer uniquely identifies a case within its issuing authority, and is commonly used as a de facto grant number when citing Swedish funding, it is not a globally unique or openly resolvable persistent identifier: formats differ between funders, numbers may be reused across authorities, and there is no shared resolver. This mirrors the situation described for the Swedish organisation numbers (organisationsnummer), which likewise serves as a practical fallback identifier in the absence of a dedicated PID.

## Other international funding data sources

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

CRISP was retired on 31 October 2009 and replaced overnight by NIH RePORTER, which retained the underlying Core Project Number identifiers while adding new query fields and links to resulting publications and patents. Legacy CRISP-era data remains accessible through the [NIH ExPORTER](https://reporter.nih.gov/exporter) data feeds.