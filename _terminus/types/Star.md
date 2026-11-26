---
kind: mdbase.type
name: Star
version: 1
description: A star.
collection:
  display:
    icon: "iconoir:bright-star"
  "x-terminus":
    accent: lime
schema:
  dialect: json-schema-2020-12
  value:
    type: object
    additionalProperties: true
---
Thing > Place > AstronomicalBody > Star

http://sweetontology.net/realmAstroBody/Star