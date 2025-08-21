# Licenses

_Last updated: 2025-08-21_

As the open science movement continues to grow and digital sharing of research outputs becomes standard, **unambiguous identification of licenses** has become essential. Persistent identifiers (PIDs) or resolvable URIs for licenses provide machine-actionable rights information that is crucial for reusability, compliance, and attribution.

Licenses are particularly relevant for:

* Research datasets
* Publications and articles
* Software and code
* Metadata records
* Media files and supplementary materials

Clearly identifying licenses allows for:

* Ensuring legal clarity on reuse conditions
* Enabling automated filtering and access control
* Supporting compliance with funder and institutional policies
* Facilitating discovery and interoperability across systems
* Aiding in reproducibility and reproducible workflows

When describing scientific digital objects, it should be noted that _licensing_ may often be differentiated from other specific _restrictions_. These may have other origins, such as national legislation. Such restrictions may be described in kernel metadata for other object-related PIDs or in accompanying documentation.

## International license identifiers

### SPDX License List

🟢 Active

The [SPDX License List](https://spdx.org/licenses/) is a standardized list of open source software licenses with unique identifiers, e.g. `MIT`, `Apache-2.0`, `GPL-3.0-or-later`, that acts as an authority file. 

Maintained by the Linux Foundation, it is widely adopted in software packaging, GitHub metadata, and compliance tools. SPDX licenses are also referenced in metadata schemas like CodeMeta and Software Heritage.

Although the focus is mainly on software licenses, many license identifiers that may be used for generic scientific outputs are included, such as the Creative Commons licenses and marks.

Each license has a short identifier string, full name, and canonical URL. The canonical URL also provides the full license text.

While not a true PID, this makes SPDX a de facto identifier for licenses.
