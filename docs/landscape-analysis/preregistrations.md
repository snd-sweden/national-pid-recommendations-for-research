# Preregistrations

_Last updated: 2026-09-16_

A preregistration is a manner of officially announcing details such as a study designs, methods and hypotheses in advance of proceeding with other parts of the research process, such as data collection, processing and analysis. Preregistrations are meant to increase transparency and reduce the effect of biases in research[@jrnl-PreregistrationRevolution-18]. They may serve as a way of preventing research fraud, dishonest representations of how the study was performed, or the skewing of hypotheses or research questions after a certain result was reached. 

The preregistration as a concept may be considered a quite recent type of research object for identification. 

Preregistrations are more common within certain fields of research, such as medicine, where they often are created in the form of research protocol documentation. There may be strict requirements for preregistrations in certain regulated contexts, such as clinical trials and pharmaceutical studies. A specific type of preregistration is registering a clinical trial in a **clinical trials registry**, which will provide metadata on the study and an identifier for the preregistration. Full PIDs are still uncommon in this category.

Other types of preregistrations may include sharing formal methodology for the study in the form of [research software](software-models.md), or sharing dummy or synthetic examples of [research data](research-data.md), to show how data will be collected, packaged and processed. A combination of several types of accessible objects may be preregistered to ensure transparency of the ongoing research process.

Using preregistration infrastructures to register ongoing or even finished studies may be possible. Depending on the case, this may remove some of the value of preregistering a study before performing other steps of the research process.

The preregistration concept is also closely related to the novel concept of **modular publishing**, where individual components of the research process are published using an as-go-you approach, inviting early input from peers as well as collaborations[@jrnl-OpenScience20-23].

## Preregistration identifiers for clinical trials

### ClinicalTrials.gov ID

🟢 Active

The National Library of Medicine provides [ClinicalTrials.gov](https://clinicaltrials.gov), an international registry for preregistrations. ClinicalTrials.gov accepts preregistering clinical trials as well as observational studies within the scope of clinical research.

A ClinicalTrials.gov preregistration will receive a **ClinicalTrials.gov ID**, also called **NCT number** for identifying the study. The format consists of NCT followed by 8 digits, f.e. `NCT00000419`. While not a full PID, the identifier may be reliably resolved at the `https://clinicaltrials.gov/study/` endpoint, i.e.: <https://clinicaltrials.gov/study/NCT00000419>

The ClinicalTrials.gov study record provides a structure for providing versioned details on the study such as research questions/hypotheses, study designs, timing, interventions, outcome measures, participants, recruitment, output management planning and administrative details. When the study is completed, users may also create relations to published results and other outcomes from their preregistration entries. 
The possible metadata contents of a preregistration entry is detailed in the [Protocol Registration DED](https://clinicaltrials.gov/policy/protocol-definitions) and for results in the [Results DED](https://clinicaltrials.gov/policy/results-definitions). 

ClinicalTrials.gov employs a model where research organisations generally only are provided with a single account in the PRS entry system for submitting preregistrations. Therefore, researchers desiring to register their study will in most cases need to contact an individual or function serving as a local PRS Administrator for ClinicalTrials.gov.

**Example:** The study _Postprandial Inflammation in Rheumatoid Arthritis (PIRA)_ conducted at the University of Gothenburg was registered on ClinicalTrials.gov in 2020, receiving the ID `NCT04247009`. After the study finished in 2021, four related publications have been added to the entry: https://clinicaltrials.gov/study/NCT04247009

### EU CT number

🟢 Active

[CTIS](https://euclinicaltrials.eu) (Clinical Trials Information System) is the current clinical trials registry mandated by the [EU Regulation (EU) No 536/2014](http://data.europa.eu/eli/reg/2014/536/oj) (Clinical Trials Regulation) for registering trials of investigational medicinal products. It is run by the European Medicines Agency. 

A clinical trial registered in CTIS will receive a **EU CT number** following a 14-digit syntax starting with the year of registration, followed by a serial number, the application number, and the resubmission count i.e. `YYYY-NNNNNN-CC-XX`. The last four digits may sometimes be omitted when referencing the number. The clinical trial may also have an associated **protocol code**, which may be following a research organisation or sponsor standard.

Metadata in CTIS is using the CTIS Structured Data Form, deprecating the older EEA CTA XML schema. Metadata may be fetched using the CTIS Public API.

**Example:** The study _Effects of the appetite-inducing hormone ghrelin on decision making in healthy volunteers_ conducted at Linköping University was assigned the EU CT number `2024-517598-26-00` after preregistering in CTIS. The protocol code `GHREDECIDE` is associated with the preregistration. The CTIS entry may be accessed at <https://euclinicaltrials.eu/ctis-public/view/2024-517598-26-00>, with additional protocol and result files being downloadable. Accessing the API using <https://euclinicaltrials.eu/ctis-public-api/retrieve/2024-517598-26-00> provides a machine-readable representation.

### Universal Trial Number

🟢 Active

[ICTRP](https://www.who.int/tools/clinical-trials-registry-platform) (International Clinical Trials Registry Platform) is an aggregator of clinical trial preregistrations run by the World Health Organisation. It indexes clinical trials from recognised _WHO Primary Registries_, including CITS, ClinicalTrials.gov and many others, but does not serve as a platform to create new preregistrations by itself.

Clinical trials in the WHO Primary Registries picked up by ICTRP may request a **Universal Trial Number** (UTN), an identifier that facilitates disambiguation of a clinical trial across multiple registries and countries. An UTN follows a 13-character format starting with a U followed by 12 digits, f.e. `U1111-2222-3333`. However, registering a UTN is not mandatory, and clinical trials will be indexed using a primary identifier from their respective registry together with secondary identifiers if available.

**Example:** The study _Effect of Group Education and Individual Counselling on Mental Health and Quality of Life in 45-60 Year Old Women_ conducted by Region Västra Götaland was registered at ClinicalTrials.gov in 2018, receiving the ClinicalTrials.gov ID `NCT03663075`. A UTN was also registered, `U1111-1219-6542`. The ICTRP entry may f.e. be accessed using the primary identifier: <https://trialsearch.who.int/Trial2.aspx?TrialID=NCT03663075>

### EudraCT number

🔴 Inactive

[EudraCT](https://eudract.ema.europa.eu) (European Union Drug Regulating Authorities Clinical Trials Database), hosted by the European Medicines Agency, formerly served as an active registry for clinical trials of medicinal products within the EU. Registering such trials in EudraCT was required by the Clinical Trials Regulation.

Registered clinical trials in EudraCT received a **EudraCT number**, following a 12-digit syntax starting with the year of registration, followed by a serial number and a checksum, i.e. `YYYY-NNNNNN-CC`. The EudraCT entry provides a webpage with metadata which complies with the [EEA CTA schema](https://eudract.ema.europa.eu//result.html).

The EudraCT infrastructure remains for looking up preregistrations of former clinical trials initiated before 2022-01-31. New registrations are referred to the superseding EU registry, CTIS.

**Example:** The study _ITT-PMS Extension_ was registered by Umeå University in EudraCT in 2012. It received the EudraCT number: `2012-000721-53`. Searching for the number using the [ search function](https://www.clinicaltrialsregister.eu/ctr-search/search) will reveal a protocol entry at: <https://www.clinicaltrialsregister.eu/ctr-search/trial/2012-000721-53/SE> as well as a results entry at: <https://www.clinicaltrialsregister.eu/ctr-search/trial/2012-000721-53/results>

## Other preregistration identifiers

### DOI

🟢 Active

There are several platforms that will accommodate general use cases for preregistrations, such as data repositories or self-publishing services. [DOI](../data-on-pids/doi.md) is a PID commonly used for identification of preregistrations in many infrastructures.

An example of a generic infrastructure supporting preregistrations and assigning DOIs is the [Open Science Framework](https://osf.io) (OSF), provided by an NPO, the Center for Open Science (COS). It provides a basic framework and registry that may be used to publish preregistration components such as hypotheses, variables, sampling/design decisions, methodology, statistical tests, models, exclusion criteria, synthetic data, etc. Several preregistration templates for various disciplines and cases are made available. A DOI will be assigned to an OSF entry when requested by the user.

**Example:** [_Does Really One in Ten Believe Capital Punishment Exists in a Contemporary European Community Country?_](https://doi.org/10.3389/fpsyg.2019.01601) is an article published in Frontiers in Psychology in 2019. In the study, the authors attempted to replicate study results presented in another article, [_Blurred world view_](https://doi.org/10.1080/07481187.2016.1186761) from 2016. Prior to initiating the replication study, the study design with research questions, hypotheses, data collection and analysis plans was published as a preregistration using OSF. The preregistration was assigned a DOI: <https://doi.org/10.17605/OSF.IO/FEHVB>