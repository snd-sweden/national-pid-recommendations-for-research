# ARK

_Last updated: 2026-08-31_

[ARK](https://arks.org) (Archival Resource Key) is a generic PID system meant for identifying a wide scope of possible PID targets. ARKs may refer to digital objects as well as physical objects, or even living beings. An ARK is most often globally resolvable.

The ARK concept provides considerable flexibility for organisations, such as running local ARK resolvers and customising the sub-namespaces and core identifier structure of the local ARK implementation after registration of a NAAN (Name Assigning Authority Number). An ARK may support qualifiers for addressing subcomponents or versions of an object, such as a single page or a specific edition. The ARK system does not hold kernel metadata, but allows for referral to implementation-specific metadata. Implementing ARK will require active maintenance of local PID infrastructure.

ARK has seen widespread use in archival organisations and cultural heritage institutions, but is not limited in scope to them. A typical use case for ARK would be creating PIDs for the official records of an organisation, or the various objects in a catalogue. The ARK system is supported by the [ARK Alliance](https://arks.org/community/), a community coordinating development and maintaining the core infrastructure. It has not yet been codified by a standard and is currently a draft for a RFC.

## Where to get started as a Swedish organisation?
| Use case                                    | Contact                        | URL |
| --------                                    | -------                        | -------                          |
| Setting up a local ARK-based infrastructure    | Apply for a NAAN for ARK   | <https://arks.org/about/getting-started-implementing-arks/> |

## PID Parameters
| Parameter                                                                               | Value                                       | Details |
| --------                                                                                | -------                                     | ------- |
| Full name                                                                               | **Archival Resource Key**                   ||
| Short name                                                                               | **ARK**                   ||
| Intended [scope](../pid-concepts/usage-scope.md) / PID target(s)                        | **Generic digital or physical objects**                 | Digital objects, physical objects, concepts, living beings. |
| Example                                                                                 | **ark:/12148/cb40766547d**                             | 12148 is a NAAN for _Bibliothèque nationale de France_ and cb40766547d a core identifier. |
| Example with resolver                                                                   | <https://n2t.net/ark:/12148/cb40766547d>         ||
| Case sensitive                                                                          | **Yes**                           | The core ID part is case sensitive. |
| General resolver                                                                        | <http://n2t.net>                     ||
| May use custom resolver                                                                 | **Yes**                                     | The ARK concept assumes and encourages the use of local resolvers. |
| Accompanying [metadata kernel](../pid-concepts/kernel-metadata.md)                      | **No**                                      | Best practices for referring to metadata exist. |
| Inception                                                                               | **2001**                                    ||
| Documentation                                                                           | **ARK Alliance: Getting started**                | <https://arks.org/about/getting-started-implementing-arks/> |
| Documentation                                                                           | **The ARK Identifier Scheme**                | <https://datatracker.ietf.org/doc/draft-kunze-ark/> |
| Wikipedia article                                                                       | **Archival Resource Key**                           | <https://en.wikipedia.org/wiki/Archival_Resource_Key> |
| Wikidata Q-ID                                                                           | **Q2860403**                                | <https://www.wikidata.org/wiki/Q2860403> |
| Wikidata P-ID                                                                           | **P8091**                                   | <https://www.wikidata.org/wiki/Property:P8091> |

## PID Ecosystem
| Component                                                                                         | Name                              | URL                           |
| --------                                                                                          | -------                           | -------                       |
| [PID Scheme](../pid-concepts/pid-ecosystem.md#scheme)                                             | **ARK System**                 | <https://datatracker.ietf.org/doc/draft-kunze-ark/>     |
| [PID Authority](../pid-concepts/pid-ecosystem.md#authority)                                       | **ARK Alliance**               | <https://www.arks.org/>       |
| [PID Standards Body](../pid-concepts/pid-ecosystem.md#standards-body)                             | **ARK Alliance WGs**  | <https://arks.org/community-groups/>          |
| [PID Provider](../pid-concepts/pid-ecosystem.md#provider)                                         | (Local implementations)        ||
| [PID Manager](../pid-concepts/pid-ecosystem.md#manager)                                           | (Local implementations)        ||

