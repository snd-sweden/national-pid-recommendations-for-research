# Instruments and research resources

_Last updated: 2026-09-28_

These recommendations concern the identification of physical instruments, research resources such as reagents and core facilities, and objects held in collections. Conceptual instruments, such as questionnaires and protocols, are covered in [Methods, protocols and study preregistrations](methods.md). For the scope of the scope-specific recommendations and how PID systems are preferred, see [Scope-specific recommendations](index.md).

## Identify instruments with DOIs and PIDINST metadata

_Applies to: research infrastructures, core facilities, organisations owning instruments and repositories._

!!! quote ""

    Identify individual instruments with DataCite DOIs using the resource type Instrument and metadata following the PIDINST schema, or with ePIC PIDs with PIDINST metadata where this fits the infrastructure. Link data to the instruments that produced it, and instruments to the research activities that made use of them.

??? question "Why?"

    Knowing which instrument produced a result is important for provenance, reproducibility and comparison of results. Individual instruments differ in configuration, calibration and maintenance history, so it matters whether an instrument model or a unique instrument is identified.

    PIDINST is a community-developed metadata model for instruments, describing owners, manufacturers, models, instrument types, measured variables, serial numbers, relations to other resources and the history of the instrument. Registered metadata makes each instrument a node in the PID graph: datasets can refer to the instrument that collected them, and organisations can follow which outputs an instrument has contributed to.

??? info "How?"

    - Decide whether a generic instrument model or a unique instrument is being identified. Use RRIDs for models and core facilities where this is established practice, and DOIs or ePIC PIDs with PIDINST metadata for unique instruments.
    - Register instrument DOIs through a service supporting PIDINST or through the Swedish DataCite consortium, and identify the owner with its ROR ID and the manufacturer with a PID where one exists.
    - Record calibrations, upgrades and other significant changes in the metadata or in linked records.
    - Relate datasets to the instruments that collected them in their DataCite metadata, and cite instrument PIDs in methods sections.

See also: [Instruments](../../landscape-analysis/instruments.md) · [DOI](../../data-on-pids/doi.md) · [ePIC](../../data-on-pids/epic.md) · [RRID](../../data-on-pids/rrid.md)

## Use RRIDs for research resources where they are established practice

_Applies to: researchers, publishers and core facilities._

!!! quote ""

    Use RRIDs to identify antibodies, cell lines, organisms, plasmids, tools and core facilities in methods sections and structured metadata, where the resource is within an RRID subtype and this is established practice in the discipline.

??? question "Why?"

    Research resources such as reagents and model organisms are often described inconsistently, which makes it hard to know exactly what was used. RRIDs give such resources precise identifiers that are widely used in the life sciences and requested by many journals. RRIDs do not have kernel metadata of their own, but they refer to records in curated registries, and they become part of the wider PID graph when they are linked from the metadata of publications and data.

??? info "How?"

    - Record the exact RRID in methods sections and resource tables, preferably in resolvable form.
    - Register new resources in the relevant RRID registry.
    - Distinguish a core facility identified with an RRID from its parent organisation identified with a ROR ID.
    - Distinguish the resource itself from publications or datasets about it, which may have DOIs, and link the identifiers.

See also: [RRID](../../data-on-pids/rrid.md) · [Research infrastructures](../../landscape-analysis/research-infrastructures.md) · [Instruments](../../landscape-analysis/instruments.md)

## Reuse the PIDs of collection-holding institutions

_Applies to: researchers, museums, archives, libraries and research infrastructures._

!!! quote ""

    When research concerns objects in museum, archive or library collections, identify them with the PIDs or persistent URIs assigned by the institution that holds the collection, and link to them from research metadata.

??? question "Why?"

    The institution that holds a collection is the natural authority for identifying and describing its objects. Reusing its identifiers avoids parallel identifiers for the same object and connects research outputs to the institution's own descriptions. Collection-holding institutions may use ARK, Handles or HTTP URIs with linked data descriptions for this purpose, but many non-PID identifiers are often in use.

??? info "How?"

    - Use the PIDs or persistent URIs of the holding institution when referring to collection objects in publications and metadata.
    - Record collection object identifiers as related identifiers in the kernel metadata of related data and publications.
    - Relate digitised representations of an object, which may have PIDs of their own, to the PID of the object itself.
    - As an institution creating PIDs for collection objects, consider ARK, or HTTP URIs following the Digg profile (see [Follow the Digg profile if you create your own PID system](../generic/choosing.md#follow-the-digg-profile-if-you-create-your-own-pid-system)), and provide linked data descriptions of the objects.

See also: [Publications](../../landscape-analysis/publications.md) · [ARK](../../data-on-pids/ark.md)
