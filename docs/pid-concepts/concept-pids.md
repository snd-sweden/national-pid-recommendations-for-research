# Concept PIDs

_Last updated: 2025-11-17_

While an important feature of persistent identifiers is addressability of unique objects, there is also a need to express how objects with PIDs _belong together_. For this purpose, the idea of a _concept PID_ has been introduced. The concept PID (or _canonical_ PID), is by itself a unique PID, but will in turn also enable the _grouping_ of other PIDs as subordinate or child objects.

The concept PID may for example direct the user to a _collection_ of objects. The perhaps most common example of this is to provide a way to refer to _all available versions_ of the conceptual digital object.

For example, publishing a report expressed in PDF format may be the specific context assigned a concept PID. The report will take the shape of various manifestations over time, such as version 1.0, 1.1 and 1.2 of the report as unique PDF files. These will all be assigned individual PIDs, but retain their connection to the concept PID, which acts as a parent.

A less common use of concept PIDs is arbitrary groupings of subordinate PIDs, such as a collection of related outputs or samples.

Most often, the relation between a concept PID and the subordinate PIDs is created through PID metadata expressing formal relations to all the related PIDs, such as PIDs for every version of a digital object. The concept PID should ideally point to some sort of [landing page](landing-pages.md) with an overview of the individual objects and their unique PIDs.

PID systems employing concept PIDs usually create concept PIDs even though there may only be one subordinate PID available (f.e. when only one version of a digital object has been published). This is done to create an reliable infrastructure where the concept PID may be used as a reference that always will provide information on where the latest version may be reached.