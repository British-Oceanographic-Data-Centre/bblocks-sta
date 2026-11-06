
# STA Thing Properties Context (Schema)

`ogc.api.sta.Thing.Properties` *v0.1*

JSON-LD context applied to each SensorThings API Thing occurrence.

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## SensorThings API Thing occurrence context

This building block defines the JSON-LD mappings applied to each Thing
occurrence, including its name, description, self link, and navigation links.

The parent Thing context supplies the shared top-level `properties` mapping.

## Examples

### SensorThings API Thing occurrence
#### json
```json
{
  "@iot.id": 1,
  "@iot.selfLink": "http://example.org/v1.1/Things(1)",
  "name": "Oven",
  "description": "This thing is an oven.",
  "Locations@iot.navigationLink": "http://example.org/v1.1/Things(1)/Locations",
  "Datastreams@iot.navigationLink": "http://example.org/v1.1/Things(1)/Datastreams",
  "HistoricalLocations@iot.navigationLink": "http://example.org/v1.1/Things(1)/HistoricalLocations"
}

```

#### jsonld
```jsonld
{
  "@context": "https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/Properties/context.jsonld",
  "@iot.id": 1,
  "@iot.selfLink": "http://example.org/v1.1/Things(1)",
  "name": "Oven",
  "description": "This thing is an oven.",
  "Locations@iot.navigationLink": "http://example.org/v1.1/Things(1)/Locations",
  "Datastreams@iot.navigationLink": "http://example.org/v1.1/Things(1)/Datastreams",
  "HistoricalLocations@iot.navigationLink": "http://example.org/v1.1/Things(1)/HistoricalLocations"
}
```

#### ttl
```ttl
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix sosa-oms: <http://www.w3.org/ns/sosa/oms/> .

[] dcterms:coverage <http://example.org/v1.1/Things(1)/HistoricalLocations> ;
    dcterms:description "This thing is an oven." ;
    dcterms:spatial <http://example.org/v1.1/Things(1)/Locations> ;
    dcterms:title "Oven" ;
    sosa-oms:makesObservationCollection <http://example.org/v1.1/Things(1)/Datastreams> .


```

## Schema

```yaml
$schema: http://json-schema.org/draft-04/schema#
title: SensorThings API Thing occurrence
description: A Thing occurrence using the entity-level JSON-LD context.
allOf:
- $ref: https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/schema.yaml
x-jsonld-extra-terms:
  name: http://purl.org/dc/terms/title
  description: http://purl.org/dc/terms/description
  HistoricalLocations@iot.navigationLink:
    x-jsonld-id: http://purl.org/dc/terms/coverage
    x-jsonld-type: '@id'
  Locations@iot.navigationLink:
    x-jsonld-id: http://purl.org/dc/terms/spatial
    x-jsonld-type: '@id'
  Datastreams@iot.navigationLink:
    x-jsonld-id: http://www.w3.org/ns/sosa/oms/makesObservationCollection
    x-jsonld-type: '@id'
  '@iot.selfLink':
    x-jsonld-id: http://www.opengis.net/def/rel/iana/1.0/self
    x-jsonld-type: '@id'
x-jsonld-prefixes:
  dct: http://purl.org/dc/terms/
  sosa-oms: http://www.w3.org/ns/sosa/oms/
  orel: http://www.opengis.net/def/rel/
  sosa: http://www.w3.org/ns/sosa/
x-bblocks-metadata:
  itemIdentifier: ogc.api.sta.Thing.Properties
  register: https://british-oceanographic-data-centre.github.io/bblocks-sta/build/register.json
  version: '0.1'
  dateOfLastChange: '2026-11-06'

```

Links to the schema:

* YAML version: [schema.yaml](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/Properties/schema.json)
* JSON version: [schema.json](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/Properties/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "properties": {
      "@id": "sdo:additionalProperty",
      "@context": {
        "category": "sdo:category",
        "identifier": "sdo:identifier",
        "provider": "sdo:provider",
        "name": "sdo:name",
        "termCode": "sdo:termCode",
        "inDefinedTermSet": "sdo:inDefinedTermSet",
        "value": "sdo:value",
        "propertyID": "sdo:propertyID"
      }
    },
    "@iot.selfLink": {
      "@id": "orel:iana/1.0/self",
      "@type": "@id"
    },
    "name": "dct:title",
    "description": "dct:description",
    "HistoricalLocations@iot.navigationLink": {
      "@id": "dct:coverage",
      "@type": "@id"
    },
    "Locations@iot.navigationLink": {
      "@id": "dct:spatial",
      "@type": "@id"
    },
    "Datastreams@iot.navigationLink": {
      "@id": "sosa-oms:makesObservationCollection",
      "@type": "@id"
    },
    "sdo": "https://schema.org/",
    "dct": "http://purl.org/dc/terms/",
    "sosa-oms": "sosa:oms/",
    "orel": "http://www.opengis.net/def/rel/",
    "sosa": "http://www.w3.org/ns/sosa/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/Properties/context.jsonld)

## Sources

* [OGC SensorThings API Part 1: Sensing Version 1.1](https://docs.ogc.org/is/18-088/18-088.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/British-Oceanographic-Data-Centre/bblocks-sta](https://github.com/British-Oceanographic-Data-Centre/bblocks-sta)
* Path: `_sources/Thing/Properties`

