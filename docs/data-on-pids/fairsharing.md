# FAIRsharing

_Last updated: 2026-08-23_

[FAIRsharing](https://fairsharing.org/) is an international catalog and data source providing curated definition records and metadata on three main entity types:

* Standards (f.e. file formats, metadata schemas, ISO standards)
* Databases (f.e. genomic databases, data repositories)
* Policies (f.e. reporting protocols, publishing guidelines)

FAIRsharing uses DataCite [DOI](doi.md) and is technically not a PID system by itself, but it is relevant to describe as a specifically scoped PID-based data source for research.

## Where to get started as a Swedish organisation?
| Use case                             | Contact                        | URL |
| --------                             | -------                        | -------                        |
| Create a new record of a standard, database or policy  | Adding content in FAIRsharing | <https://fairsharing.org/new> |
| Curate an existing record      | Request ownership of the record in the Actions menu                       | <https://fairsharing.gitbook.io/fairsharing/record-sections-and-fields/how-to-update-a-record> |

## PID Parameters
| Parameter                                                                               | Value                                   | Details |
| --------                                                                                | -------                                 | ------- |
| Full name                                                                               | **FAIRsharing DOI**           ||
| Intended [scope](../pid-concepts/usage-scope.md) / PID target(s)                        | **Standards, databases and policies**             |  |
| Based on other PID system(s)                                                            | **[Handle System](handle.md)**                   ||
| Handle namespace                                                                        | **10.25504**                                  ||
| Example                                                                                 | **10.25504/FAIRsharing.WWI10U**                    ||
| Example with resolver                                                                   | <https://doi.org/10.25504/FAIRsharing.WWI10U>      ||
| Case sensitive                                                                          | **No**                                  ||
| General resolver #1                                                                     | <https://doi.org/>                      ||
| General resolver #2                                                                     | <https://dx.doi.org/>                   ||
| May use custom resolver                                                                 | **Yes**                                 | Theoretically, but not implemented. |
| Accompanying [metadata kernel](../pid-concepts/kernel-metadata.md)                      | **Yes**                                 | Uses _DataCite Metadata Schema_. |
| Inception                                                                               | **2009**                                ||
| Standard                                                                                | **ISO 26324**                           | <https://www.iso.org/obp/ui/#iso:std:iso:26324> |
| Documentation                                                                           | **Getting Started with FAIRsharing**    | <https://fairsharing.gitbook.io/fairsharing> |
| Kernel metadata schema                                                                  | **DataCite Metadata Schema**            | <https://schema.datacite.org> |


## PID Ecosystem
| Component                                                                                         | Name                              | URL                           |
| --------                                                                                          | -------                           | -------                       |
| [PID Scheme](../pid-concepts/pid-ecosystem.md#scheme)                                             | **[Handle System](handle.md)**                 | <https://www.handle.net/>     |
| [PID Authority](../pid-concepts/pid-ecosystem.md#authority)                                       | **DONA Foundation**               | <https://www.dona.net/>       |
| [PID Standards Body](../pid-concepts/pid-ecosystem.md#standards-body)                             | **International Organization for Standardization** (ISO)  | <https://www.iso.org/>          |
| [PID Multi-Primary Administrator](../pid-concepts/pid-ecosystem.md#multi-primary-administrator)   | **International DOI Foundation**  | <https://www.doi.org/>        |
| [PID Provider](../pid-concepts/pid-ecosystem.md#provider)                                         | **DataCite**                      | <https://datacite.org/>       |
| [PID Manager](../pid-concepts/pid-ecosystem.md#manager)                                           | The FAIRsharing team, University of Oxford                        | <https://fairsharing.org/communities#governance> |
| [PID Manager](../pid-concepts/pid-ecosystem.md#manager)                                           | (Individual record maintainers)                          ||

