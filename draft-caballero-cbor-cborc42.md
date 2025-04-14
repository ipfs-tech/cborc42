---
###
# Internet-Draft Markdown Template
#
# Rename this file from draft-todo-yourname-protocol.md to get started.
# Draft name format is "draft-<yourname>-<workgroup>-<name>.md".
#
# For initial setup, you only need to edit the first block of fields.
# Only "title" needs to be changed; delete "abbrev" if your title is short.
# Any other content can be edited, but be careful not to introduce errors.
# Some fields will be set automatically during setup if they are unchanged.
#
# Don't include "-00" or "-latest" in the filename.
# Labels in the form draft-<yourname>-<workgroup>-<name>-latest are used by
# the tools to refer to the current version; see "docname" for example.
#
# This template uses kramdown-rfc: https://github.com/cabo/kramdown-rfc
# You can replace the entire file if you prefer a different format.
# Change the file extension to match the format (.xml for XML, etc...)
#
###
title: "The tag-42 profile of CBOR Core"
abbrev: "CBOR/c-42"
category: info

docname: draft-caballero-cborc42
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
area: AREA
workgroup: CBOR Working Group
keyword:
 - CBOR
 - CBOR/c
 - deterministic encoding
 - sparkling distributed ledger
venue:
  group: WG
  type: Working Group
  mail: WG@example.com
  arch: https://example.com/WG
  github: ipfs-tech/cborc42
  latest: https://example.com/LATEST

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
