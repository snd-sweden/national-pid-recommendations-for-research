# PID ecosystem

A *PID ecosystem* refers to the layered set of technologies, infrastructures, services and actors that together enable the creation, resolution, management, and use of PIDs. The PID stack as described here was defined in the FAIR-IMPACT project.[@rep-D33Guidelines-24]

## Scheme
A *PID Scheme* defines the basic architecture of the PID, such as the basic template of its composition. It may also contain metadata schemes for metadata that is required or possible to embed together with the PID.

## Authority
A *PID Authority* governs the core concepts and backbone infrastructure of the PID system. It will most often certify or provide licensing to other actors of the PID ecosystem, such as PID Providers. It may lead the strategic development of the PID system, or take a more passive role. 

## Standards Body

The strategic direction of a PID system may in some cases be controlled by a separate *PID Standards Body*, developing standards that define core aspects of the PID system. The Standards Body may define a kernel metadata schema that in some cases may be extended by other actors in the PID ecosystem.

## Provider
A *PID Provider* makes it possible for PID Owners to register PIDs and PID Users to make use of existing registered PIDs. The Provider will often maintain their own infrastructure for storing and managing the PIDs that have been registered through the provider. In many cases, the PID Provider will facilitate PID registration using a hierarchical model, where organisations sign up to manage PIDs for their respective users. 

## Multi-Primary Administrator
In some cases, the Provider will take a larger role in the PID stack. It may for example provide PID resolution infrastructure for all PIDs registered with the Provider. It may also develop and govern a specific subset of the metadata schema associated with the PID. To differentiate this specific type of Provider, they are sometimes referred to as *Multi-Primary Administrator* or MPAs. The main PID system using this terminology today is the Handle system.

## Manager
The individual organisations registered with a PID Provider may be managed by PID Managers through organisational accounts. The PID Managers may register PIDs manually or gain access to infrastructure such as Provider APIs to integrate PID registration and management into software and services.

Some PID systems may be less complex and less decentralised. One organisation may be responsible for several components of the PID ecosystem. In some cases it may even be managed by a single entity, such as PID systems made for local usage.  

## Example 
As an example, we will follow the PID stack of a [DOI](../data-on-pids/doi.md) assigned through DataCite and the [Swedish National Data Service](../pid-actors-sweden/snd.md). Lets assume that this fictional example DOI is: **10.12345/abc-def-xyz**

1. The basic *PID Scheme* for a DOI is in fact based on another PID system, the Handle System. The Handle system has an international PID Authority, the [DONA Foundation](https://www.dona.net/). Among other things, it decides the basic structure of the PID: **firstnumber.secondnumber/suffix**
2. The DONA Foundation is a special type of PID Authority that allows *PID Multi-Primary Administrators* for various implementations of the Handle system. In this case, the PID MPA is the [International DOI Foundation](https://www.doi.org), who governs the DOI system. All DOIs follow the scheme: **10.number/suffix**
3. The *PID Provider* used is [DataCite](https://datacite.org), one of the major organisations providing DOIs. DataCite governs the [DataCite Metadata Schema](https://schema.datacite.org), allowing description of the digital object being pointed to by the DOI while making basic descriptory elements, such as title, creator and resource type, mandatory for all registered DOIs.
4. The *PID Manager* is the [Swedish National Data Service](../pid-actors-sweden/snd.md). However, they are also a DataCite Consortium Lead. This means that other organisations in the Swedish consortium also may act as PID Managers for a specific organisational context, such as a specific DOI prefix registered under their organisation.
5. The local organisation has already registered the DOI prefix: **10.12345**  
Now, they only need to register new DOIs using it.
6. A *PID User* in the local organisation requests the registration of the full DOI using this prefix, **10.12345/abc-def-xyz**, for example through a web tool for publishing digital materials that has API integration with DataCite. Providing the actual target URL as well as DOI metadata for registration may be handled by manual as well as automated processes.
7. The DOI is activated and would, if real, be accessible and resolvable at: **https://doi.org/10.12345/abc-def-xyz**