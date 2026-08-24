# SWHID

_Last updated: 2026-08-18_

SWHID (SoftWare Hash IDentifier) is a PID system for unique identification of software artifacts, such as source code files. 

The infrastructure of the PID system will assign a SWHID and simultaneously archive a full copy of the PID target for future reference.

SWHID has been specifically designed to meet the need for identifying and preserving various types of PID targets within distributed software version control systems, such as specific versions, releases, commits or excerpts of source code.

A globally available SWHID minting and archival service is provided by the Software Heritage Archive, although anyone may set up their own SWHID service.

## Where to get started as a Swedish organisation?
| Use case                                                                   | Contact                           | URL |
| --------                                                                   | -------                           | -------                                                                         |
| Deposit source code and create a SWHID                                     | Save code now                     | <https://archive.softwareheritage.org/save/>                                    |
| Automate the creation of SWHIDs through the Deposit API                    | Register account                  | <https://docs.softwareheritage.org/devel/swh-deposit/api/register-account.html> |

## PID Parameters
| Parameter                                                                               | Value                                   | Details |
| --------                                                                                | -------                                 | ------- |
| Full name                                                                               | **SoftWare Hash IDentifier**            ||
| Abbreviated name                                                                        | **SWHID**                               ||
| Intended [scope](../pid-concepts/usage-scope.md) / PID target(s)                        | **Software artifacts**                  | Source code, repositories, releases, commits, gists etc. |
| Based on other PID system(s)                                                            | **No**                                  ||
| Example                                                                                 | **swh:1:dir:df32c75242bf8d797ccd43af8ce8e294f35cd8fd** {: colspan=2 } ||
| Example with resolver                                                                   | [https://archive.softwareheritage.org/swh:1:dir:df32c75242bf8d797ccd43af8ce8e294f35cd8fd](https://archive.softwareheritage.org/swh:1:dir:df32c75242bf8d797ccd43af8ce8e294f35cd8fd) {: colspan=2 }||
| Case sensitive                                                                          | **Partially**                           | Core identifier uses case-insensitive hexadecimal notation, but some use cases may embed file names |
| General resolver                                                                        | <https://archive.softwareheritage.org/> ||
| May use custom resolver                                                                 | **Yes**                                 | Supports creation of independently hosted instances of the SWHID infrastructure. |
| Accompanying [metadata kernel](../pid-concepts/kernel-metadata.md)                      | **Yes**                                 | As described in the SWHID specification |
| Inception                                                                               | **2018**                                ||
| Standard                                                                                | **ISO/IEC 18670**                       | <https://www.iso.org/obp/ui/en/#iso:std:89985> |
| Documentation                                                                           | **SWHID Specification**                 | <https://www.swhid.org/swhid-specification/latest/> |
| Documentation                                                                           | **Software Heritage Documentation**     | <https://docs.softwareheritage.org> |
| Kernel metadata schema                                                                  | **SWHID Syntax**                        | <https://docs.softwareheritage.org/devel/swh-model/persistent-identifiers.html> |
| Wikipedia article                                                                       | **SoftWare Hash IDentifier**            | <https://en.wikipedia.org/wiki/SoftWare_Hash_IDentifier> |
| Wikidata Q-ID                                                                           | **Q134567344**                          | <https://www.wikidata.org/wiki/Q134567344> |
| Wikidata P-ID                                                                           | **P6138**                               | <https://www.wikidata.org/wiki/Property:P6138> |

## PID Ecosystem
| Component                                                                                         | Name                              | URL                                       |
| --------                                                                                          | -------                           | -------                                   |
| [PID Scheme](../pid-concepts/pid-ecosystem.md#scheme)                                             | **SWHID model**                   | <https://www.swhid.org/swhid-specification/latest/> |
| [PID Authority](../pid-concepts/pid-ecosystem.md#authority)                                       | **SWHID Core Team**             | <https://www.swhid.org/coreteam/>       |
| [PID Standards Body](../pid-concepts/pid-ecosystem.md#standards-body)                             | **International Organization for Standardization** (ISO)  | <https://www.iso.org/>          |
| [PID Provider](../pid-concepts/pid-ecosystem.md#provider)                                         | **Software Heritage Archive**     | <https://archive.softwareheritage.org>                         |
| [PID Manager](../pid-concepts/pid-ecosystem.md#manager)                                           | (Individuals, CI/CD staff, admins etc.) |        |