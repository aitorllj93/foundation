---
kind: mdbase.type
name: CreativeWorkSeason
version: 1
description: A media season, e.g. TV, radio, video game etc.
collection:
  display:
    icon: "lucide:list-ordered"
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
      numberOfEpisodes:
        description: The number of episodes in this season or series.
        type: integer
      partOfSeries:
        description: The series to which this episode or season belongs. Supersedes partOfTVSeries.
        type: string
      seasonNumber:
        description: Position of the season within an ordered group of seasons.
        type: integer
    required:
      - "@type"
---
A Schema.org Type

Thing > CreativeWork > CreativeWorkSeason

A media season, e.g. TV, radio, video game etc.