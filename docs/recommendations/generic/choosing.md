# Choosing PID systems and services

_Last updated: 2026-09-28_

These recommendations concern how organisations choose the PID systems and services they use, how the metadata of PIDs is kept open, and what to consider if they decide to create a PID system of their own.

## Prefer established PID systems and avoid creating new ones

_Applies to: organisations selecting PID services._

!!! quote ""

    Use established, widely adopted PID systems wherever their scope fits the need. Do not create a new PID system, or a local identifier scheme presented as a PID, for a need that an established system already covers.

??? question "Why?"

    The value of a PID grows with the number of systems and actors that recognise it. Every additional PID system adds cost and fragmentation for everyone who needs to support it. Established systems also come with tested infrastructure, documentation and user communities, while new or little-used systems carry a higher risk of being discontinued or superseded.

??? info "How?"

    - Before considering alternatives, check the [landscape analysis](../../landscape-analysis/index.md) and [Data on PIDs](../../data-on-pids/index.md) for established PID systems covering what you need to identify.
    - Adopt an emerging PID system only when it clearly adds value that existing systems cannot provide.
    - Coordinate the adoption of emerging PID systems with other Swedish actors in the same area; see [National coordination of PID usage](../national/index.md).
    - Avoid PID systems whose development or support has ceased.
    - If you still decide to create your own PID system, see [Follow the Digg profile if you create your own PID system](#follow-the-digg-profile-if-you-create-your-own-pid-system).

See also: [PID ecosystem](../../pid-concepts/pid-ecosystem.md) · [Coverage](../../pid-concepts/coverage.md)

## Prefer PID systems with kernel metadata

_Applies to: organisations selecting PID services and PID Managers._

!!! quote ""

    Prefer PID systems that store descriptive metadata with each identifier ([kernel metadata](../../pid-concepts/kernel-metadata.md)) over basic PIDs, which only provide resolution to a target. Use basic PIDs only where there is a specific reason to do so.

??? question "Why?"

    Whether a PID system stores metadata with each identifier is one of its most consequential properties. Kernel metadata:

    - makes a minimum description of what is identified available independently of the target service;
    - lets aggregators, citation indexes and research information systems find it and its relationships to other PIDs without harvesting individual landing pages;
    - keeps the PID interpretable if the target is temporarily unavailable or permanently withdrawn, and can hold tombstone information after a digital object has been withdrawn;
    - sets a common minimum level of description through mandatory fields in a shared metadata schema.

    With basic PIDs, the target service carries the entire description. If the target service disappears and the PID has not been redirected to a tombstone page, nothing about what it identified remains.

??? info "How?"

    - When possible, always use a PID system with kernel metadata for digital objects and phenomena that are meant to be cited, discovered or reused outside the organisation that holds them.
    - Use basic PIDs only where there is a specific reason, typically when:
        - the PID mainly needs to provide stable resolution with very limited external exposure, such as the internal workflows of a research organisation or infrastructure;
        - the digital objects are numerous and fine-grained, such as individual files, intermediate processing results or data streams, so that registering kernel metadata for each would be disproportionate.
    - Where both are needed, combine them: use a PID with kernel metadata at the level where citation and discovery happen, such as a dataset, and basic PIDs for components below that level, such as files, with explicit links between them.
    - When basic PIDs are used, provide a landing page with machine-readable metadata for every PID (see [Let PIDs resolve to informative landing pages](assigning.md#let-pids-resolve-to-informative-landing-pages)), and redirect PIDs to tombstone pages when digital objects are withdrawn (see [Never delete or reassign a PID, and provide tombstone pages](assigning.md#never-delete-or-reassign-a-pid-and-provide-tombstone-pages)).
    - Designate one authoritative source for the metadata, normally the system where the digital object or record is managed, and update the kernel metadata from it automatically. Do not maintain kernel metadata by hand in parallel with the source.
    - Fill in recommended and optional fields, especially relationships to other PIDs, whenever the information is available.
    - Where a PID system has optional or implementation-specific kernel information, document which metadata profile you use so that others can interpret it.

See also: [Kernel metadata](../../pid-concepts/kernel-metadata.md) · [Interpretability](../../pid-concepts/interpretability.md) · [Landing pages](../../pid-concepts/landing-pages.md)

## Make PID metadata openly available under an open licence

_Applies to: PID Managers and organisations selecting PID services._

!!! quote ""

    Make the metadata you register with PIDs openly available for reuse, preferably with a public domain dedication such as CC0, and through open APIs or data dumps.

??? question "Why?"

    PID metadata is the raw material of open research information. Aggregators, research information systems and scientific knowledge graphs can only link and reuse metadata that they are allowed to access and reuse. Restrictive licences, closed interfaces and missing licence statements stop metadata from flowing between systems, and create dependencies on proprietary services.

    Several major PID providers already make registered metadata openly available. What is registered, and the licence of metadata published elsewhere, such as on landing pages and in repository exports, remain the responsibility of the PID Manager.

??? info "How?"

    - Prefer PID services that make registered metadata openly available (see [Assess PID systems and providers against explicit criteria](#assess-pid-systems-and-providers-against-explicit-criteria)).
    - Apply an open licence, preferably CC0, to metadata you publish yourself, such as landing page metadata, repository exports and catalogue records, and state the licence explicitly.
    - Provide metadata through open APIs, harvesting interfaces or data dumps.
    - Remember that an open licence for metadata does not require the digital object itself to be openly available (see [Keep PIDs and descriptive metadata open, even when access is restricted](#keep-pids-and-descriptive-metadata-open-even-when-access-is-restricted)).

See also: [Kernel metadata](../../pid-concepts/kernel-metadata.md)

## Keep PIDs and descriptive metadata open, even when access is restricted

_Applies to: organisations selecting PID services and PID Managers._

!!! quote ""

    Make sure that PIDs can be resolved by anyone, without authentication and from any network. When access to the digital object itself is restricted, the PID should still resolve to a publicly accessible description of it.

??? question "Why?"

    A PID that cannot be resolved by everyone cannot serve as a reliable reference in citations and metadata shared outside the organisation. Restricted data, such as sensitive personal data or data under confidentiality, also benefits from being findable: an open description lets others discover that the data exists, cite it and request access through the proper channels, without exposing the data itself. Kernel metadata may be hard or impossible to withdraw once registered, since it is replicated and harvested by other services.

??? info "How?"

    - Let PIDs for restricted digital objects resolve to a public landing page that describes them and explains how access can be requested.
    - Control exposure of the PID target by adapting its descriptive metadata to current needs, and avoid hiding the existence of the digital object.
    - Restrict descriptive metadata in exceptional cases, where even the existence or description of a digital object is sensitive.
    - Decide on such cases before a PID is registered.

See also: [Resolvability](../../pid-concepts/resolvability.md) · [Landing pages](../../pid-concepts/landing-pages.md)

## Assess PID systems and providers against explicit criteria

_Applies to: organisations selecting PID services._

!!! quote ""

    Choose PID systems and providers based on a documented assessment against explicit criteria, rather than on which service happens to be at hand.

??? question "Why?"

    Adopting a PID system is a long-term commitment. PIDs are meant to outlive the systems, and often the organisations, that register them, and PIDs that have been cited must remain resolvable even if the organisation later changes to another system. PID systems differ in scope, resolution, metadata, governance and cost in ways that are not always visible when a service is first set up. A documented assessment makes the choice transparent and allows it to be reviewed as the landscape changes.

??? info "How?"

    - Assess at least the properties listed in the criteria table.
    - Document the assessment and the reasons for the choice, for example in your PID policy (see [Adopt a PID policy with clear responsibilities](organisation.md#adopt-a-pid-policy-with-clear-responsibilities)).
    - Review the assessment when the needs, the PID system or the provider change significantly.
    - Use [Data on PIDs](../../data-on-pids/index.md), which documents several of these properties for the PID systems most relevant to the Swedish research sector.

    | Property | Questions to ask | Related concepts |
    | -------- | ---------------- | ---------------- |
    | Scope and conceptual coverage | Is the system designed for what you need to identify? Can its model express the distinctions you need, such as versions, parts, collections and contributor roles? | [Usage scope](../../pid-concepts/usage-scope.md), [Coverage](../../pid-concepts/coverage.md) |
    | Implementational coverage | Is the system supported by the tools and services your researchers, partners, funders, publishers and aggregators use? | [Coverage](../../pid-concepts/coverage.md) |
    | Resolvability | Is there an open, global resolver using HTTPS? Does resolution depend on local or national resolvers that someone must keep running? Can PIDs be resolved without authentication? | [Resolvability](../../pid-concepts/resolvability.md) |
    | Kernel metadata | Does the system store metadata with each PID? Which metadata is mandatory, and is it openly available? See [Prefer PID systems with kernel metadata](#prefer-pid-systems-with-kernel-metadata). | [Kernel metadata](../../pid-concepts/kernel-metadata.md) |
    | Uniqueness and persistence | Who guarantees that PIDs are never reused or deleted? Is there a published persistence policy? | [Uniqueness](../../pid-concepts/uniqueness.md), [Persistence](../../pid-concepts/persistence.md) |
    | Versioning and granularity | Does the system support concept PIDs, version relationships and part–whole relationships? | [Concept PIDs](../../pid-concepts/concept-pids.md) |
    | Governance | Who is the PID Authority and Provider? Is governance open, non-profit and community-led? Do research communities, including Swedish and European ones, have a voice? | [PID ecosystem](../../pid-concepts/pid-ecosystem.md) |
    | Sustainability and exit | Is the business model transparent? Does the provider have a contingency or exit plan? Can you export all your PIDs, targets and metadata? | [Persistence](../../pid-concepts/persistence.md) |
    | Preservation and certification | Are the identified digital objects and their metadata preserved in the long term? Is the service, or the repository behind it, certified, for example with CoreTrustSeal? | [Persistence](../../pid-concepts/persistence.md) |
    | Scale | How many PIDs are expected, and how fast will their number grow? Can the service and its cost model handle that volume, including a future migration? | |
    | Service level | Are availability, support, API documentation and incident reporting adequate for the intended use? | |
    | Cost | What does registration, membership and maintenance cost, and who pays? Resolution should be free for end users. | |
    | Legal and data protection | Where is metadata stored and processed? How is personal data handled under the GDPR? | |
    | Standardisation | Is the system based on an open specification or a formal standard (ISO, RFC)? | [Data on PIDs](../../data-on-pids/index.md) |

See also: [PID concepts](../../pid-concepts/index.md)

## Follow the Digg profile if you create your own PID system

_Applies to: organisations selecting PID services and PID Managers._

!!! quote ""

    If an organisation, after considering other options, decides to create and operate a new PID system of its own, follow [_Profil för beständiga identifierare_](https://www.dataportal.se/profil-for-bestandiga-identifierare), the profile for persistent identifiers published by the Swedish Agency for Digital Government (Digg).

??? question "Why?"

    While established PID systems should be the first choice, an organisation may still have good reasons to create its own PIDs, for example when it is the natural authority for digital objects or phenomena that no established PID system covers. Such PIDs are only as reliable as the way they are designed and operated, and a system built from scratch lacks the shared rules, infrastructure and tools that established PID systems provide.

    The Digg profile gives Swedish public sector organisations common rules for persistent identifiers, built on established web standards and linked data principles. Following it makes an organisation's PIDs work in the same way as those of other Swedish public actors, so that they can be resolved and interpreted with ordinary web tools and used in linked open data.

    PIDs created in this way have no [kernel metadata](../../pid-concepts/kernel-metadata.md) held by a separate PID service. The descriptions returned by the organisation's own lookup mechanism are then the only metadata available, which makes consistent, machine-readable responses particularly important.

??? info "How?"

    - Document why an established PID system cannot be used. If other actors already identify the same things, inform them, point out their identifiers as alternate or canonical identifiers, and aim for agreement on which identifier to use.
    - Express PIDs as HTTP or HTTPS URLs under a domain name with a stable owner, normally the organisation's own domain. Do not include port numbers, user names, passwords, query parameters, fragments, version numbers or file extensions in the URLs.
    - Keep the URL structure of the PID simple and stable. Prefer generated, opaque strings for the final part whenever possible. Use an existing identifier from the organisation's own systems, such as a case number, only when it is itself guaranteed to be persistent and there is a clear need to reuse it (see [Keep PID strings opaque and free from meaning](assigning.md#keep-pid-strings-opaque-and-free-from-meaning)).
    - Let PIDs be resolved with ordinary DNS and HTTP. Return information resources directly, and offer alternative formats and languages through content negotiation and HTTP `Link` headers.
    - Use standard HTTP responses for changes over the lifecycle.
    - Provide machine-readable descriptions of what the PIDs identify, preferably as linked data, and apply the recommendations on landing pages and tombstone pages (see [Let PIDs resolve to informative landing pages](assigning.md#let-pids-resolve-to-informative-landing-pages) and [Never delete or reassign a PID, and provide tombstone pages](assigning.md#never-delete-or-reassign-a-pid-and-provide-tombstone-pages)).

See also: [Resolvability](../../pid-concepts/resolvability.md) · [Interpretability](../../pid-concepts/interpretability.md) · [Landing pages](../../pid-concepts/landing-pages.md) · [Tombstone pages](../../pid-concepts/tombstone-pages.md)
