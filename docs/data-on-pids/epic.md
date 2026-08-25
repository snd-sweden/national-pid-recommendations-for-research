# ePIC

_Last updated: 2026-08-24_

[ePIC](https://www.pidconsortium.net/) is an international consortium and service framework for registering and resolving persistent identifiers for research resources. The service is based on the [Handle System](handle.md) and technically, an ePIC PID is a Handle. The distinguishing ePIC profile consists of consortium governance, prefix allocation, a common REST API, operational policies, monitoring, replication, and support for PID Information Types.

New ePIC prefixes are allocated in Handle namespace `21`. ePIC PIDs can be assigned to research data and other digital research objects, including intermediate, fine-grained, or workflow-related resources. This makes the service relevant when identifiers are needed before or outside formal publication.

Metadata may be stored directly in the Handle record as typed values. These values can include one or more target URLs, checksums, content types, version relations, access or embargo information, rights information, and links to richer metadata. The [ePIC Data Type Registry](https://dtr-pit.pidconsortium.net/) supports shared definitions for such PID Information Types. There is no single mandatory metadata schema applied uniformly to all ePIC prefixes; requirements depend on the service provider and the profile in use.

ePIC distinguishes production prefixes from test or non-persistent prefixes. Under ePIC policy, production PIDs cannot be deleted. If the identified object is removed, unavailable, or access-restricted, the PID should remain and provide appropriate status information or resolve to a tombstone. Persistence of the identifier therefore does not by itself guarantee continued access to the identified object; the PID manager remains responsible for maintaining target and status information.

## Where to get started as a Swedish organisation?

| Use case                                    | Contact                                                         | URL |
| --------                                    | -------                                                         | -------       
| Request an ePIC prefix                      | [Swedish National Data Service](../pid-actors-sweden/snd.md)    | [pid@snd.se](mailto:pid@snd.se) |

## PID Parameters

| Parameter                                                             | Value                                                 | Details |
| ---------                                                             | -----                                                 | ------- |
| Full name                                                             | **ePIC Persistent Identifier**                        ||
| Abbreviated name                                                      | **ePIC PID, ePIC Handle**                             ||
| Intended [scope](../pid-concepts/usage-scope.md) / PID target(s)      | **Generic digital research objects and collections**  | Particularly applicable to research data, intermediate outputs, fine-grained resources, and workflow objects. |
| Based on other PID system(s)                                          | **[Handle System](handle.md)**                        | Uses Handle infrastructure and resolution. |
| Handle namespace                                                      | **21**                                                | Used for new ePIC prefixes. Legacy ePIC prefixes in other Handle namespaces remain in use. |
| Identifier syntax                                                     | **`<prefix>/<suffix>`**                               | The suffix must be unique within its prefix. |
| Test/non-persistent prefix convention                                 | **`21.T...`**                                         | A capital `T` after the first dot marks an ePIC test or non-persistent prefix. |
| Example                                                               | **21.012/xyz-123**                                    | Illustrative example used in the ePIC FAQ. |
| Example with resolver                                                 | <https://hdl.handle.net/21.012/xyz-123>               | Illustrative example; it is not presented as a registered production PID. |
| Case sensitive                                                        | **Yes**                                               | ePIC does not apply a case-insensitivity mapping. Printable ASCII is mandatory for suffixes; using one consistent case is recommended when DOI interoperability may be relevant.  |
| General resolver                                                      | <https://hdl.handle.net/>                             ||
| May use custom resolver                                               | **Yes**                                               | Handle-compatible proxies and local resolution services may be used. |
| Accompanying [metadata kernel](../pid-concepts/kernel-metadata.md)    | **Implementation-dependent**                          | ePIC supports typed Handle values and PID Information Types stored with the PID, but it does not impose one universal kernel metadata schema across all prefixes. |
| Inception                                                             | **2009**                                              ||
| Standard                                                              | **RFC 3650**                                          | <https://doi.org/10.17487/RFC3650> |
| Standard                                                              | **RFC 3651**                                          | <https://doi.org/10.17487/RFC3651> |
| Standard                                                              | **RFC 3652**                                          | <https://doi.org/10.17487/RFC3652> |
| Documentation                                                         | **ePIC API documentation**                            | <https://doc.pidconsortium.net/> |
| Policy                                                                | **ePIC Quality of Service and Policies**              | <https://www.pidconsortium.net/?page_id=904> |
| Kernel metadata schema                                                | **PID Information Types / provider profile**          | Shared data types can be registered in the [ePIC Data Type Registry](https://dtr-pit.pidconsortium.net/). |
| Persistence policy                                                    | **Production PIDs cannot be deleted**                 | If an object is deleted or inaccessible, the PID remains and should provide metadata and appropriate status information. |

## PID Ecosystem

| Component                                                             | Name                                                                  | URL |
| ---------                                                             | ----                                                                  | --- |
| [PID Scheme](../pid-concepts/pid-ecosystem.md#scheme)                 | **[Handle System](handle.md)**                                        | <https://www.handle.net/> |
| [PID Authority](../pid-concepts/pid-ecosystem.md#authority)           | **DONA Foundation**                                                   | <https://www.dona.net/> |
| [PID Standards Body](../pid-concepts/pid-ecosystem.md#standards-body) | **RFC-based** (Internet Engineering Task Force, Corporation for National Research Initiatives) | <https://rfc-editor.org/> <https://www.cnri.reston.va.us/> |
| [PID Multi-Primary Administrator](../pid-concepts/pid-ecosystem.md#multi-primary-administrator) | **ePIC Consortium** | <https://www.pidconsortium.net> |
| [PID Provider](../pid-concepts/pid-ecosystem.md#provider)             | **ePIC member organisations and ePIC-certified service providers**    | <https://www.pidconsortium.net/?page_id=74> |
| [PID Provider for Sweden](../pid-concepts/pid-ecosystem.md#provider)  | **Swedish National Data Service**                                     | <https://snd.se/en/services/epic-pid> |
| [PID Manager](../pid-concepts/pid-ecosystem.md#manager)               | (Institutions, projects, and communities maintaining ePIC PIDs under an allocated prefix) ||

## References

- [ePIC website](https://www.pidconsortium.net/)
- [Swedish Service Provider: Swedish National Data Service](https://snd.se/tjanster/epic-pid)
- [ePIC structure and members](https://www.pidconsortium.net/?page_id=74)
- [ePIC Quality of Service and Policies](https://www.pidconsortium.net/?page_id=904)
- [ePIC frequently asked questions](https://www.pidconsortium.net/?page_id=1060)
- [ePIC API documentation](https://doc.pidconsortium.net/)
- [ePIC API v2 source and specification](https://github.com/pidconsortium/ePIC-API-v2)
- [ePIC Data Type Registry](https://dtr-pit.pidconsortium.net/)
