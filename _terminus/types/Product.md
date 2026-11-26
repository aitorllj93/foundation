---
kind: mdbase.type
name: Product
version: 1
description: "Any offered product or service. For example: a pair of shoes; a concert ticket; the rental of a car; a haircut; or an episode of a TV show streamed online."
collection:
  display:
    icon: "carbon:product"
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
      brand:
        description: The brand(s) associated with a product or service, or the brand(s)
          maintained by an organization or business person.
        type: object
        properties:
          name:
            description: The name of the item.
            type: string
        title: Brand
      category:
        description: A category for the item. Greater signs or slashes can be used to
          informally indicate a category hierarchy.
        anyOf:
          - type: object
            properties:
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
                          (closed caption, subtitles etc.) use MediaObject and
                          indicate the encodingFormat.
                        type: string
                      author:
                        description: The author of this content or rating. Please note that author is
                          special in that HTML 5 provides a special mechanism
                          for indicating authorship via the rel tag. That is
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
                  - type: array
                    items:
                      anyOf:
                        - type: string
                        - type: object
                          properties:
                            caption:
                              description: The caption for this object. For downloadable machine formats
                                (closed caption, subtitles etc.) use MediaObject
                                and indicate the encodingFormat.
                              type: string
                            author:
                              description: The author of this content or rating. Please note that author is
                                special in that HTML 5 provides a special
                                mechanism for indicating authorship via the rel
                                tag. That is equivalent to this and may be used
                                interchangeably.
                              type: string
                            contentUrl:
                              description: Actual bytes of the media object, for example the image file or
                                video file.
                              type: string
                            datePublished:
                              description: Date of first publication or broadcast. For example the date a
                                CreativeWork was broadcast or a Certification
                                was issued.
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
            title: CategoryCode
            description: A Category Code.
          - type: array
            items:
              type: object
              properties:
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
                            (closed caption, subtitles etc.) use MediaObject and
                            indicate the encodingFormat.
                          type: string
                        author:
                          description: The author of this content or rating. Please note that author is
                            special in that HTML 5 provides a special mechanism
                            for indicating authorship via the rel tag. That is
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
                    - type: array
                      items:
                        anyOf:
                          - type: string
                          - type: object
                            properties:
                              caption:
                                description: The caption for this object. For downloadable machine formats
                                  (closed caption, subtitles etc.) use
                                  MediaObject and indicate the encodingFormat.
                                type: string
                              author:
                                description: The author of this content or rating. Please note that author is
                                  special in that HTML 5 provides a special
                                  mechanism for indicating authorship via the
                                  rel tag. That is equivalent to this and may be
                                  used interchangeably.
                                type: string
                              contentUrl:
                                description: Actual bytes of the media object, for example the image file or
                                  video file.
                                type: string
                              datePublished:
                                description: Date of first publication or broadcast. For example the date a
                                  CreativeWork was broadcast or a Certification
                                  was issued.
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
              title: CategoryCode
              description: A Category Code.
          - type: string
          - type: array
            items:
              type: string
        title: Category
      color:
        description: The color of the product.
        type: string
      consumerNotice:
        description: A consumer notice, such as a safety warning or mandatory
          information, related to the product.
        anyOf:
          - type: string
          - type: object
            properties:
              name:
                description: The name of the item.
                type: string
              text:
                description: The textual content of this CreativeWork.
                type: string
            title: TextObject
            description: A text file. The text can be unformatted or contain markup, html,
              etc.
          - type: array
            items:
              anyOf:
                - type: string
                - type: object
                  properties:
                    name:
                      description: The name of the item.
                      type: string
                    text:
                      description: The textual content of this CreativeWork.
                      type: string
                  title: TextObject
                  description: A text file. The text can be unformatted or contain markup, html,
                    etc.
      description:
        description: A description of the item.
        type: string
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
      hasMerchantReturnPolicy:
        type: object
        properties: {}
        title: MerchantReturnPolicy
        description: A MerchantReturnPolicy provides information about product return
          policies associated with an Organization, Product, or Offer.
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
      inProductGroupWithID:
        description: Indicates the productGroupID for a ProductGroup that this product
          isVariantOf.
        type: string
      isAccessoryOrSparePartFor:
        anyOf:
          - $ref: "#"
          - type: array
            items:
              $ref: "#"
        description: A pointer to another product (or multiple products) for which this
          product is an accessory or spare part.
      isOftenBoughtWith:
        anyOf:
          - $ref: "#"
          - type: array
            items:
              $ref: "#"
        description: Indicates a product that is often bought with the described product.
      isRelatedTo:
        anyOf:
          - $ref: "#"
          - type: array
            items:
              $ref: "#"
        description: A pointer to another, somehow related product (or multiple products).
      isSimilarTo:
        anyOf:
          - $ref: "#"
          - type: array
            items:
              $ref: "#"
        description: A pointer to another, functionally similar product (or multiple
          products).
      isVariantOf:
        type: object
        properties:
          hasVariant:
            description: "Indicates a Product that is a member of this ProductGroup (or
              ProductModel). Inverse property: isVariantOf"
            type: array
            items:
              $ref: "#"
          productGroupId:
            description: Indicates a textual identifier for a ProductGroup.
            type: string
          variesBy:
            type: array
            items:
              anyOf:
                - type: object
                  properties:
                    name:
                      description: The name of the item.
                      type: string
                    value:
                      description: >-
                        The value of a QuantitativeValue (including Observation)
                        or property value node.

                        - For QuantitativeValue and MonetaryAmount, the
                        recommended type for values is 'Number'.

                        - For PropertyValue, it can be 'Text', 'Number',
                        'Boolean', 'StructuredValue' or 'QualitativeValue'.

                        - Use values from 0123456789 (Unicode 'DIGIT ZERO'
                        (U+0030) to 'DIGIT NINE' (U+0039)) rather than
                        superficially similar Unicode symbols.

                        - Use '.' (Unicode 'FULL STOP' (U+002E)) rather than ','
                        to indicate a decimal point. Avoid using these symbols
                        as a readability separator.
                      type: array
                      items:
                        anyOf:
                          - type: object
                            properties:
                              name:
                                description: The name of the item.
                                anyOf:
                                  - type: array
                                    items:
                                      type: string
                                  - type: string
                              sizeSystem:
                                description: The size system used to identify a product's size. Typically either
                                  a standard (for example, "GS1" or
                                  "ISO-EN13402"), country code (for example "US"
                                  or "JP"), or a measuring system (for example
                                  "Metric" or "Imperial").
                                type: string
                              sizeGroup:
                                description: The size group (also known as "size type") for a product's size.
                                  Size groups are common in the fashion industry
                                  to define size segments and suggested
                                  audiences for wearable products. Multiple
                                  values can be combined, for example "men's big
                                  and tall", "petite maternity" or "regular".
                                type: string
                            title: SizeSpecification
                            description: Size related properties of a product, typically a size code (name)
                              and optionally a sizeSystem, sizeGroup, and
                              product measurements (hasMeasurement). In
                              addition, the intended audience can be defined
                              through suggestedAge, suggestedGender, and
                              suggested body measurements
                              (suggestedMeasurement).
                            examples:
                              - "@type": SizeSpecification
                                name:
                                  - XS
                                  - S
                                sizeSystem: https://schema.org/WearableSizeSystemUS
                                sizeGroup: https://schema.org/WearableSizeGroupPetite
                              - "@type": SizeSpecification
                                name:
                                  - M
                                  - L
                                sizeSystem: https://schema.org/WearableSizeSystemUS
                                sizeGroup: https://schema.org/WearableSizeGroupRegular
                              - "@type": SizeSpecification
                                name: XL
                                sizeSystem: https://schema.org/WearableSizeSystemUS
                                sizeGroup: https://schema.org/WearableSizeGroupPlus
                              - "@type": SizeSpecification
                                name:
                                  - XXL
                                  - XXXL
                                sizeSystem: https://schema.org/WearableSizeSystemUS
                                sizeGroup: https://schema.org/WearableSizeGroupBig
                          - type: string
                          - type: number
                          - type: "null"
                    valueGroup:
                      description: A header or section name for grouping related property values.
                      type: string
                    unitCode:
                      description: The unit of measurement given using the UN/CEFACT Common Code (3
                        characters) or a URL. Other codes than the UN/CEFACT
                        Common Code may be used with a prefix followed by a
                        colon.
                      type: string
                    unitText:
                      description: A string or text indicating the unit of measurement. Useful if you
                        cannot provide a standard unit code for unitCode.
                      type: string
                  title: PropertyValue
                  description: A property-value pair, e.g. representing a feature of a product or
                    place. Use the 'name' property for the name of the property.
                    If there is an additional human-readable version of the
                    value, put that into the 'description' property. Always use
                    specific schema.org properties when a) they exist and b) you
                    can populate them. Using PropertyValue as a substitute will
                    typically not trigger the same effect as using the original,
                    specific property.
                  examples:
                    - "@type": PropertyValue
                      name: color
                      value:
                        - black
                        - silver
                    - "@type": PropertyValue
                      name: material
                      value:
                        - plastic
                        - aluminum
                    - "@type": PropertyValue
                      name: size
                      value:
                        - "@type": SizeSpecification
                          name:
                            - XS
                            - S
                          sizeSystem: https://schema.org/WearableSizeSystemUS
                          sizeGroup: https://schema.org/WearableSizeGroupPetite
                        - "@type": SizeSpecification
                          name:
                            - M
                            - L
                          sizeSystem: https://schema.org/WearableSizeSystemUS
                          sizeGroup: https://schema.org/WearableSizeGroupRegular
                        - "@type": SizeSpecification
                          name: XL
                          sizeSystem: https://schema.org/WearableSizeSystemUS
                          sizeGroup: https://schema.org/WearableSizeGroupPlus
                        - "@type": SizeSpecification
                          name:
                            - XXL
                            - XXXL
                          sizeSystem: https://schema.org/WearableSizeSystemUS
                          sizeGroup: https://schema.org/WearableSizeGroupBig
                - type: string
            description: Indicates the property or properties by which the variants in a
              ProductGroup vary, e.g. their size, color etc. Schema.org
              properties can be referenced by their short name e.g. "color";
              terms defined elsewhere can be referenced with their URIs. Variant
              properties can be provided using PropertyValue instead of plain
              Text, to allow specification of the values available for a variant
              property.
        required:
          - variesBy
        title: ProductGroup
        description: Indicates the kind of product that this is a variant of. In the
          case of ProductModel, this is a pointer (from a ProductModel) to a
          base product from which this product is a variant. It is safe to infer
          that the variant inherits all product features from the base model,
          unless defined locally. This is not transitive. In the case of a
          ProductGroup, the group description also serves as a template,
          representing a set of Products that vary on explicitly defined,
          specific dimensions only (so it defines both a set of variants, as
          well as which values distinguish amongst those variants). When used
          with ProductGroup, this property can apply to any Product included in
          the group.
      keywords:
        description: Keywords or tags used to describe some item. Multiple textual
          entries in a keywords list are typically delimited by commas, or by
          repeating the property.
        type: string
      material:
        description: A material that something is made from, e.g. leather, wool, cotton,
          paper.
        type: string
      name:
        description: The name of the item.
        type: string
      productId:
        description: 'The product identifier, such as ISBN. For example: meta
          itemprop="productID" content="isbn:123-456-789".'
        type: string
      releaseDate:
        description: The release date of a product or product model. This can be used to
          distinguish the exact variant of a product.
        type: string
        format: date
        pattern: ^(?:(?:\d\d[2468][048]|\d\d[13579][26]|\d\d0[48]|[02468][048]00|[13579][26]00)-02-29|\d{4}-(?:(?:0[13578]|1[02])-(?:0[1-9]|[12]\d|3[01])|(?:0[469]|11)-(?:0[1-9]|[12]\d|30)|(?:02)-(?:0[1-9]|1\d|2[0-8])))$
      sameAs:
        description: URL of a reference Web page that unambiguously indicates the item's
          identity. E.g. the URL of the item's Wikipedia page, Wikidata entry,
          or official website.
        type: array
        items:
          type: string
      size:
        anyOf:
          - type: object
            properties:
              name:
                description: The name of the item.
                anyOf:
                  - type: array
                    items:
                      type: string
                  - type: string
              sizeSystem:
                description: The size system used to identify a product's size. Typically either
                  a standard (for example, "GS1" or "ISO-EN13402"), country code
                  (for example "US" or "JP"), or a measuring system (for example
                  "Metric" or "Imperial").
                type: string
              sizeGroup:
                description: The size group (also known as "size type") for a product's size.
                  Size groups are common in the fashion industry to define size
                  segments and suggested audiences for wearable products.
                  Multiple values can be combined, for example "men's big and
                  tall", "petite maternity" or "regular".
                type: string
            title: SizeSpecification
            description: Size related properties of a product, typically a size code (name)
              and optionally a sizeSystem, sizeGroup, and product measurements
              (hasMeasurement). In addition, the intended audience can be
              defined through suggestedAge, suggestedGender, and suggested body
              measurements (suggestedMeasurement).
            examples:
              - "@type": SizeSpecification
                name:
                  - XS
                  - S
                sizeSystem: https://schema.org/WearableSizeSystemUS
                sizeGroup: https://schema.org/WearableSizeGroupPetite
              - "@type": SizeSpecification
                name:
                  - M
                  - L
                sizeSystem: https://schema.org/WearableSizeSystemUS
                sizeGroup: https://schema.org/WearableSizeGroupRegular
              - "@type": SizeSpecification
                name: XL
                sizeSystem: https://schema.org/WearableSizeSystemUS
                sizeGroup: https://schema.org/WearableSizeGroupPlus
              - "@type": SizeSpecification
                name:
                  - XXL
                  - XXXL
                sizeSystem: https://schema.org/WearableSizeSystemUS
                sizeGroup: https://schema.org/WearableSizeGroupBig
          - type: array
            items:
              type: object
              properties:
                name:
                  description: The name of the item.
                  anyOf:
                    - type: array
                      items:
                        type: string
                    - type: string
                sizeSystem:
                  description: The size system used to identify a product's size. Typically either
                    a standard (for example, "GS1" or "ISO-EN13402"), country
                    code (for example "US" or "JP"), or a measuring system (for
                    example "Metric" or "Imperial").
                  type: string
                sizeGroup:
                  description: The size group (also known as "size type") for a product's size.
                    Size groups are common in the fashion industry to define
                    size segments and suggested audiences for wearable products.
                    Multiple values can be combined, for example "men's big and
                    tall", "petite maternity" or "regular".
                  type: string
              title: SizeSpecification
              description: Size related properties of a product, typically a size code (name)
                and optionally a sizeSystem, sizeGroup, and product measurements
                (hasMeasurement). In addition, the intended audience can be
                defined through suggestedAge, suggestedGender, and suggested
                body measurements (suggestedMeasurement).
              examples:
                - "@type": SizeSpecification
                  name:
                    - XS
                    - S
                  sizeSystem: https://schema.org/WearableSizeSystemUS
                  sizeGroup: https://schema.org/WearableSizeGroupPetite
                - "@type": SizeSpecification
                  name:
                    - M
                    - L
                  sizeSystem: https://schema.org/WearableSizeSystemUS
                  sizeGroup: https://schema.org/WearableSizeGroupRegular
                - "@type": SizeSpecification
                  name: XL
                  sizeSystem: https://schema.org/WearableSizeSystemUS
                  sizeGroup: https://schema.org/WearableSizeGroupPlus
                - "@type": SizeSpecification
                  name:
                    - XXL
                    - XXXL
                  sizeSystem: https://schema.org/WearableSizeSystemUS
                  sizeGroup: https://schema.org/WearableSizeGroupBig
      sku:
        description: The Stock Keeping Unit (SKU), i.e. a merchant-specific identifier
          for a product or service, or the product to which the offer refers.
        type: string
      slogan:
        description: A slogan or motto associated with the item.
        type: string
      specification:
        description: A specification of the product, often grouped by a section
          header/name. This is a cleaner alternative to additionalProperty for
          strict retail product specifications.
        type: array
        items:
          type: object
          properties:
            name:
              description: The name of the item.
              type: string
            value:
              description: >-
                The value of a QuantitativeValue (including Observation) or
                property value node.

                - For QuantitativeValue and MonetaryAmount, the recommended type
                for values is 'Number'.

                - For PropertyValue, it can be 'Text', 'Number', 'Boolean',
                'StructuredValue' or 'QualitativeValue'.

                - Use values from 0123456789 (Unicode 'DIGIT ZERO' (U+0030) to
                'DIGIT NINE' (U+0039)) rather than superficially similar Unicode
                symbols.

                - Use '.' (Unicode 'FULL STOP' (U+002E)) rather than ',' to
                indicate a decimal point. Avoid using these symbols as a
                readability separator.
              type: array
              items:
                anyOf:
                  - type: object
                    properties:
                      name:
                        description: The name of the item.
                        anyOf:
                          - type: array
                            items:
                              type: string
                          - type: string
                      sizeSystem:
                        description: The size system used to identify a product's size. Typically either
                          a standard (for example, "GS1" or "ISO-EN13402"),
                          country code (for example "US" or "JP"), or a
                          measuring system (for example "Metric" or "Imperial").
                        type: string
                      sizeGroup:
                        description: The size group (also known as "size type") for a product's size.
                          Size groups are common in the fashion industry to
                          define size segments and suggested audiences for
                          wearable products. Multiple values can be combined,
                          for example "men's big and tall", "petite maternity"
                          or "regular".
                        type: string
                    title: SizeSpecification
                    description: Size related properties of a product, typically a size code (name)
                      and optionally a sizeSystem, sizeGroup, and product
                      measurements (hasMeasurement). In addition, the intended
                      audience can be defined through suggestedAge,
                      suggestedGender, and suggested body measurements
                      (suggestedMeasurement).
                    examples:
                      - "@type": SizeSpecification
                        name:
                          - XS
                          - S
                        sizeSystem: https://schema.org/WearableSizeSystemUS
                        sizeGroup: https://schema.org/WearableSizeGroupPetite
                      - "@type": SizeSpecification
                        name:
                          - M
                          - L
                        sizeSystem: https://schema.org/WearableSizeSystemUS
                        sizeGroup: https://schema.org/WearableSizeGroupRegular
                      - "@type": SizeSpecification
                        name: XL
                        sizeSystem: https://schema.org/WearableSizeSystemUS
                        sizeGroup: https://schema.org/WearableSizeGroupPlus
                      - "@type": SizeSpecification
                        name:
                          - XXL
                          - XXXL
                        sizeSystem: https://schema.org/WearableSizeSystemUS
                        sizeGroup: https://schema.org/WearableSizeGroupBig
                  - type: string
                  - type: number
                  - type: "null"
            valueGroup:
              description: A header or section name for grouping related property values.
              type: string
            unitCode:
              description: The unit of measurement given using the UN/CEFACT Common Code (3
                characters) or a URL. Other codes than the UN/CEFACT Common Code
                may be used with a prefix followed by a colon.
              type: string
            unitText:
              description: A string or text indicating the unit of measurement. Useful if you
                cannot provide a standard unit code for unitCode.
              type: string
          title: PropertyValue
          description: A property-value pair, e.g. representing a feature of a product or
            place. Use the 'name' property for the name of the property. If
            there is an additional human-readable version of the value, put that
            into the 'description' property. Always use specific schema.org
            properties when a) they exist and b) you can populate them. Using
            PropertyValue as a substitute will typically not trigger the same
            effect as using the original, specific property.
          examples:
            - "@type": PropertyValue
              name: color
              value:
                - black
                - silver
            - "@type": PropertyValue
              name: material
              value:
                - plastic
                - aluminum
            - "@type": PropertyValue
              name: size
              value:
                - "@type": SizeSpecification
                  name:
                    - XS
                    - S
                  sizeSystem: https://schema.org/WearableSizeSystemUS
                  sizeGroup: https://schema.org/WearableSizeGroupPetite
                - "@type": SizeSpecification
                  name:
                    - M
                    - L
                  sizeSystem: https://schema.org/WearableSizeSystemUS
                  sizeGroup: https://schema.org/WearableSizeGroupRegular
                - "@type": SizeSpecification
                  name: XL
                  sizeSystem: https://schema.org/WearableSizeSystemUS
                  sizeGroup: https://schema.org/WearableSizeGroupPlus
                - "@type": SizeSpecification
                  name:
                    - XXL
                    - XXXL
                  sizeSystem: https://schema.org/WearableSizeSystemUS
                  sizeGroup: https://schema.org/WearableSizeGroupBig
      offers:
        description: An offer to provide this item—for example, an offer to sell a
          product, rent the DVD of a movie, perform a service, or give away
          tickets to an event. Use businessFunction to indicate the kind of
          transaction offered, i.e. sell, lease, etc. This property can also be
          used to describe a Demand. While this property is listed as expected
          on a number of common types, it can be used in others. In that case,
          using a second type, such as Product or a subtype of Product, can
          clarify the nature of the offer.
        type: array
        items:
          type: object
          properties:
            availability:
              description: The availability of this item—for example In stock, Out of stock,
                Pre-order, etc.
              anyOf:
                - type: string
                  const: Discontinued
                  description: Indicates that the item has been discontinued.
                - type: string
                  const: InStock
                  description: Indicates that the item is in stock.
                - type: string
                  const: LimitedAvailability
                  description: Indicates that the item has limited availability.
                - type: string
                  const: MadeToOrder
                  description: Indicates that the item is made to order (custom made).
                - type: string
                  const: OutOfStock
                  description: Indicates that the item is out of stock.
                - type: string
                  const: SoldOut
                  description: Indicates that the item has sold out.
              title: ItemAvailability
            condition:
              description: A predefined value from OfferItemCondition specifying the condition
                of the product or service, or the products or services included
                in the offer. Also used for product return policies to specify
                the condition of products accepted for returns.
              anyOf:
                - type: string
                  const: DamagedCondition
                  description: Indicates that the item is damaged.
                - type: string
                  const: NewCondition
                  description: Indicates that the item is new.
                - type: string
                  const: RefurbishedCondition
                  description: Indicates that the item is refurbished.
                - type: string
                  const: UsedCondition
                  description: Indicates that the item is used.
              title: ItemCondition
            category:
              description: A category for the item. Greater signs or slashes can be used to
                informally indicate a category hierarchy.
              anyOf:
                - type: object
                  properties:
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
                                (closed caption, subtitles etc.) use MediaObject
                                and indicate the encodingFormat.
                              type: string
                            author:
                              description: The author of this content or rating. Please note that author is
                                special in that HTML 5 provides a special
                                mechanism for indicating authorship via the rel
                                tag. That is equivalent to this and may be used
                                interchangeably.
                              type: string
                            contentUrl:
                              description: Actual bytes of the media object, for example the image file or
                                video file.
                              type: string
                            datePublished:
                              description: Date of first publication or broadcast. For example the date a
                                CreativeWork was broadcast or a Certification
                                was issued.
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
                                      (closed caption, subtitles etc.) use
                                      MediaObject and indicate the
                                      encodingFormat.
                                    type: string
                                  author:
                                    description: The author of this content or rating. Please note that author is
                                      special in that HTML 5 provides a special
                                      mechanism for indicating authorship via
                                      the rel tag. That is equivalent to this
                                      and may be used interchangeably.
                                    type: string
                                  contentUrl:
                                    description: Actual bytes of the media object, for example the image file or
                                      video file.
                                    type: string
                                  datePublished:
                                    description: Date of first publication or broadcast. For example the date a
                                      CreativeWork was broadcast or a
                                      Certification was issued.
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
                  title: CategoryCode
                  description: A Category Code.
                - type: array
                  items:
                    type: object
                    properties:
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
                                  (closed caption, subtitles etc.) use
                                  MediaObject and indicate the encodingFormat.
                                type: string
                              author:
                                description: The author of this content or rating. Please note that author is
                                  special in that HTML 5 provides a special
                                  mechanism for indicating authorship via the
                                  rel tag. That is equivalent to this and may be
                                  used interchangeably.
                                type: string
                              contentUrl:
                                description: Actual bytes of the media object, for example the image file or
                                  video file.
                                type: string
                              datePublished:
                                description: Date of first publication or broadcast. For example the date a
                                  CreativeWork was broadcast or a Certification
                                  was issued.
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
                                        (closed caption, subtitles etc.) use
                                        MediaObject and indicate the
                                        encodingFormat.
                                      type: string
                                    author:
                                      description: The author of this content or rating. Please note that author is
                                        special in that HTML 5 provides a
                                        special mechanism for indicating
                                        authorship via the rel tag. That is
                                        equivalent to this and may be used
                                        interchangeably.
                                      type: string
                                    contentUrl:
                                      description: Actual bytes of the media object, for example the image file or
                                        video file.
                                      type: string
                                    datePublished:
                                      description: Date of first publication or broadcast. For example the date a
                                        CreativeWork was broadcast or a
                                        Certification was issued.
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
                    title: CategoryCode
                    description: A Category Code.
                - type: string
                - type: array
                  items:
                    type: string
              title: Category
            eligibleQuantity:
              description: The interval and unit of measurement of ordering quantities for
                which the offer or price specification is valid. This allows
                e.g. specifying that a certain freight charge is valid only for
                a certain quantity.
              type: object
              properties:
                maxValue:
                  description: The upper value of some characteristic or property.
                  type: number
                minValue:
                  description: The lower value of some characteristic or property.
                  type: number
                value:
                  description: The value of a QuantitativeValue (including Observation) or
                    property value node.
                  type: number
              title: QuantitativeValue
            inventoryLevel:
              description: The current approximate inventory level for the item or items.
              type: object
              properties:
                maxValue:
                  description: The upper value of some characteristic or property.
                  type: number
                minValue:
                  description: The lower value of some characteristic or property.
                  type: number
                value:
                  description: The value of a QuantitativeValue (including Observation) or
                    property value node.
                  type: number
              title: QuantitativeValue
            price:
              title: Price
              description: >
                The offer price of a product, or of a price component when
                attached to PriceSpecification and its subtypes.


                Usage guidelines:


                - Use the priceCurrency property (with standard formats: ISO
                4217 currency format, e.g. "USD"; Ticker symbol for
                cryptocurrencies, e.g. "BTC"; well known names for Local
                Exchange Trading Systems (LETS) and other currency types, e.g.
                "Ithaca HOUR") instead of including ambiguous symbols such as
                '$' in the value.

                - Use '.' (Unicode 'FULL STOP' (U+002E)) rather than ',' to
                indicate a decimal point. Avoid using these symbols as a
                readability separator.

                - Note that both RDFa and Microdata syntax allow the use of a
                "content=" attribute for publishing simple machine-readable
                values alongside more human-friendly formatting.

                - Use values from 0123456789 (Unicode 'DIGIT ZERO' (U+0030) to
                'DIGIT NINE' (U+0039)) rather than superficially similar Unicode
                symbols.
              type:
                - number
                - string
            priceSpecification:
              type: array
              items:
                type: object
                properties:
                  price:
                    title: Price
                    description: The offer price of a product, or of a price component when attached
                      to PriceSpecification and its subtypes.
                    type:
                      - number
                      - string
                  priceCurrency:
                    type: string
                    description: The currency of the price, or a price component when attached to
                      PriceSpecification and its subtypes.
                  priceType:
                    description: Defines the type of a price specified for an offered product, for
                      example a list price, a (temporary) sale price or a
                      manufacturer suggested retail price. If multiple prices
                      are specified for an offer the priceType property can be
                      used to identify the type of each such specified price.
                      The value of priceType can be specified as a value from
                      enumeration PriceTypeEnumeration or, a UN/EDIFACT 5387
                      code, or as a free form text string for price types that
                      are not already predefined in PriceTypeEnumeration.
                    anyOf:
                      - type: string
                        const: ListPrice
                        description: Represents the list price of an offered product. Typically the same
                          as the MSRP.
                      - type: string
                        const: RegularPrice
                        description: Represents the regular price of an offered product. This is usually
                          the advertised price before a temporary sale. Once the
                          sale period ends the advertised price will go back to
                          the regular price.
                      - type: string
                        const: SalePrice
                        description: Represents a sale price (usually active for a limited period) of an
                          offered product.
                      - type: string
                        const: StrikethroughPrice
                        description: Represents the strikethrough price (the previous advertised price)
                          of an offered product.
                    title: PriceTypeEnumeration
                required:
                  - price
                  - priceCurrency
            priceCurrency:
              description: >-
                The currency of the price, or a price component when attached to
                PriceSpecification and its subtypes.


                Use standard formats: ISO 4217 currency format, e.g. "USD";
                Ticker symbol for cryptocurrencies, e.g. "BTC"; well known names
                for Local Exchange Trading Systems (LETS) and other currency
                types, e.g. "Ithaca HOUR".
              type: string
            priceValidUntil:
              description: The date after which the price is no longer available.
              type: string
              format: date
              pattern: ^(?:(?:\d\d[2468][048]|\d\d[13579][26]|\d\d0[48]|[02468][048]00|[13579][26]00)-02-29|\d{4}-(?:(?:0[13578]|1[02])-(?:0[1-9]|[12]\d|3[01])|(?:0[469]|11)-(?:0[1-9]|[12]\d|30)|(?:02)-(?:0[1-9]|1\d|2[0-8])))$
          title: Offer
          description: "An offer to transfer some rights to an item or to provide a
            service — for example, an offer to sell tickets to an event, to rent
            the DVD of a movie, to stream a TV show over the internet, to repair
            a motorcycle, or to loan a book. Note: As the businessFunction
            property, which identifies the form of offer (e.g. sell, lease,
            repair, dispose), defaults to http://purl.org/goodrelations/v1#Sell;
            an Offer without a defined businessFunction value can be assumed to
            be an offer to sell."
      potentialAction:
        description: Indicates a potential Action, which describes an idealized action
          in which this thing would play an 'object' role.
        type: array
        items:
          type: object
          properties:
            identifier:
              description: The identifier property represents any kind of identifier for any
                kind of Thing, such as ISBNs, GTIN codes, UUIDs etc. Schema.org
                provides dedicated properties for representing many of these,
                either as textual strings or as URL (URI) links. See background
                notes for more details.
              type: string
            name:
              description: The name of the item.
              type: string
            description:
              description: The description of the item.
              type: string
            target:
              description: Indicates a target EntryPoint, or url, for an Action.
              type: string
          title: Action
          description: An action performed by a direct agent and indirect participants
            upon a direct object. Optionally happens at a location with the help
            of an inanimate instrument. The execution of the action may produce
            a result. Specific action sub-type documentation specifies the exact
            expectation of each argument/role.
      url:
        description: URL of the item.
        type: string
    title: Product
    description: "Any offered product or service. For example: a pair of shoes; a
      concert ticket; the rental of a car; a haircut; or an episode of a TV show
      streamed online."
    examples:
      - "@context": https://schema.org/
        "@type": Product
        sku: 44E01-M11000
        inProductGroupWithID: "44E01"
        gtin14: "12345678901231"
        image: https://www.example.com/jacket_large_green.jpg
        name: Large green jacket
        description: Large wool green jacket for the winter months
        brand:
          "@type": Brand
          name: A fashion brand
        color: green
        size:
          "@type": SizeSpecification
          sizeSystem: https://schema.org/WearableSizeSystemUS
          sizeGroup:
            - https://schema.org/WearableSizeGroupMens
            - https://schema.org/WearableSizeGroupBig
            - https://schema.org/WearableSizeGroupTall
          name: 3XL
          hasMeasurement:
            - "@type": QuantitativeValue
              valueReference: https://schema.org/WearableMeasurementChestOrBust
              unitCode: INH
              value: 52
            - "@type": QuantitativeValue
              valueReference: https://schema.org/WearableMeasurementLength
              unitCode: INH
              value: 42
          suggestedGender: male
          suggestedAge:
            "@type": QuantitativeValue
            name: adult
            unitCode: ANN
            minValue: 13
          suggestedMeasurement:
            - "@type": QuantitativeValue
              valueReference: https://schema.org/BodyMeasurementChest
              unitCode: INH
              minValue: 51
              maxValue: 54
            - "@type": QuantitativeValue
              valueReference: https://schema.org/BodyMeasurementHeight
              unitCode: FOT
              minValue: 6
              maxValue: 6.3
        offers:
          "@type": Offer
          url: https://www.example.com/jacket?s=l&c=g
          priceCurrency: USD
          price: 239.99
          itemCondition: https://schema.org/NewCondition
          availability: https://schema.org/InStock
    required:
      - "@type"
---
A Schema.org Type

Thing > Product

Any offered product or service. For example: a pair of shoes; a concert ticket; the rental of a car; a haircut; or an episode of a TV show streamed online.