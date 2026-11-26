---
kind: mdbase.type
name: AstronomicalBody
version: 1
description: An astronomical body.
collection:
  display:
    icon: "iconoven:asteroid"
  "x-terminus":
    accent: lime
schema:
  dialect: json-schema-2020-12
  value:
    type: object
    additionalProperties: true
---
Thing > Place > AstronomicalBody

http://sweetontology.net/realmAstroBody/AstronomicalBody 