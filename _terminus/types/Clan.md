---
kind: mdbase.type
name: Clan
version: 1
description: A group of people united by actual or perceived kinship and descent.
collection:
  display:
    icon: "mdi:family-tree"
  "x-terminus":
    accent: rose
schema:
  dialect: json-schema-2020-12
  value:
    type: object
    additionalProperties: true
---
Thing > Organization > Clan

A **clan** is a group of people united by actual or perceived kinship and descent. Even if lineage details remain unknown or non-specific, clan members may claim descent from a founding individual or apical ancestor who serves as a symbol of the clan's unity. Many societies' exogamy rules are on a clan basis, where all members of one's own clan, or the clans of both parents or even grandparents, are excluded from marriage as incest.