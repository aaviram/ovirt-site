---
title: API - oVirt workshop November 2011 Notes
category: event/workshop
authors: dannfrazier, michael pasternak, quaid
wiki_category: Workshop November 2011
wiki_title: API - oVirt workshop November 2011 Notes
wiki_revision_count: 4
wiki_last_updated: 2012-01-15
---

# API - oVirt workshop November 2011 Notes

Presenter slides: ![](oVirt-API-CLI-SDK-20111102.pdf "fig:oVirt-API-CLI-SDK-20111102.pdf")

## oVirt API

### Maintainer

Michael Pasternak: mpastern@redhat.com

### Overview

*   Overview of HTTP and RESTful protocols
*   Compare/Contrast SOAP & REST
*   Overview of oVirt-API url structure / headers; examples of different methods
*   Responses are blocked until operation completes (is what I think I heard)
*   Browser tour of API
*   Suggested tools for using the REST API (FF REST, curl, etc), and examples operations w/ 'em
*   Python SDK - fully compliant w/ oVirt API, autogenerated
    -   RSDL - RESTful Services Description Language; http(s)://server:port/api?rsdl describes parameter constraints
    -   Overview of using the SDK
    -   (Something about SSL - missed it doubletasking)
*   CLI usage
*   What next?
    -   non-admin user access - restricting views of resources
    -   atomic ops - e.g. changing network config w/o losing access (iirc)
    -   supporting new features of the oVirt engine

### Discussion

      Q: How do we know that we didn't break API compat?
      In general we don't want to break the API, but some things are marked as new/may change.
      Need to define a deprecation strategy.
      Suggestion: major versions can break the API/minors must not.
      Maybe too early to keep a static API.
      DB scheme changes - API will have to change or backward compat layer maintained
      Q: can you lock a resource (e.g. while updating)
      Not today; actions can conflict (shutdown a vm racing w/ a vm change) - but updates do not.
      Maybe worth adding this functionality to the API.

[Category:Workshop November 2011](Category:Workshop November 2011)