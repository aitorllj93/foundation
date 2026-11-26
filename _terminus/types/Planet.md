---
kind: mdbase.type
name: Planet
version: 1
description: A planet.
collection:
  display:
    icon: "iconoven:planet-sharp"
  "x-terminus":
    accent: lime
schema:
  dialect: json-schema-2020-12
  value:
    type: object
    additionalProperties: true
---
Thing > Place > AstronomicalBody > Planet

http://sweetontology.net/realmAstroBody/Planet