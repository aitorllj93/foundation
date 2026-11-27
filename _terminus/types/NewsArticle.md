---
kind: mdbase.type
name: NewsArticle
version: 1
description: A NewsArticle is an article whose content reports news, or provides background context and supporting materials for understanding the news.
collection:
  display:
    icon: newspaper
  "x-terminus":
    accent: blue
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
      articleBody:
        description: The actual body of the article.
        type: string
      articleSection:
        description: Articles may belong to one or more 'sections' in a magazine or newspaper, such as Sports, Lifestyle, etc.
        type: string
      backstory:
        description: For an Article, typically a NewsArticle, the backstory property provides a textual summary giving a brief explanation of why and how an article was created. In a journalistic setting this could include information about reporting process, methods, interviews, data sources, etc.
        type: string
      dateline:
        description: "A dateline is a brief piece of text included in news articles that describes where and when the story was written or filed though the date is often omitted. Sometimes only a placename is provided."
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
      printColumn:
        description: The number of the column in which the NewsArticle appears in the print edition.
        type: string
      printEdition:
        description: The edition of the print product in which the NewsArticle appears.
        type: string
      printPage:
        description: If this NewsArticle appears in print, this field indicates the name of the page on which the article is found. Please note that this field is intended for the exact page name (e.g. A5, B18).
        type: string
      printSection:
        description: If this NewsArticle appears in print, this field indicates the print section in which the article appeared.
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

Thing > CreativeWork > Article > NewsArticle

A NewsArticle is an article whose content reports news, or provides background context and supporting materials for understanding the news.

