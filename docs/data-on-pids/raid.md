# RAiD

_Last updated: 2026-08-19_

RAiD (Research Activity Identifier) is a PID for identifying research activities, typically a research project, and sharing information about them. A RAiD may contain metadata on the outputs created within a research activity, who is performing the research, how it is funded, and many other details. 

The metadata is mainly provided through making references to other PIDs, such as ORCIDs, ROR IDs and DOIs. A RAiD may have hierarchical references to encapsulating or subordinate research activities, such as a research project being part of a research programme.

RAiD is provided by a global network of RAiD Service Points, and coordinated by the Australian Research Data Commons. The EU RAiD services is currently being set up as a part of the EOSC infrastructure.

## Where to get started as a Swedish organisation?
| Use case                                                                   | Contact                           | URL |
| --------                                                                   | -------                           | -------                                    |
| Start minting RAiDs as a Swedish organisation   | Contact SND for declaring interest | [pid@snd.se](mailto:pid@snd.se)        |
| Follow the progress of the EU RAiD infrastructure | SURF RAiD Pilot   | <https://www.surf.nl/en/services/publishing/raid>  |

## PID Parameters
| Parameter                                                                               | Value                                   | Details |
| --------                                                                                | -------                                 | ------- |
| Full name                                                                               | **Research Activity Identifier**            ||
| Abbreviated name                                                                        | **RAiD, RAiD ID**                               ||
| Intended [scope](../pid-concepts/usage-scope.md) / PID target(s)                        | **Research activities**                  | Research projects, research programmes, work packages, recurring data collection events, research assessment tasks, spontaneous collaborations etc. |
| Based on other PID system(s)                                                            | **[DOI](doi.md)**                                  | Uses DataCite DOI as an underlying component. |
| Example                                                                                 | **10.26259/0d7f1865** ||
| Example with resolver                                                                   | <https://raid.org/10.26259/0d7f1865>||
| Case sensitive                                                                          | **No**                           ||
| General resolver                                                                        | <https://raid.org/> ||
| May use custom resolver                                                                 | **Yes**                                 | In theory, but the current organisation is focusing on the global resolver. |
| Accompanying [metadata kernel](../pid-concepts/kernel-metadata.md)                      | **Yes**                                 | As described by the _RAiD Metadata Schema_. |
| Inception                                                                               | **2017**                                ||
| Standard                                                                                | **ISO 23527**                           | <https://www.iso.org/obp/ui/en/#iso:std:75931> |
| Documentation                                                                           | **RAiD Documentation**                  | <https://documentation.raid.org/raid/> |
| Kernel metadata schema                                                                  | **RAiD Metadata Schema**                | <https://metadata.raid.org/en/latest/> |
| Wikidata Q-ID                                                                           | **Q108378148**                          | <https://www.wikidata.org/wiki/Q108378148> |

## PID Ecosystem
| Component                                                                                         | Name                              | URL                                       |
| --------                                                                                          | -------                           | -------                                   |
| [PID Scheme](../pid-concepts/pid-ecosystem.md#scheme)                                             | **[Handle System](handle.md)**                 | <https://www.handle.net/>     |
| [PID Authority](../pid-concepts/pid-ecosystem.md#authority)                                       | **RAiD Registration Authority, ARDC**             | <https://ardc.edu.au>       |
| [PID Standards Body](../pid-concepts/pid-ecosystem.md#standards-body)                             | **International Organization for Standardization** (ISO)  | <https://www.iso.org/>          |
| [PID Provider](../pid-concepts/pid-ecosystem.md#provider)                                         | (RAiD Registration Agencies)     |                        |
| [PID Manager](../pid-concepts/pid-ecosystem.md#manager)                                           | (RAiD Service Points) |        |