# Funding and grants

Unambiguous identification of research funding and grants ensures that funders will get attribution, while also making it possible to track how resources assigned to research activities translate into long-lasting impact and benefits. However, challenges for  identification of funding and grants remain in many cases. 

The traditional method of providing information on funding and grants is through mentioning them in [research publications](publications.md), typically in a section for declaring acknowledgements or conflicts of interest, and in some cases in a dedicated funding section. The practice of mainly mentioning funding and grants within the text of a research publication may create several vulnerabilities, such as ambiguous names or identifiers of grants and projects, or only being able to name the funding organisation itself.

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

In all examples above, grant numbers and names may sometimes only be provided in an in-text mention, or as string-type textual metadata. This ambiguity may be done away with by creating a resolvable **grant PIDs** for each logical grant awarded, along with a corresponding [landing page](../pid-concepts/landing-pages.md).

## _Grant_, or _project_?

Many research endeavors are heavily reliant on external funding. Funders may create targeted funding calls with specific objectives, where the grant makes up the entirety of the funding of a specific project. 

This has created a situation where it is relatively common that funders and systems may consider the **grant** entity by itself to be a **research project** entity. The practice of sometimes using research project titles to refer to awarded grants may also enforce this view. Some systems also refer to their grant numbers as **project IDs**.

However, this must be considered a dysfunctional concept that is of limited use outside the funding organisation itself, while not being interoperable with identification and description of [research projects and activities](projects-activities.md) in general. A specific research project may be funded by _several_ different grants and resources at the same time, or it may have _no_ specific external funding assigned to it at all.

Responsible identification of grants as well as their related research projects therefore requires the careful use of PIDs to identify grants as well as projects as separately adressable, well defined individual entities.

## International PIDs and identifiers

### DOI

🟢 Active  

A commonly used PID to refer to individual grants is the [DOI](../data-on-pids/doi.md) system. This will allow for providing detailed funding information on the landing page of the grant DOI, as well as funding metadata embedded in the [kernel metadata](../pid-concepts/kernel-metadata.md) payload distributed using the schema of the DOI [provider](../pid-concepts/pid-ecosystem.md#provider) in use.

Crossref DOIs are currently in wide-spread use for grant DOIs[@web-GrantsMarkupGuide], while DataCite is also providing good support for grants through its kernel metadata [@web-OpenFundingMetadata-26].

An example of a grant DOI implementation may be seen in the EU _CORDIS_ portal, which provides information on research grants funded by EU funding programmes. A grant number (here: _grant agreement ID_) is created, f.e. `101132777`. This will also be assigned a Crossref DOI for the grant, `10.3030/101132777`. A landing page describing the context of the grant will then be accessible at: <https://doi.org/10.3030/101132777>

When examining the kernel metadata for the grant DOI at <https://api.crossref.org/works/doi/10.3030/101132777>, we can see that rich machine-readable information about the grant is available, such as the size of the grant in EUR, or the identity of the funder expressed with a PID.


## Swedish national level identifiers and data sources

### Swecris _Project-ID_

🟢 Active  

The Swedish grant index [Swecris](https://www.vr.se/swecris/) is maintained and provided by the Swedish Research Council since 2016. 

Swecris lists information on grants awarded by some of the larger governmental research funders in Sweden (f.e. Formas, Forte, Riksbankens Jubileumsfond, Vinnova and the SRC itself), as well as several others.

While providing basic metadata about the awarded grant, it also provides certain grant number (here called: **Project-ID**) harmonisation and collision prevention. For example, an older Vinnova grant with the internal Vinnova grant number `2010-02635` has been indexed as `2010-02635_Vinnova` in Swecris . The corresponding entry may be accessed at: <https://www.vr.se/english/swecris.html#/project/2010-02635_Vinnova>

Swecris also provides [API-level access](https://www.vr.se/swecris/swecris-api.html) to the metadata of all grants indexed by the system, where they may be retrieved using their respective grant numbers. However, the Swecris system provides no resolvable PIDs for grants. 

When using the API, some related PIDs may be extracted, such as [ORCID](../data-on-pids/orcid.md) for the _Principal Investigator_ if available.

### GDP API

🟢 Active  

The [GDP project](https://gdphub.se) (_Gemensamma data-projektet_) is an attempt by Vinnova, Forte, Formas and the Swedish Research Council to create a Swedish standard for disseminating metadata on research grants, grant applications and funding calls through a REST API. This API may then be implemented by individual Swedish research funding organisations.

Read access to the APIs requires registration through the coordinating portal [GDPHub.se](https://gdphub.se).

At the moment, the grant data retrievable using the APIs do not include any PIDs. The grants are indexed using their internal grant numbers (diarienummer), such as `2026-01990`, while funders and research principals are identified by their corresponding [Swedish organisation numbers (organisationsnummer)](organisations.md#swedish-organisation-number-organisationsnummer), such as `202100-3153`.