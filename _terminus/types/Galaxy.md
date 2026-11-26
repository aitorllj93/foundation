---
kind: mdbase.type
name: Galaxy
version: 1
description: A galaxy.
collection:
  display:
    icon: "galaxy"
  "x-terminus":
    accent: lime
schema:
  dialect: json-schema-2020-12
  value:
    type: object
    additionalProperties: true
---
Thing > Place > AstronomicalBody > Galaxy

http://sweetontology.net/realmAstroBody/Galaxy