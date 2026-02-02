# Resolvability

_Last updated: 2026-01-27_

For a PID system to be truly usable, it needs to provide a manner to easily resolve the PID to reach a target in the form of an existing digital object. In a modern online setting this will most often be a **resolver** implemented as a web service, using the HTTP protocol. The resolver will be able to redirect the end user to the target object when using a standard access method, such as a web browser, as well as when using other tools able to fetch or interact with with web resources.

The most common PID resolvers are open and free to use for the end user. An example of this is that the fictional DOI `10.12345/abc-xyz` would be able to be resolved at the general resolver at `doi.org` through the URL `https://doi.org/10.12345/abc-xyz`.

However, some PID systems make use of a distributed resolver infrastructure, where each participating organisation has the responsibility of providing a specific resolver that serves requests for "their own" PIDs to end users. In such cases, resolvability may be incomplete for the PID system, depending on local resolver implementation, outages, etc.

Certain PID systems may be fully resolvable, but require additional authentication or that a request is made from a specific network or environment.

Some legacy PID systems and identifiers may be resolvable using non-common methods, such as making specific queries or database lookups in a specific infrastructure, while not being able to provide access using a common resolvable URL.