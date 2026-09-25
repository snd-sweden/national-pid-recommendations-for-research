# Instruments

_Last updated: 2026-09-25_

When using a broad definition, research instruments may be considered being resources that are used to observe, elicit, measure, record, transform, or structure the production of research evidence. Therefore, instruments used in research are manifested as several types of objects and concepts that need identification. 

## Physical instruments

Physical research instruments are tangible devices, equipment, or platforms such as microscopes, spectrometers, sensors, laboratory equipment, telescopes, and field-monitoring devices. Individual instruments may differ in configuration, calibration, maintenance history, and operating conditions.

Larger and more complex physical research instruments may even be classified as [research infrastructures](research-infrastructures.md), or directly provided by them.

Identifying physical instruments and the setup used is especially relevant to record research provenance and enable reproducibility and comparability.

When identifying a physical instrument, it is important to distinguish if a **generic model/type** of instrument is being identified, or if a **unique instance** of the instrument is being pointed out. Both are valid cases for identification and provenance. For example, unique instances of instruments may have known defects or variations.

## Conceptual instruments

Conceptual research instruments are structured intellectual or methodological resources, such as published questionnaires, psychometric scales, interview guides, observation protocols, assessment instruments, coding schemes, and survey designs. Actual use cases in different research disciplines may refer to conceptual instruments in various ways, i.e. _data collection instrument_, _methodological instrument_, _protocol_, _guide_, _scheme_, etc. Like physical instruments, they can exist in different versions, translations, adaptations, and configurations that may materially affect the resulting data, and have a clear need for identification. 

The scope of conceptual research instruments does not always align with the [conceptual coverage](../pid-concepts/coverage.md) of a specific PID system. A conceptual research instrument may for example in some cases be treated as a [publication](publications.md), be implemented as [research software](software-models.md), or be embedded in a [preregistration](preregistrations.md). Formal workflows and protocols are often treated as unique digital objects.

## PIDs for physical instruments

### RRID

🟢 Active

Within the [RRID](../data-on-pids/rrid.md) (Research Resource Identifier) system, various subtypes of research resources may be identified. The RRID _Core facility or Instrument_ subtype may be used to identify a **generic model/type** of instrument. The RRID system is mainly used within the life sciences and the physical sciences.

The [SciCrunch Registry](https://scicrunch.org/) serves as the authority for the `SCR_` class that includes instruments and core facilities. [ABRF CoreMarketplace](https://coremarketplace.org) registers both, and interlinks them to keep track of instruments available at a specific facility.

**Example:** The _Zeiss LSM 980 with Airyscan 2 Microscope_ has been assigned the RRID short identifier `RRID:SCR_025048`. It may be resolved using: <https://identifiers.org/RRID:SCR_025048>  
In the SciCrunch entry, additional metadata on specifications are available along with vendor documentation and related facilities.

### PIDINST (DOI or ePIC PID)

🟢 Active

[PIDINST](https://www.pidinst.org/) (Persistent Identification of Instruments) is an identifier for **unique instances** of physical instruments. PIDINST is best understood as a community-developed metadata model and set of recommendations, rather than a separate PID infrastructure or identifier namespace.

The [PIDINST Metadata Schema](https://doi.org/10.15497/RDA00070) describes properties such as instrument name, owner/operator, manufacturer, model, instrument type, measured variables, dates, alternate identifiers such as serial numbers, and relationships to other resources. It may hold a technical record of how the instrument has been used over time.

PIDINST may be used through assigning an instrument a [DataCite DOI](../data-on-pids/doi.md), using **Instrument** as its general resource type. PIDINST may also be used with [ePIC PID](../data-on-pids/epic.md) through [B2INST](https://b2inst.pid.gwdg.de), where the instrument receives an ePIC Handle with PIDINST metadata stored alongside it.

**Example**: A specific _HMP155 humidity and temperature sensor_ manufactured by Vaisala is owned by the _Karlsruhe Institute of Technology (KIT)_. Using ePIC PID with PIDINST, `21.11157/6a91284a-0316-4268-954d-07807f110b83` has been assigned by KIT through B2INST for this unique instance of sensor. The ePIC Handle may be resolved at: <http://hdl.handle.net/21.11157/6a91284a-0316-4268-954d-07807f110b83>

This resolves to a B2INST landing page for the instrument, where PIDINST metadata are available, such as `S3070055 2020`, the serial number of the sensor, and a reference to an Atmohub Sensor Management System entry for the same unique sensor.

**Example**: The _DTU Space_ insititute at the Technical University of Denmark owns a _iNAT-RQH-4001 inertial measurement unit / strapdown gravimeter_ manufactured by iMAR Navigation. It has been assigned a DataCite DOI with PIDINST metadata, `10.11583/DTU.25673604`. This may be resolved at: <https://doi.org/10.11583/DTU.25673604>

The DOI resolves to a local DTU repository which supports PIDINST. Metadata such as the serial number `iNAT-RQH-0001` and the technical record of the instrument with hardware upgrades and specific research field campaigns are available in the record. There are also file attachments such as photographs of the instrument and vendor datasheets.

## PIDs for conceptual instruments

### DOI

🟢 Active

[DOI](../data-on-pids/doi.md) is a common identifier for conceptual instruments such as established questionnaires, protocols, interview guides and similar materials. DataCite DOIs and Crossref DOIs are both frequently used for identification of them.

Since conceptual instruments come in many forms, they may be described and referred to in several different ways. In some cases they may look similar to a standard publication. This results in non-uniform metadata, and it is therefore not always simple to recognise an instrument from its DOI kernel metadata only, without interpretation of the meaning of titles and abstracts or reviewing how it has been referred to.

**Example:** The _Standards-Compliant General Protocol for Systematic Reviews_ is a protocol for implementing established methodology when performing systematic reviews of published research, such as the ROSES and PRISMA checklists. Three versions of the protocol has been uploaded to [protocols.io](https://www.protocols.io), a platform run by Springer Nature.

Version 3 has been assigned a Crossref DOI, `10.17504/protocols.io.n92ldydzxl5b/v3`, resolvable at: <https://doi.org/10.17504/protocols.io.n92ldydzxl5b/v3>  
The registered Crossref kernel metadata says that it is of the _type_ `posted-content`, a generic type for non-peer reviewed materials.

**Example:** _The Motivation and Pleasure Scale – Self-Report (MAP-SR)_ is a psychometric questionnaire. The specific German variant of MAP-SR has been registered in the [ZPID Open Test Archive](https://www.testarchiv.eu/). 

The latest version of it has been assigned the DataCite DOI `10.23668/psycharchives.4649`, resolving to its PsychArchives frontend: <https://doi.org/10.23668/psycharchives.4649>  
The registered DataCite kernel metadata says that it is of _resourceTypeGeneral_ `Other` and the free-form _resourceType_ `test`.

## Other identifiers for conceptual instruments

### ISBN

Conceptual instruments, especially older ones, may have been treated as regular publications and assigned an ISBN and/or an eISBN. Depending on what was published, the identifier may be assigned to the instrument itself, or a larger publication such as a manual, method chapter or supplement in which the instrument was embedded.

**Example:** The _SF-36 Health Survey_ (36-Item Short Form Health Survey) is a well-established questionnaire for measuring health status and health-related quality of life. The latest official revision of the English-language questionnaire is embedded within the second edition of its manual:

Ware, J. E., Kosinski, M., Gandek, B., & Dewey, J. E. (2000). _SF-36 Health Survey: Manual and Interpretation Guide_, 2nd ed. QualityMetric.

The only identifier that can be reliably used to refer to the official SF-36 is the revised manual ISBN: `978-1-891810-06-0`. It should be noted that specific translations and variations of the revised SF-36 questionnaire may have other identifiers, such as DOI.