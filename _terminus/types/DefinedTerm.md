---
kind: mdbase.type
name: DefinedTerm
version: 1
description: A word, name, acronym, phrase, etc. with a formal definition. Often used
  in the context of category or subject classification, glossaries or dictionaries,
  product or creative work types, etc. Use the name property for the term being defined,
  use termCode if the term has an alpha-numeric code allocated, use description to
  provide the definition of the term. Use the about property to specify what the term
  is about.
collection:
  display:
    icon: "carbon:term"
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
      inDefinedTermSet:
        description: A DefinedTermSet that contains this term.
        type: string
      name:
        description: The name of the item.
        type: string
      termCode:
        description: A code that identifies this DefinedTerm within a DefinedTermSet.
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

Thing > Intangible > DefinedTerm

A word, name, acronym, phrase, etc. with a formal definition. Often used in the context of category or subject classification, glossaries or dictionaries, product or creative work types, etc. Use the name property for the term being defined, use termCode if the term has an alpha-numeric code allocated, use description to provide the definition of the term. Use the about property to specify what the term is about.
