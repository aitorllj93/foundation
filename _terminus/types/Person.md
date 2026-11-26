---
kind: mdbase.type
name: Person
version: 1
description: A person (alive, dead, undead, or fictional).
collection:
  display:
    icon: "user"
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
      additionalName:
        description: An additional name for a Person, can be used for a middle name.
        type: string
      alternateName:
        description: An alias for the item.
        type: array
        items:
          type: string
      affiliation:
        description: An organization that this person is affiliated with. For example, a school/university, a club, or a team.
        type: array
        items:
          type: string
      alumniOf:
        description: "An organization that the person is an alumni of. Inverse property: alumni"
        type: array
        items:
          type: string
      award:
        description: An award won by or for this item.
        type: array
        items:
          type: string
      birthDate:
        description: Date of birth.
        type: string
      birthPlace:
        description: The place where the person was born.
        type: string
      children:
        description: A child of the person.
        type: array
        items:
          type: string
      colleague:
        description: A colleague of the person.
        type: array
        items:
          type: string
      deathDate:
        description: Date of death.
        type: string
      deathPlace:
        description: The place where the person died.
        type: string
      familyName:
        description: Family name. In the U.S., the last name of a Person.
        type: string
      follows:
        description: The most generic uni-directional social relation.
        type: array
        items:
          type: string
      gender:
        description: Gender of something, typically a Person, but possibly also fictional characters, animals, etc.
        type: string
      givenName:
        description: Given name. In the U.S., the first name of a Person.
        type: string
      hasOccupation:
        description: The Person's occupation. For past professions, use Role for expressing dates.
        type: array
        items:
          type: string
      height:
        description: The height of the item.
        type: string
      honorificPrefix:
        description: An honorific prefix preceding a Person's name such as Dr/Mrs/Mr.
        type: string
      honorificSuffix:
        description: An honorific suffix following a Person's name such as M.D./PhD/MSCSW.
        type: string
      identifier:
        description: The identifier property represents any kind of identifier for any
          kind of Thing, such as ISBNs, GTIN codes, UUIDs etc. Schema.org provides dedicated
          properties for representing many of these, either as textual strings or as URL
          (URI) links. See background notes for more details.
        type: array
        items:
          type: string
      jobTitle:
        description: The job title of the person (for example, Financial Manager).
        type: array
        items:
          type: string
      knows:
        description: The most generic uni-directional social relation.
        type: array
        items:
          type: string
      lifeEvent:
        description: A life event like baptism, communions, Bar Mitzvahs, Aqiqah, Namakarana, Miyamairi, burial, ....
        type: array
        items:
          type: string
      memberOf:
        description: "An Organization (or ProgramMembership) to which this Person or Organization belongs. Inverse property: member"
        type: array
        items:
          type: string
      name:
        description: The name of the item.
        type: string
      nationality:
        description: Nationality of the person.
        type: array
        items:
          type: string
      parent:
        description: A parent of this person. 
        type: array
        items:
          type: string
      performerIn:
        description: Event that this person is a performer or participant in.
        type: array
        items:
          type: string
      relatedTo:
        description: The most generic familial relation.
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
      sibling:
        description: A sibling of the person.
        type: array
        items:
          type: string
      skills:
        description: A statement of knowledge, skill, ability, task or any other assertion expressing a competency that is either claimed by a person, an organization or desired or required to fulfill a role or to work in an occupation..
        type: array
        items:
          type: string
      spouse:
        description: The person's spouse.
        type: array
        items:
          type: string
      weight:
        description: The weight of the product or person.
        type: array
        items:
          type: string
      worksFor:
        description: Organizations that the person works for.
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

Thing > Person

A person (alive, dead, undead, or fictional).
