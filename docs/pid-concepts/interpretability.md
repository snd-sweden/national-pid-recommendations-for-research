# Interpretability

_Last updated: 2026-01-28_

An important aspect of persistent identifiers is the sources of information that enable interpretation of PIDs by various actors and functions. In many PID systems, there are various layers of interpretability.

## Structure and semantics

The **structure** of the identifier itself may carry meaning that can be interpreted. This is usually the case at least for PIDs employing a prefix-suffix structure, where the prefix may be associated with a certain scope or organisational entity.
Some PID users also encode information within other parts of the PID, such as expressing a hierarchical relation or mirroring some other identifier or metadata, such as an ISBN or journal volume, issue and article numbers.

However, the discourse on PID methodologies has generally been taking a restrictive stance when it comes to encoding excessive information within the structure of the PID itself. Encoding static information in such a manner may be counterproductive, since PIDs are meant to be able to provide flexibility when underlying infrastructure, hierarchies or governing bodies change. 

Therefore, it is often considered being more future-proof to use randomly generated strings for the unique parts of the PID structure, while encoding the core information about the digital object in the accompanying PID metadata.

## Resolving the PID

The [resolvability](resolvability.md) of a PID is usually ensured by an open online resolver service, although there may be exceptions to this.

The resolver helps interpreting the PID contents through redirecting the request to the digital object targeted by the PID, as well as providing a means of access to related metadata.

## Interpreting PID metadata

Several PID systems carry metadata embedded within the PID infrastructure itself, where unique metadata is stored for each PID. This is commonly referred to as [kernel metadata](kernel-metadata.md). This kind of metadata will be available as a separate entity for interpretation, alongside the target digital object that the PID is redirecting the user to when following a link.

Kernel metadata may be accessed through different means, such as using HTTP content negotiation to request a metadata representation of the PID. This may f.e. be a JSON text object with structured metadata describing the target object, that may be parsed and interpreted by humans or software. 

## Interpreting the target object

### Header metadata

While the PID system itself may include information in the HTTP headers, the target object may also do so. This may include interpretable metadata on available delivery formats as well as provenance and licensing.

### Landing page

The target object will most often provide human readable metadata for interpretation, ideally in the form of a [landing page](landing-pages.md) describing the digital object. This may be providing further context and documentation. It may also contain _embedded_ metadata that is not visually rendered but may be interpreted by parsing metadata tags.

### Payloads of the target object

The payload delivered by the PID target is one or more representations of the digital object, most often in the form of a file. This may include download links of the payload in one or more formats. If multiple formats are available, they may also be selectable through HTTP content negotiation, allowing both manual and automatic interpretation of what is offered.

Simpler implementations of PIDs may lack landing pages, immediately redirecting the user to a single file download of the payload.

It should also be noted that the goal of many PID systems is to specifically _deliver structured metadata_ as digital objects and payloads to be interpreted. Examples of such target objects include metadata files with formal definitions of individuals, organisations, geographical features, keywords, units or instruments.

### Concept PIDs

If the PID is a [concept PID](concept-pids.md), the landing page and payload may be a representation of the hierarchical subdivisions and other objects referred to by the concept PID, clarifying their relations and providing access to them for end users.