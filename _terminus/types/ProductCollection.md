---
kind: mdbase.type
name: ProductCollection
version: 1
description: "A set of products (either ProductGroups or specific variants) that are listed together e.g. in an Offer."
collection:
  display:
    icon: "codicon:collection"
  "x-terminus":
    accent: teal
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
      url:
        type: string
      image:
        anyOf:
          - type: string
          - type: object
            properties:
              caption:
                description: The caption for this object. For downloadable machine formats
                  (closed caption, subtitles etc.) use MediaObject and indicate
                  the encodingFormat.
                type: string
              author:
                description: The author of this content or rating. Please note that author is
                  special in that HTML 5 provides a special mechanism for
                  indicating authorship via the rel tag. That is equivalent to
                  this and may be used interchangeably.
                type: string
              contentUrl:
                description: Actual bytes of the media object, for example the image file or
                  video file.
                type: string
              datePublished:
                description: Date of first publication or broadcast. For example the date a
                  CreativeWork was broadcast or a Certification was issued.
                type: string
                format: date
                pattern: ^(?:(?:\d\d[2468][048]|\d\d[13579][26]|\d\d0[48]|[02468][048]00|[13579][26]00)-02-29|\d{4}-(?:(?:0[13578]|1[02])-(?:0[1-9]|[12]\d|3[01])|(?:0[469]|11)-(?:0[1-9]|[12]\d|30)|(?:02)-(?:0[1-9]|1\d|2[0-8])))$
              description:
                description: A description of the item.
                type: string
              name:
                description: The name of the item.
                type: string
              width:
                description: The width of the item.
                type: string
              height:
                description: The height of the item.
                type: string
            title: ImageObject
            description: An image file.
            examples:
              - "@context": https://schema.org
                "@type": ImageObject
                author: Jane Doe
                contentLocation: Puerto Vallarta, Mexico
                contentUrl: mexico-beach.jpg
                datePublished: 2008-01-25
                description: I took this picture while on vacation last year.
                name: Beach in Mexico
          - type: array
            items:
              anyOf:
                - type: string
                - type: object
                  properties:
                    caption:
                      description: The caption for this object. For downloadable machine formats
                        (closed caption, subtitles etc.) use MediaObject and
                        indicate the encodingFormat.
                      type: string
                    author:
                      description: The author of this content or rating. Please note that author is
                        special in that HTML 5 provides a special mechanism for
                        indicating authorship via the rel tag. That is
                        equivalent to this and may be used interchangeably.
                      type: string
                    contentUrl:
                      description: Actual bytes of the media object, for example the image file or
                        video file.
                      type: string
                    datePublished:
                      description: Date of first publication or broadcast. For example the date a
                        CreativeWork was broadcast or a Certification was
                        issued.
                      type: string
                      format: date
                      pattern: ^(?:(?:\d\d[2468][048]|\d\d[13579][26]|\d\d0[48]|[02468][048]00|[13579][26]00)-02-29|\d{4}-(?:(?:0[13578]|1[02])-(?:0[1-9]|[12]\d|3[01])|(?:0[469]|11)-(?:0[1-9]|[12]\d|30)|(?:02)-(?:0[1-9]|1\d|2[0-8])))$
                    description:
                      description: A description of the item.
                      type: string
                    name:
                      description: The name of the item.
                      type: string
                    width:
                      description: The width of the item.
                      type: string
                    height:
                      description: The height of the item.
                      type: string
                  title: ImageObject
                  description: An image file.
                  examples:
                    - "@context": https://schema.org
                      "@type": ImageObject
                      author: Jane Doe
                      contentLocation: Puerto Vallarta, Mexico
                      contentUrl: mexico-beach.jpg
                      datePublished: 2008-01-25
                      description: I took this picture while on vacation last year.
                      name: Beach in Mexico
      video:
        type: array
        items:
          type: object
          properties:
            contentUrl:
              type: string
              minLength: 1
            name:
              type: string
              minLength: 1
            thumbnailUrl:
              type: string
          required:
            - contentUrl
            - name
      collectionSize:
        description: The number of items in the Collection.
        type: number
      description:
        description: A description of the item.
        type: string
      includesObject:
        minItems: 1
        type: array
        items:
          type: object
          properties:
            typeOfGood:
              type: string
              pattern: ^[a-zA-Z0-9_-]+(?:\/[a-zA-Z0-9_-]+)*$
            amountOfThisGood:
              default: 1
              type: integer
              exclusiveMinimum: 0
              maximum: 9007199254740991
          required:
            - typeOfGood
      name:
        type: string
        minLength: 1
    required:
      - "@type"
---
A Schema.org Type

This term is in the "new" area - implementation feedback and adoption from applications and websites can help improve our definitions.

Thing > CreativeWork > Collection > ProductCollection
Thing > Product > ProductCollection

A set of products (either ProductGroups or specific variants) that are listed together e.g. in an Offer.
