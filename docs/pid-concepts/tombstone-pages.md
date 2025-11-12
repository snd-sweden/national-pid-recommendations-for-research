# Tombstone pages

_Last updated: 2025-11-12_

Persistent identifiers are intended to act as permanent references to resources such as digital objects. Even so, in some cases digital objects are not supposed to be accessible anymore. This may f.e. be a document that has been actively retracted.  

In a PID-less workflow, this may lead to non-working references and links, or what is commonly known as [link rot](https://en.wikipedia.org/wiki/Link_rot).

When using PIDs, the best practice for handling retraction and removal of a PID target is to let the user following the PID land at a specific type of [landing page](landing-pages.md) commonly called a **tombstone page**[@web-BestPracticesTombstone-23]. This will enable the functional use of the PID beyond the lifespan of the information it is pointing to, and make sure that users as well as automated services are able to investigate any existing references to the PID target and understand what has happened to it.

The tombstone page should provide information on what digital object was available, when it was removed and the reason for doing so. It should provide details on any resource substituting or replacing it and where it may be reached. It may also provide details on the authority responsible for the removal, and where questions about the removed object should be directed. The tombstone information should be provided as human readable metadata as well as machine-readable metadata. 

If possible, it is also good practice to signal the removal of the object using the HTTP response and header from the actual web server delivering the PID target. Using currently available web standards, this would mean sending a response with the status code `HTTP 410 (Gone)`[@rep-HTTPSemantics-22] as well as providing the tombstone page with the header metadata as a resource tagged with `rel="sunset"`.[@rep-SunsetHTTP-19]