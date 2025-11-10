# Landing pages

_Last updated: 2025-11-10_

While the purpose of a PID is to point out a digital object or resource, it is not considered good practice to let the PID target be a direct download of that object and nothing else. A responsible implementation of PIDs will also let the PID direct the user to a context that provides information about the digital object. This should ideally be human readable information as well as machine-readable metadata.

For this purpose, providing a default **landing page** for the PID is common practice, and a good solution for most implementations.

The landing page should at least provide basic information about the digital object that is the PID target, including but not limited to:[@web-BestPracticesDOI-24]

* Descriptive information of the target object, such as bibliographic information
* A clear display of the PID itself
* A way to access the target object, such as a direct link or information on how to request it

It is good practice to also let the information provided on the landing page be packaged in widely used machine-readable metadata formats, such as embedded HTML tags complying with the [Schema.org](https://schema.org/) or [Dublin Core](https://www.dublincore.org/) metadata schemas. This will ensure that the PID target can be interpreted by many actors worldwide.

While the landing page should ideally be what is loaded by default for a user following the PID, it is also polite to allow access to various representations of the contents of the PID target resource and the metadata describing it. This may be provided using [content negotiation](https://en.wikipedia.org/wiki/Content_negotiation) with the web server offering f.e. various file formats, in addition to links accessible through the landing page itself. The web server could also be configured to provide rich metadata about the PID target in the HTTP header itself, a technique often referred to as *signposting*.[@web-FAIRSignpostingProfile-23] This may be metadata declaring the aforementioned content and metadata resources and what they are, as well as other descriptive metadata.

If the PID target is not supposed to be accessible anymore, providing a specific landing page called a [tombstone page](tombstone-pages.md) when following the PID will ensure that the PID remains resolvable and that any user will be able to understand what has happened to the PID target.