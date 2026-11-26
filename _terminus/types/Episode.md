---
kind: mdbase.type
name: Episode
version: 1
description: A media episode (e.g. TV, radio, video game) which can be part of a series or season.
collection:
  display:
    icon: "lucide:numbers"
  "x-terminus":
    accent: purple
schema:
  dialect: json-schema-2020-12
  value:
    type: object
    additionalProperties: true
    properties:
      "@type":
        anyOf:
          - type: string
          - type: array
            items: { type: string }
      episodeNumber:
        description: Position of the episode within an ordered group of episodes.
        type: number
      partOfSeason:
        description: The season to which this episode belongs.
        type: string
      partOfSeries:
        description: The series to which this episode or season belongs. Supersedes partOfTVSeries.
        type: string
    required:
      - "@type"
---
A Schema.org Type

Thing > CreativeWork > Episode

A media episode (e.g. TV, radio, video game) which can be part of a series or season.
