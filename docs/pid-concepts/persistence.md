# Persistence

_Last updated: 2025-11-17_

Persistence is, as might be expected, a core concept of persistent identifiers.

Persistence means that the PID will always be resolveable and point to a digital object, even though that object may move to different hosting solutions during its lifecycle.
For example, a journal article may move to another content management system, or a government document may move to another web server, but the PID for each object would still remain and be usable as a link, redirecting the user to the current target URL of the object.

This also means that providing the PID will always be the best option when citing or providing a reference to the digital object.

Persistence also involves a commitment to use a specific PID for a specific object, and avoiding arbitrary creation of other PIDs for the same object within the same PID system in the future.

Persistence may also be seen as a promise to govern the long-term accessibility of the digital object by the entity in charge of publishing it, making sure that a valid target URL, i.e. for a [landing page](landing-pages.md), and correct PID metadata is kept maintained. This should be maintained by the [PID Manager](pid-ecosystem.md#manager).

If a decision that the digital object should no longer be available is made, it is considered good practice to provide a [tombstone page](tombstone-pages.md) in place of the removed object, accessible through the PID. A tombstone page may contain metadata and information about when and why the object was withdrawn, if any other object has replaced it, etc.

Persistence is also closely related to the concept of [uniqueness](uniqueness.md), ensuring that existing PIDs will not be reused for different digital objects, so that references will not break or refer to different content over time.
