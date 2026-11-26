---
kind: mdbase.type
name: CategoryCode
version: 1
description: A Category Code.
collection:
  display:
    icon: "akar-icons:tag"
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
      codeValue:
        description: A short textual code that uniquely identifies the value.
        type: string
      description:
        description: A description of the item.
        type: string
      name:
        description: The name of the item.
        type: string
      image:
        description: An image of the item. This can be a URL or a fully described
          ImageObject.
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
      inCodeSet:
        description: A CategoryCodeSet that contains this category code.
        type: string
    required:
      - "@type"
---
A Schema.org Type

Thing > Intangible > DefinedTerm > CategoryCode

A Category Code.