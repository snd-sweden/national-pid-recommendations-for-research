# National Bibliography Number (URN:NBN)

[NBN (National Bibliography Number)](https://en.wikipedia.org/wiki/National_Bibliography_Number) is a generic PID for digital publications. 
It uses the [URN scheme](https://en.wikipedia.org/wiki/Uniform_Resource_Name) and is therefore commonly referred to as **URN:NBN**.

The the National Library of Sweden (KB) provides registration services for Swedish organisations in the `urn:nbn:se` namespace.

## Where to get started as a Swedish organisation?
| Use case                                                                   | Contact                           | URL |
| --------                                                                   | -------                           | -------                                    |
| Read about the Swedish national URN:NBN service   | National Library: URN:NBN service information       | <https://www.kb.se/isbn-och-utgivning/urnnbn.html>        |
| Request a new organisational namespace for the Swedish national URN:NBN service   | National Library: URN:NBN service contact e-mail    | [e-plikt@kb.se](mailto:e-plikt@kb.se)        |

## PID Parameters
| Parameter                                                                               | Value                                   | Details |
| --------                                                                                | -------                                 | ------- |
| Full name                                                                               | **National Bibliography Number**   ||
| Abbreviated name                                                                        | **NBN, URN:NBN**                         ||
| Intended use                                                                            | **Publications and certain other digital objects**              | Articles, reports, theses, student essays etc. Acts as a fallback identifier for publications which did not receive another primary identifier from a publisher or infrastructure. |
| Based on other PID system(s)                                                            | **No**                                  ||
| Example                                                                                 | **urn:nbn:se:lnu:diva-80554**                           ||
| Example with resolver #1                                                                  | <https://urn.kb.se/resolve?urn=urn%3Anbn%3Ase%3Alnu%3Adiva-80554>             | <https://urn.kb.se/> is the national resolver for the Swedish `urn:nbn:se` namespace. |
| Example with resolver #2                                                                  | <https://nbn-resolving.org/urn:nbn:se:lnu:diva-80554>             ||
| Case sensitive                                                                          | **No**                                 | While not being case sensitive by design, lower case is expected in practical use to avoid confusion. |
| General resolver                                                                        | <http://nbn-resolving.org>                      | If not in the `urn:nbn:de` or `urn:nbn:ch` namespaces, this general resolver only _redirects_ requests to other national resolvers. If a resolver is down, this might fail. |
| May use custom resolver                                                                 | **Yes, mandatory**  | The infrastructure is based on national resolvers serving their respective namespaces. |
| Accompanying metadata kernel                                                            | **No**                                 |  |
| Inception                                                                               | **2001**                                ||
| Standard                                                                                | **RFC 8458**                                  | <https://datatracker.ietf.org/doc/html/rfc8458> |
| Standard                                                                                | **RFC 3188**                                  | <https://datatracker.ietf.org/doc/html/rfc3188> |
| Documentation                                                                           | **URN-Service - Dokumentation**                   | <https://wiki.dnb.de/display/URNSERVDOK/URN-Resolver+API> (in German) |
| Wikipedia article                                                                       | **National Bibliography Number**      | <https://en.wikipedia.org/wiki/National_Bibliography_Number> |
| Wikidata Q-ID                                                                           | **Q3873059**                           | <https://www.wikidata.org/wiki/Q3873059> |
| Wikidata P-ID                                                                           | **P4109**                               | <https://www.wikidata.org/wiki/Property:P4109> |

## PID Ecosystem
| Component                                                                                         | Name                              | URL                                       |
| --------                                                                                          | -------                           | -------                                   |
| [PID Scheme](../pid-concepts/pid-ecosystem.md#scheme)                                             | **URN:NBN**                | <https://datatracker.ietf.org/doc/html/rfc8458>   |
| [PID Authority](../pid-concepts/pid-ecosystem.md#authority)                                       | **RFC-based** (Internet Engineering Task Force)           | <https://rfc-editor.org/>       |
| [PID Standards Body](../pid-concepts/pid-ecosystem.md#standards-body)                             | **RFC-based** (Internet Engineering Task Force) | <https://rfc-editor.org/>       |
| [PID Provider](../pid-concepts/pid-ecosystem.md#provider)                                         | (National namespace providers. In Sweden: the National Library (KB)) |                      |
| [PID Manager](../pid-concepts/pid-ecosystem.md#manager)                                           | (Handled by organisations within each sub-namespace)  | |
