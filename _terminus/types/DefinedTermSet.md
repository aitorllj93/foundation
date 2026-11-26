---
kind: mdbase.type
name: DefinedTermSet
version: 1
description: A set of defined terms, for example a set of categories or a classification scheme, a glossary, dictionary or enumeration. Use the about property to specify what the term set is about.
collection:
  display:
    icon: "carbon:term-reference"
  "x-terminus":
    accent: mauve
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
      alternateName:
        description: An alias for the item.
        type: array
        items:
          type: string
      description:
        description: A description of the item.
        type: string
      identifier:
        description: The identifier property represents any kind of identifier for any
          kind of Thing, such as ISBNs, GTIN codes, UUIDs etc. Schema.org provides dedicated
          properties for representing many of these, either as textual strings or as URL
          (URI) links. See background notes for more details.
        type: array
        items:
          type: string
      inLanguage:
        description: The language of the content or performance or used in an action.
          Please use one of the language codes from the IETF BCP 47 standard. See also
          availableLanguage. Supersedes language.
        type: string
      name:
        description: The name of the item.
        type: string
      sameAs:
        description: URL of a reference Web page that unambiguously indicates the item's
          identity. E.g. the URL of the item's Wikipedia page, Wikidata entry, or official
          website.
        type: array
        items:
          type: string
      url:
        description: URL of the item.
        type: string
      version:
        description: The version of the CreativeWork embodied by a specified resource.
        type: string
    required:
      - "@type"
---
A Schema.org Type

Thing > CreativeWork > DefinedTermSet

A set of defined terms, for example a set of categories or a classification scheme, a glossary, dictionary or enumeration. Use the about property to specify what the term set is about.
