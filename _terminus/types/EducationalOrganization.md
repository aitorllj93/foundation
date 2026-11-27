---
kind: mdbase.type
name: EducationalOrganization
version: 1
description: An educational organization.
collection:
  display:
    icon: "mynaui:graduation-cap"
  "x-terminus":
    accent: amber
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
      alumni:
        description: "Alumni of an organization. Inverse property: alumniOf"
        type: array
        items:
          type: string
      areaServed:
        description: The geographic area where a service or offered item is provided. Supersedes serviceArea.
        type: array
        items:
          type: string
      authorizedRepresentative:
        description: An organization or person officially appointed to act on behalf of the manufacturer in a specific region or context.
        type: array
        items:
          type: string
      department:
        description: "A relationship between an organization and a department of that organization, also described as an organization (allowing different urls, logos, opening hours). For example: a store with a pharmacy, or a bakery with a cafe."
        type: array
        items:
          type: string
      description:
        description: A description of the item.
        type: string
      dissolutionDate:
        description: The date that this organization was dissolved.
        type: string
      employee:
        description: Someone working for this organization.
        type: array
        items:
          type: string
      event:
        description: Upcoming or past event associated with this place, organization, or action. Supersedes events.organization.
        type: array
        items:
          type: string
      founder:
        description: A person or organization who founded this organization. Supersedes founders.
        type: array
        items:
          type: string
      foundingDate:
        description: The date that this organization was founded.
        type: string
      foundingLocation:
        description: The place where the Organization was founded.
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
      keywords:
        description: Keywords or tags used to describe some item. Multiple textual entries in a keywords list are typically delimited by commas, or by repeating the property.
        type: array
        items:
          type: string
      legalName:
        description: The official name of the organization, e.g. the registered company name.
        type: string
      location:
        description: The location of, for example, where an event is happening, where an organization is located, or where an action takes place.
        type: array
        items:
          type: string
      logo:
        description: An associated logo.
        type: string
      member:
        description: "A member of an Organization or a ProgramMembership. Organizations can be members of organizations; ProgramMembership is typically for individuals.Inverse property: memberOf"
        type: array
        items:
          type: string
      memberOf:
        description: "An Organization (or ProgramMembership) to which this Person or Organization belongs.Inverse property: member"
        type: array
        items:
          type: string
      name:
        description: The name of the item.
        type: string
      parentOrganization:
        description: "The larger organization that this organization is a subOrganization of, if any. Inverse property: subOrganization."
        type: array
        items:
          type: string
      sameAs:
        description: URL of a reference Web page that unambiguously indicates the item's
          identity. E.g. the URL of the item's Wikipedia page, Wikidata entry, or official
          website.
        type: array
        items:
          type: string
      slogan:
        description: A slogan or motto associated with the item.
        type: string
      subOrganization:
        description: "A relationship between two organizations where the first includes the second, e.g., as a subsidiary. See also: the more specific 'department' property. Inverse property: parentOrganization"
        type: array
        items:
          type: string
      url:
        description: URL of the item.
        type: string
    required:
      - "@type"
---
A Schema.org Type

Thing > Place > CivicStructure > EducationalOrganization
Thing > Organization > EducationalOrganization

An educational organization.