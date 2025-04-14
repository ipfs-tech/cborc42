---
title: "The tag-42 profile of CBOR Core"
abbrev: "CBOR/c-42"
category: info

docname: draft-caballero-cbor-cborc42-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
area: ""
workgroup: "Concise Binary Object Representation Maintenance and Extensions"
keyword:
 - CBOR
 - CBOR/c
 - deterministic encoding
 - sparkling distributed ledger
venue:
  group: "Concise Binary Object Representation Maintenance and Extensions"
  type: ""
  mail: "cbor@ietf.org"
  arch: "https://www.ietf.org/mail-archive/web/cbor/current/maillist.html"
  github: "ipfs-tech/cborc42"
  latest: "https://ipfs-tech.github.io/cborc42/draft-caballero-cbor-cborc42.html"

author:
 -
    fullname: Juan Caballero
    organization: IPFS Foundation
    email: bumblefudge@learningproof.xyz
 -
    fullname: Robin Berjon
    organization: IPFS Foundation
    email: robin@berjon.com

normative:

informative:

--- abstract

This document defines a strict profile of CBOR Core (CBOR/c) intended for use with the special tag 42.
Like the CBOR Core it profiles, "CBOR/c-42" can also be used as an internet-scale serialization for JSON, and is optimized for objects that compose into a directed acyclical graph.
Since CBOR/c-42 objects link to one another by hash-based identifiers, deterministic encoding is mandated.
This document mainly targets CBOR tool developers and those downstream users who would like to precisely configure their tools.

--- middle

# Introduction

TODO Introduction


# Conventions and Definitions

{::boilerplate bcp14-tagged}


# Security Considerations

TODO Security


# IANA Considerations

This document has no IANA actions.


--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.
