# RRID

_Last updated: 2026-08-23_

[RRID](https://rrid.site/) (Research Resource Identifier) is a PID system created for unique identification of entities often referred to in life sciences research, making up specific RRID subtypes. Examples include reagents, f.e. organisms, antibodies, plasmids or cell lines. It is also used to identify specific core facilities and instruments, as well as tools and software packages.

RRIDs were introduced by the [Resource Identification Initiative](https://www.rrids.org/) and originated in the [SciCrunch](https://scicrunch.org) infrastructure run by the University of California. RRIDs.org is now run as an NPO.

RRID subtypes are indexed in specific collaborating registries, such as [ABRF CoreMarketplace](https://coremarketplace.org) which registers core facilities and instruments. The RRID landing page may contain a link to a local entry in a specific registry or database.

## Where to get started as a Swedish organisation?
| Use case                             | Contact                        | URL |
| --------                             | -------                        | -------                        |
| Add a new RRID resource to one of the RRID subtype registries | RRID Portal: Add a resource | <https://rrid.site/about/resource> |

## PID Parameters
| Parameter                                                                               | Value                                   | Details |
| --------                                                                                | -------                                 | ------- |
| Full name                                                                               | **Research Resource Identifier**           ||
| Abbreviated name                                                                        | **RRID**                                 ||
| Intended [scope](../pid-concepts/usage-scope.md) / PID target(s)                        | **Reagents, materials, tools, facilities etc.**             | Detailed scopes are specified for each RRID subtype. |
| Based on other PID system(s)                                                            | **No**                       ||
| Namespace                                                                               | **RRID:**                                  | Subtypes will also make use of sub-namespaces. |
| Example                                                                                 | **RRID:AB_2783747**                    ||
| Example with resolver #1                                                                 | <https://n2t.net/RRID:AB_2783747>      | Example: Antibody |
| Example with resolver #2                                                                 | <https://n2t.net/RRID:IMSR_JAX:000664> | Example: Organism |
| Example with resolver #3                                                                 | <https://n2t.net/RRID:Addgene_80088>   | Example: Plasmid |
| Example with resolver #4                                                                 | <https://n2t.net/RRID:CVCL_LB79>  | Example: Cell line |
| Example with resolver #5                                                                 | <https://n2t.net/RRID:SAMN19842595>      | Example: Biosample |
| Example with resolver #6                                                                 | <https://n2t.net/RRID:SCR_028619>      | Example: Core facility or Instrument |
| Example with resolver #7                                                                 | <https://n2t.net/RRID:SCR_003070>      | Example: Tool or Software |
| Case sensitive                                                                          | **No**                                  ||
| General resolver #1                                                                     | <https://n2t.net/>                      ||
| General resolver #2                                                                     | <https://identifiers.org/RRID/>                   ||
| May use custom resolver                                                                 | **Yes**                                 | Separate resolvers are serving RRID subtype registries. |
| Accompanying [metadata kernel](../pid-concepts/kernel-metadata.md)                      | **No**                                  |  |
| Inception                                                                               | **2014**                                | <https://www.rrids.org/rridhistory> |
| Documentation                                                                           | **RRID Portal: Getting Started**        | <https://rrid.site/about/Getting%20Started> |
| Wikipedia article                                                                       | **SciCrunch: Research Resource Identifiers**                           | <https://en.wikipedia.org/wiki/SciCrunch#Research_Resource_Identifiers> |
| Wikidata Q-ID                                                                           | **Q107278278**                              | <https://www.wikidata.org/wiki/Q107278278> |
| Wikidata P-ID                                                                           | **P9712**                                | <https://www.wikidata.org/wiki/Property:P9712> |

## PID Ecosystem
| Component                                                                                         | Name                              | URL                           |
| --------                                                                                          | -------                           | -------                       |
| [PID Scheme](../pid-concepts/pid-ecosystem.md#scheme)                                             | **RRID System**                 | <https://www.rrids.org/current-project>     |
| [PID Authority](../pid-concepts/pid-ecosystem.md#authority)                                       | **Research Resource Identification Initiative**               | <https://www.rrids.org/>       |
| [PID Standards Body](../pid-concepts/pid-ecosystem.md#standards-body)                             | **Research Resource Identification Initiative Board** | <https://www.rrids.org/team>          |
| [PID Provider](../pid-concepts/pid-ecosystem.md#provider)                                      | (Various subtype registries)                      | |
| [PID Manager](../pid-concepts/pid-ecosystem.md#manager)                                           | (Various subtype registries)                          ||

