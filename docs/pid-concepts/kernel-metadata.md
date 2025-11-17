# Kernel metadata

_Last updated: 2025-11-17_

The main task of persistent identifiers is to act as robust links and references to digital objects that will always work. The target of the link can be maintained over time even though the target moves or migrates to other infrastructures.

However, the ability to maintain elaborate metadata about the object _within the PID system itself_ is an important distinction when classifying PIDs.

## Basic PID (no kernel metadata)
The simplest PID systems will only handle the redirection job through a PID resolver, but nothing more. The PID will point to a link target in the form of another URL. This URL can be updated if the digital object that the PID is targeting has moved. Examples of basic PID systems working like this are the [Handle](../data-on-pids/handle.md) or [URN:NBN](../data-on-pids/nbn.md) systems.

## PIDs with kernel metadata
In addition to redirection services, more advanced PID systems enable the specification of detailed information in a core or _kernel_ of metadata content that is associated with each individual persistent identifier. This kernel metadata package is stored by the PID service itself. This information may be accessed independently of any information provided by the linked/targeted digital object, through communicating with the PID service.

Kernel metadata may consist of various information such as titles, resource types, authors, affiliations or other relationships to digital objects, phenomena or concepts. The possible contents of the kernel metadata depends on the scope of the PID. Constraints on formats and standards may apply, and the provision of certain kernel metadata may be mandatory. The PID system will have adopted a metadata schema providing the rules for how to create kernel metadata.

Kernel metadata may be reused for various purposes, from simple tasks like generating references to complex operations such as creating scientific knowledge graphs through analysis of PID interrelations. High quality kernel metadata is important for interoperable and reusable open research information.

An example of a common PID system providing kernel metadata is the [DOI](../data-on-pids/doi.md) system.