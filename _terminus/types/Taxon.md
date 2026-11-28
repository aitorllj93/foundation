---
kind: mdbase.type
name: Taxon
version: 1
description: A set of organisms asserted to represent a natural cohesive biological unit.
collection:
  display:
    icon: "streamline-cyber:gorilla"
  "x-terminus":
    accent: rose
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
      childTaxon:
        description: "Closest child taxa of the taxon in question. Inverse property: parentTaxon."
        type: array
        items:
          type: string
      description:
        description: A description of the item.
        type: string
      disambiguatingDescription:
        description: A sub property of description. A short description of the item used to disambiguate from other, similar items. Information from other properties (in particular, name) may be necessary for the description to be useful for disambiguation.
        type: string
      identifier:
        description: The identifier property represents any kind of identifier for any
          kind of Thing, such as ISBNs, GTIN codes, UUIDs etc. Schema.org provides dedicated
          properties for representing many of these, either as textual strings or as URL
          (URI) links. See background notes for more details.
        type: array
        items:
          type: string
      image:
        type: array
        items:
          type: string
      name:
        description: The name of the item.
        type: string
      parentTaxon:
        description: "Closest parent taxon of the taxon in question. Inverse property: childTaxon"
        type: string
      sameAs:
        description: URL of a reference Web page that unambiguously indicates the item's
          identity. E.g. the URL of the item's Wikipedia page, Wikidata entry, or official
          website.
        type: array
        items:
          type: string
      taxonRank:
        description: "The taxonomic rank of this taxon given preferably as a URI from a controlled vocabulary – typically the ranks from TDWG TaxonRank ontology or equivalent Wikidata URIs."
        type: string
      url:
        description: URL of the item.
        type: string
    required:
      - "@type"
---
A Schema.org Type

Thing > Taxon

A set of organisms asserted to represent a natural cohesive biological unit.
