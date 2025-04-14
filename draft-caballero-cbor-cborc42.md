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

- RFC8610
- RFC8949

informative:

- RFC6920

--- abstract

This document defines a strict profile of CBOR Core (CBOR/c) intended for use with the special tag 42.
Like the CBOR Core it profiles, "CBOR/c-42" can also be used as an internet-scale serialization for JSON, and is optimized for objects that compose into a directed acyclical graph.
Since CBOR/c-42 objects link to one another by hash-based identifiers, deterministic encoding is mandated.
This document mainly targets CBOR tool developers and those downstream users who would like to precisely configure their tools.

--- middle

# Introduction

The IPFS ecosystem has long made structural usage of its own home-grown CBOR profile, dating from the early days of the CBOR working group and fine-tuned over the years in community/internal venues.
Configuring CBOR tooling in various languages to decode this data and encode new data conformantly has been a challenge, and a unified specification (updated to modern terminology, as the CBOR working group has iterated and evolved so much in the intervening years) is set out in this document.

Note: unlike the CBOR/c specification, no opinion on signing mechanics is expressed here, and will be addressed in future documents, if at all.

## Design Goals

The primary goal with this specification, is enabling application developers to configure CBOR tooling for this profile in as language-agnostic a way as possible.
The historical design of this profile was to maximize determinism and simplicity for an internet-scale directed acyclical graph of CBOR documents linked to one another by binary hashes.
These simple content identifiers, defined in Appendix A, are always expressed as bytestrings of tag 42 (similar in design to to [RFC6920] Named Information Hashes).
All other tags, and many major and minor types, are forbidden to reduce ambiguity, and developers are encouraged to express many kinds of data at higher layers by using the supported types (such as strings or bytestrings).

## Requirements Language

{::boilerplate bcp14-tagged}

## Common Definitions

* This document uses the conventions defined in CDDL [RFC8610] for expressing the type of CBOR [RFC8949] data items.
* Examples showing CBOR data, are expressed in "diagnostic notation" as defined in Section 8 of [RFC8949].
* The term "CBOR object" is equivalent to "CBOR data item" used in [RFC8949].
* The term "CBOR Core" is in this document abbreviated to "CBOR/c".

# Specification

## Supported CBOR Objects

## Deterministic Encoding Scheme Profile

## CBOR Tool Requirements

# Security Considerations

TODO Security

# IANA Considerations

This document has no IANA actions.

--- back

# Binary Content Identifiers (Tag 42)

# Acknowledgments
{:numbered="false"}

TODO acknowledge.
