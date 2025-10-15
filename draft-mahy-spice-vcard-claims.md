---
title: "Web Token Claim Registration Inspired by vCard Properties"
abbrev: "vCard properties in Web Tokens"
category: info

docname: draft-mahy-spice-vcard-claims-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
area: "Security"
workgroup: "Secure Patterns for Internet CrEdentials"
keyword:
 - vCard
 - identity
 - web tokens
 - JWT
 - CWT
 - JSON Web Token
 - CBOR Web Token
 - claims
venue:
  group: "Secure Patterns for Internet CrEdentials"
  type: "Working Group"
  mail: "spice@ietf.org"
  arch: "https://mailarchive.ietf.org/arch/browse/spice/"
  github: "rohanmahy/mahy-spice-vcard-claims"
  latest: "https://rohanmahy.github.io/mahy-spice-vcard-claims/draft-mahy-spice-vcard-claims.html"

author:
 -
    fullname: Rohan Mahy
    organization:
    email: rohan.ietf@gmail.com

normative:

informative:


--- abstract

A number of useful claims about humans are registered for use in JSON Web Tokens and CBOR Web Tokens. Another useful source of similar information is in the vCard specification. This document registers those fields.


--- middle

# Introduction

TODO Introduction


# Conventions and Definitions

{::boilerplate bcp14-tagged}


# New Claims

# vcard:geo

The vCard GEO property contains a geographical coordinate.

~~~ json
"vcard:geo": "50.8449007, 4.3498171"
~~~

~~~ cbor-diag
281: [50.8449007, 4.3498171]
~~~

# vcard:impp

The vCard IMPP property contains an instant messaging address. It is a text string.


# vcard:title

The vCard TITLE property contains the formal title of the (usually human) subject, for example:
"Principal Engineer"

It is a text string.

# vcard:org



| vcard:geo |  |  |  | 53.484715052499816, -2.238374047408401 |
| vcard:impp |  |  |  | https://acme.co.uk/u/bob.jones |
| vcard:title |  |  |  | Principal Engineer |
| vcard:org |  |  |  | "Acme Widgets, Ltd." |
logo_uri
| vcard:logo |  |  |  | https://www.acme.co.uk/acme-logo-med.png |
| vcard:member |  |  |  | Full Time Employees, Engineering, Security Alerts, Key Staff |
| vcard:fburl |  |  |  |  |    # Free busy list
vcard:caladuri: |  |  |  |  |  # Send scheduling requests here
vcard:caluri: |  |  |  |  |    # a calendar address (ex: public calendar for a musician or public figure)

~~~
vcard:language

vcard:socialprofile

vcard:sound # pronunciation of name
vcard:phonetic:ipa  # IPA phonetic representation
vcard:phonetic:piny # Pinyin phonetic representation
vcard:phonetic:jyut # Jyutping phonetic representation

vcard:gramgender # grammatical gender
vcard:pronouns
~~~


# Security Considerations

TODO Security


# IANA Considerations

## JWT Claims

JWT already has

- groups, roles, entitlements
- title
- place_of_birth
- nationality
- birth_*_name



## CWT Claims

| vcard:geo |  |  |  | 53.484715052499816, -2.238374047408401 |
| vcard:impp |  |  |  | https://acme.co.uk/u/bob.jones |
| vcard:title |  |  |  | Principal Engineer |
| vcard:org |  |  |  | "Acme Widgets, Ltd." |
logo_uri
| vcard:logo |  |  |  | https://www.acme.co.uk/acme-logo-med.png |
| vcard:member |  |  |  | Full Time Employees, Engineering, Security Alerts, Key Staff |

array

| vcard:fburl |  |  |  |  |    # Free busy list
vcard:caladuri: |  |  |  |  |  # Send scheduling requests here
vcard:caluri: |  |  |  |  |    # a calendar address (ex: public calendar for a musician or public figure)


vcard:lang (languages that may be used for contacting the entity associated with the vCard)


~~~
vcard:socialprofile

vcard:sound # pronunciation of name
vcard:phonetic:ipa  # IPA phonetic representation
vcard:phonetic:piny # Pinyin phonetic representation
vcard:phonetic:jyut # Jyutping phonetic representation

vcard:gramgender # grammatical gender
vcard:pronouns

birthplace, deathplace, deathdate
~~~

--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.
