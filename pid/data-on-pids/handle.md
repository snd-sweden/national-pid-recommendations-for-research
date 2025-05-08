# Handle

_Last updated: 2025-05-08_

The Handle System is a basic PID infrastructure that may be used to create PIDs called _handles_ to refer to generic digital objects, including but not limited to documents, web pages, file archives, structured metadata, etc. Each handle is made up of a numeric prefix and a unique suffix. The handle itself is not designed to contain metadata describing the nature of the object, since its primary purpose is to serve as a transparent link redirecting the user to the target object.

The Handle System is run as a decentralised infrastructure, with locally hosted _Local Handle Services_ being able to create new handles. They are coordinated by the _Global Handle Registry_ administered by the DONA Foundation, which keeps track of handle prefixes. Registering a prefix comes with a yearly fee.

Many infrastructures build upon the Handle System, including several other PID systems. Examples of PIDs built on top of the Handle infrastructure include [DOI](doi.md) and ePIC. This is enabled by infrastructures being accredited as multi-primary administrators for a Handle implementation, making rich customisation possible.

## Where to get started as a Swedish organisation?
| Use case                                    | Contact                        | URL |
| --------                                    | -------                        | -------                          |
| Setting up a Handle-based infrastructure    | Handle.net Registry            | <https://handle.net/prefix.html> |

## PID Parameters
| Parameter                                                                               | Value                                       | Details |
| --------                                                                                | -------                                     | ------- |
| Full name                                                                               | **Handle, Handle System**                   ||
| Intended use                                                                            | **Generic digital objects**                 | Any digital object accessible with an URI |
| Example                                                                                 | **20.1000/105**                             ||
| Example with resolver                                                                   | <http://hdl.handle.net/20.1000/105>         ||
| Case sensitive                                                                          | **Yes (default)**                           | Implementation dependent |
| General resolver                                                                        | <http://hdl.handle.net>                     ||
| May use custom resolver                                                                 | **Yes**                                     | As part of a _Local Handle Service_ |
| Accompanying metadata                                                                   | **No**                                      | Metadata should be delivered by the handle target if needed |
| Inception                                                                               | **1994**                                    ||
| Standard                                                                                | **RFC 3650**                                | <https://doi.org/10.17487%2FRFC3650> |
| Standard                                                                                | **RFC 3651**                                | <https://doi.org/10.17487%2FRFC3651> |
| Standard                                                                                | **RFC 3652**                                | <https://doi.org/10.17487%2FRFC3652> |
| Documentation                                                                           | **Handle.net Documentation**                | <https://handle.net/hnr_documentation.html> |
| Wikipedia article                                                                       | **Handle System**                           | <https://en.wikipedia.org/wiki/Handle_System> |
| Wikidata Q-ID                                                                           | **Q3126718**                                | <https://www.wikidata.org/wiki/Q3126718> |
| Wikidata P-ID                                                                           | **P1184**                                   | <https://www.wikidata.org/wiki/Property:P1184> |

## PID Ecosystem
| Component                                                                                         | Name                              | URL                           |
| --------                                                                                          | -------                           | -------                       |
| [PID Scheme](../pid-concepts/pid-ecosystem.md#scheme)                                             | **Handle System**                 | <https://www.handle.net/>     |
| [PID Authority](../pid-concepts/pid-ecosystem.md#authority)                                       | **DONA Foundation**               | <https://www.dona.net/>       |
| [PID Standards Body](../pid-concepts/pid-ecosystem.md#standards-body)                             | **RFC-based** (Internet Engineering Task Force, Corporation for National Research Initiatives) | <https://rfc-editor.org/> <https://www.cnri.reston.va.us/>          |
| [PID Multi-Primary Administrator](../pid-concepts/pid-ecosystem.md#multi-primary-administrator)   | (Implementation dependent)        ||
| [PID Provider](../pid-concepts/pid-ecosystem.md#provider)                                         | (Implementation dependent)        ||
| [PID Manager](../pid-concepts/pid-ecosystem.md#manager)                                           | (Implementation dependent)        ||

