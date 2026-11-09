
# STA Thing (Schema)

`ogc.api.sta.Thing` *v0.1*

A thing is an object of the physical world (physical things) or the information world (virtual things) that is capable of being identified and integrated into communication networks. [ITU-T Y.2060]

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## Thing

The OGC SensorThings API follows the ITU-T definition, i.e., with regard to the Internet of Things, a thing is an object of the physical world (physical things) or the information world (virtual things) that is capable of being identified and integrated into communication networks [ITU-T Y.2060].

### Limitations
For compliance with SwaggerHub where the schema can be referred:
- type of id is not specified, while it shall be string or number


## References

Requirements: [http://www.opengis.net/spec/iot_sensing/1.1/req/datamodel/thing](https://docs.ogc.org/is/18-088/18-088.html#thing)

## Examples

### Observation whose Datastream has an ObservationType of OM_Measurement. A result’s data type is defined by the observationType.
#### json
```json
{
  "@iot.id": 1,
  "@iot.selfLink": "http://example.org/v1.1/Things(1)",
  "Locations@iot.navigationLink": "Things(1)/Locations",
  "Datastreams@iot.navigationLink": "Things(1)/Datastreams",
  "HistoricalLocations@iot.navigationLink": "Things(1)/HistoricalLocations",

  "name": "Oven",
  "description": "This thing is an oven.",
  "properties": {
    "owner": "Noah Liang",
    "color": "Black"
  }
}

```

#### jsonld
```jsonld
{
  "@context": "https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/context.jsonld",
  "@iot.id": 1,
  "@iot.selfLink": "http://example.org/v1.1/Things(1)",
  "Locations@iot.navigationLink": "Things(1)/Locations",
  "Datastreams@iot.navigationLink": "Things(1)/Datastreams",
  "HistoricalLocations@iot.navigationLink": "Things(1)/HistoricalLocations",
  "name": "Oven",
  "description": "This thing is an oven.",
  "properties": {
    "owner": "Noah Liang",
    "color": "Black"
  }
}
```

#### ttl
```ttl
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix sosa-oms: <http://www.w3.org/ns/sosa/oms/> .

[] dcterms:coverage <http://w3id.org/ogcincubator/bblocks-sta/Things(1)/HistoricalLocations> ;
    dcterms:description "This thing is an oven." ;
    dcterms:spatial <http://w3id.org/ogcincubator/bblocks-sta/Things(1)/Locations> ;
    dcterms:title "Oven" ;
    sosa-oms:makesObservationCollection <http://w3id.org/ogcincubator/bblocks-sta/Things(1)/Datastreams> .


```

## Schema

```yaml
$schema: http://json-schema.org/draft-04/schema#
title: Observation object
description: Schema for Sensor things API 1.3 Observation
type: object
properties:
  '@iot.id':
    type:
    - string
    - number
    description: The Id of the observation
  '@iot.selfLink':
    type: string
    description: The direct link to the entity
    x-jsonld-id: http://www.opengis.net/def/rel/iana/1.0/self
    x-jsonld-type: '@id'
  parameters:
    type: object
  phenomenonTime:
    type: string
    description: The time when the observation happened. or Time Interval string (e.g.,
      2010-12-23T10:20:00.00-07:00 or 2010-12-23T10:20:00.00-07:00/2010-12-23T12:20:00.00-07:00)
  result:
    description: The estimated value of the observed property. Type depends on the
      observationType defined in the associated Datastream
  resultQuality:
    type: string
    description: A description of the quality of the result. Type DQ_Element.
  resultTime:
    type: string
    description: The time the result was generated. TM_Instant (ISO 8601 Time string)
  validTime:
    type: string
    description: The time period during which the result can be used. TM_Period (ISO
      8601 Time Interval string)
  Datastream@iot.navigationLink:
    type: string
    description: Reference link to the DataStream Definition.
  FeatureOfInterest@iot.navigationLink:
    type: string
    description: Reference link to the FeatureOfInterest.
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
x-jsonld-prefixes:
  dct: http://purl.org/dc/terms/
  sosa-oms: http://www.w3.org/ns/sosa/oms/
  orel: http://www.opengis.net/def/rel/
x-bblocks-metadata:
  itemIdentifier: ogc.api.sta.Thing
  register: https://british-oceanographic-data-centre.github.io/bblocks-sta/build/register.json
  version: '0.1'
  dateOfLastChange: '2026-11-09'

```

Links to the schema:

* YAML version: [schema.yaml](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/schema.json)
* JSON version: [schema.json](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
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
    "@iot.selfLink": {
      "@id": "orel:iana/1.0/self",
      "@type": "@id"
    },
    "dct": "http://purl.org/dc/terms/",
    "sosa-oms": "http://www.w3.org/ns/sosa/oms/",
    "orel": "http://www.opengis.net/def/rel/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/context.jsonld)

## Sources

* [OGC SensorThings API Part 1: Sensing Version 1.1](https://docs.ogc.org/is/18-088/18-088.html#thing)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/British-Oceanographic-Data-Centre/bblocks-sta](https://github.com/British-Oceanographic-Data-Centre/bblocks-sta)
* Path: `_sources/Thing`

