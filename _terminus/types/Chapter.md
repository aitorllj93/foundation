---
kind: mdbase.type
name: Chapter
version: 1
description: One of the sections into which a book is divided. A chapter usually has a section number or a name.
collection:
  display:
    icon: "fluent:notebook-section-24-regular"
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
      about:
        description: The subject matter of an object.
        type: array
        items:
          type: string
      additionalType:
        description: An additional type for the item, typically used for adding more specific types from external vocabularies in microdata syntax. This is a relationship between something and a class that the thing is in. Typically the value is a URI-identified RDF class, and in this case corresponds to the use of rdf:type in RDF. Text values can be used sparingly, for cases where useful information can be added without their being an appropriate schema to reference. In the case of text values, the class label should follow the schema.org style guide.
        type: array
        items:
          type: string
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
      isPartOf:
        description: Indicates an item or CreativeWork that this item, or CreativeWork (in some sense), is part of.
        type: string
      name:
        description: The name of the item.
        type: string
      pageEnd:
        description: 'The page on which the work ends; for example "138" or "xvi".'
        type: string
      pageStart:
        description: 'The page on which the work starts; for example "135" or "xiii".'
        type: string
      pagination:
        description: 'Any description of pages that is not separated into pageStart and pageEnd; for example, "1-6, 9, 55" or "10-12, 46-49".'
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

Thing > CreativeWork > Chapter

One of the sections into which a book is divided. A chapter usually has a section number or a name.
