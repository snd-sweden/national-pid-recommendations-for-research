# Uniqueness

_Last updated: 2025-06-02_

Uniqueness, as a PID concept, may be seen as a promise that the PID will remain a unique identifier. This means that the PID will not be reused to point to another digital object. This should be maintained by the [PID Manager](pid-ecosystem.md#manager).

PID uniqueness ensures that references and citations using PIDs will always refer to the digital object intended.

It should however be noted that not all PIDs refer to single objects. A special type of PID, [concept PIDs](), may in turn refer to many objects at once. The concept PID may for example direct the user to a collection of objects, or may provide a way to refer to all available versions of a digital object. Most often, this is done through PID metadata expressing [formal relations]() to all the related PIDs, such as PIDs for every version of a digital object. The concept PID should ideally point to some sort of [landing page](landing-pages.md) with an overview of the individual objects and their unique PIDs.