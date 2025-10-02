
# STA ObservedProperty (Schema)

`ogc.api.sta.ObservedProperty` *v0.1*

An ObservedProperty specifies the phenomenon of an Observation. It defines what is being observed or measured, typically referenced using a URI from a controlled vocabulary or ontology.

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## ObservedProperty

An ObservedProperty specifies the phenomenon of an Observation. It defines what is being observed or measured (e.g., temperature, concentration, water level). The ObservedProperty is typically identified by a URI that points to a definition in a controlled vocabulary or ontology to ensure semantic clarity and interoperability.

##### Needs to be change from here
STA sensor is based on the concept from [OGC and ISO 19156:2001, OGC 10-004r3 and ISO 19156:2011(E), OGC Abstract Specification: Geographic information — Observations and Measurements.](http://portal.opengeospatial.org/files/?artifact_id=41579)

### Limitations
For compliance with SwaggerHub where the schema can be referred:
- type of id is not specified, while it shall be string or number
- type of metadata property is not specified, while it shall be string or object

##### Till here


## References

Requirements: [http://www.opengis.net/spec/iot_sensing/1.1/req/datamodel/observedproperty](https://docs.ogc.org/is/18-088/18-088.html#observedproperty)

## Examples

### ObservedProperty specifies the phenomenon of an Observation. It defines what is being observed or measured.
#### json
```json
{
  "@iot.selfLink": "http://example.org/v1.1/ObservedProperties(1)",
  "@iot.id": 1,
  "name": "air_temperature",
  "definition": "http://vocab.nerc.ac.uk/collection/P07/current/CFSN0023/",
  "description": "Air temperature is the bulk temperature of the air, not the surface (skin) temperature.",
  "Datastreams@iot.navigationLink": "http://example.org/v1.1/ObservedProperties(1)/Datastreams"
}

```

#### jsonld
```jsonld
{
  "@context": "https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/ObservedProperty/context.jsonld",
  "@iot.selfLink": "http://example.org/v1.1/ObservedProperties(1)",
  "@iot.id": 1,
  "name": "air_temperature",
  "definition": "http://vocab.nerc.ac.uk/collection/P07/current/CFSN0023/",
  "description": "Air temperature is the bulk temperature of the air, not the surface (skin) temperature.",
  "Datastreams@iot.navigationLink": "http://example.org/v1.1/ObservedProperties(1)/Datastreams"
}
```

#### ttl
```ttl
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix sosa: <http://www.w3.org/ns/sosa/> .

<http://w3id.org/ogcincubator/bblocks-sta/1> dcterms:description "Air temperature is the bulk temperature of the air, not the surface (skin) temperature." ;
    dcterms:title "air_temperature" ;
    sosa:definition <http://vocab.nerc.ac.uk/collection/P07/current/CFSN0023/> ;
    sosa:isObservedBy <http://example.org/v1.1/ObservedProperties(1)/Datastreams> .


```

## Schema

```yaml
$schema: http://json-schema.org/draft-04/schema#
title: ObservedProperty object
description: Schema for ObservedProperty entity in OGC SensorThings API 1.3
type: object
properties:
  '@iot.id':
    description: The Id of the ObservedProperty
    x-jsonld-id: '@id'
  '@iot.selfLink':
    type: string
    description: The direct link to the ObservedProperty entity
    x-jsonld-id: http://www.opengis.net/def/rel/iana/1.0/self
  name:
    type: string
    description: A label for the ObservedProperty, commonly a short descriptive name.
    x-jsonld-id: http://purl.org/dc/terms/title
  definition:
    type: string
    format: uri
    description: A URI that defines the observed phenomenon (e.g., from a controlled
      vocabulary or ontology).
    x-jsonld-id: http://www.w3.org/ns/sosa/definition
    x-jsonld-type: '@id'
  description:
    type: string
    description: Detailed description of the ObservedProperty.
    x-jsonld-id: http://purl.org/dc/terms/description
  properties:
    type: object
    description: A JSON Object containing user-annotated properties as key-value pairs.
    x-jsonld-id: https://schema.org/additionalProperty
    x-jsonld-extra-terms:
      name: https://schema.org/name
      value: https://schema.org/value
      unit: http://qudt.org/schema/qudt/unit
  Datastreams@iot.navigationLink:
    type: string
    description: Reference link to related Datastream entities.
    x-jsonld-id: http://www.w3.org/ns/sosa/isObservedBy
    x-jsonld-type: '@id'
required:
- '@iot.id'
- '@iot.selfLink'
- name
- definition
- description
- properties
x-jsonld-prefixes:
  orel: http://www.opengis.net/def/rel/
  dct: http://purl.org/dc/terms/
  sosa: http://www.w3.org/ns/sosa/
  sdo: https://schema.org/
  qudt: http://qudt.org/schema/qudt/

```

Links to the schema:

* YAML version: [schema.yaml](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/ObservedProperty/schema.json)
* JSON version: [schema.json](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/ObservedProperty/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "@iot.id": "@id",
    "@iot.selfLink": "orel:iana/1.0/self",
    "name": "dct:title",
    "definition": {
      "@id": "sosa:definition",
      "@type": "@id"
    },
    "description": "dct:description",
    "properties": {
      "@context": {
        "name": "sdo:name",
        "value": "sdo:value",
        "unit": "qudt:unit"
      },
      "@id": "sdo:additionalProperty"
    },
    "Datastreams@iot.navigationLink": {
      "@id": "sosa:isObservedBy",
      "@type": "@id"
    },
    "orel": "http://www.opengis.net/def/rel/",
    "dct": "http://purl.org/dc/terms/",
    "sosa": "http://www.w3.org/ns/sosa/",
    "sdo": "https://schema.org/",
    "qudt": "http://qudt.org/schema/qudt/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/ObservedProperty/context.jsonld)

## Sources

* [OGC SensorThings API Part 1: Sensing Version 1.1](https://docs.ogc.org/is/18-088/18-088.html#observedproperty)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/British-Oceanographic-Data-Centre/bblocks-sta](https://github.com/British-Oceanographic-Data-Centre/bblocks-sta)
* Path: `_sources/ObservedProperty`

