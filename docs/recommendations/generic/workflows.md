# Systems and workflows

_Last updated: 2026-09-28_

These recommendations concern how PIDs and PID metadata are handled in systems and workflows.

## Build PIDs into systems and automate their use

_Applies to: all PID Users and PID Managers._

!!! quote ""

    Capture, register and exchange PIDs as part of normal workflows, so that research support systems handle PIDs on behalf of their users with as little manual effort as possible.

??? question "Why?"

    Researchers mainly choose services, not identifiers. Manual handling of PIDs is both a burden and a source of errors. When PIDs are captured at the source and passed between systems automatically, information needs to be entered only once, can be verified against authoritative registries, and can be reused for reporting, discovery and follow-up. Systems that cannot handle PIDs limit what an organisation can achieve, and are costly to change once in place.

??? info "How?"

    - Collect PIDs at the source, for example when a person signs in, a dataset is deposited or a grant is registered, and propagate them between systems through APIs instead of making users re-enter information.
    - Retrieve metadata from authoritative PID registries instead of maintaining local copies by hand.
    - Expose PIDs and PID relationships through open APIs and machine-readable exports.
    - Aim for two-way integration: retrieve metadata from PID registries, and write new information back, for example by adding new outputs and grants to ORCID records.
    - Synchronise PID-linked metadata automatically between repositories, research information systems and reporting systems through standard interfaces, such as REST APIs and OAI-PMH.
    - When procuring or developing research information systems, repositories and other research support systems, require that they can record, validate, display, link and, where relevant, register PIDs and PID metadata.

## Include personal data needed for credit, transparency and accountability

_Applies to: all PID Users and PID Managers handling personal data in PID metadata._

!!! quote ""

    Personal data in PID metadata, such as names, person identifiers, affiliations and contributor roles, is in most cases information about people's professional roles in research. Include it where it is needed to give the people involved proper attribution, to ensure transparency and accountability, and to document what has officially been produced in publicly funded research.

??? question "Why?"

    In the research sector, the personal data found in PID metadata mostly describes who has created, contributed to or taken responsibility for research and its outputs. This is the information that gives researchers and other staff proper credit for their work, and that makes it possible for others to cite them, follow their contributions and recognise their expertise.

    The same information makes research transparent and accountable. It shows who is responsible for a study, a dataset or a publication, which is essential for research integrity and for the scrutiny of research results.

    A large part of Swedish research is publicly funded and carried out at universities and other organisations that are government agencies. Researchers and other staff at these organisations are in most cases employed as public servants, and research and its outputs are produced as part of their official duties.

    Such data is still personal data under the GDPR. However, it concerns people's professional roles rather than their private lives, and it serves purposes that are central to how research works. Removing or withholding it would weaken both the credit given to the people involved and the transparency of publicly funded research.

??? info "How?"

    - Identify people and organisations with PIDs where possible, so that credit and responsibility are attributed to the right person and organisation (see [Express relationships between PIDs as links with explicit relation types](referencing.md#express-relationships-between-pids-as-links-with-explicit-relation-types)).
    - Include names, affiliations and contributor roles in PID metadata when they are needed to credit the people involved and to show who is responsible for research and its outputs.
    - Inform researchers and other staff about how information about their professional roles is published in PID metadata and reused by other services.
    - Document the purposes of publishing personal data in PID metadata, and the legal basis for doing so, for example in your PID policy and privacy notices (see [Adopt a PID policy with clear responsibilities](organisation.md#adopt-a-pid-policy-with-clear-responsibilities)).

See also: [Researchers and contributors](../../landscape-analysis/researchers-contributors.md) · [Organisations](../../landscape-analysis/organisations.md) · [Kernel metadata](../../pid-concepts/kernel-metadata.md)
