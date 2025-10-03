
# STA HistoricalLocation (Schema)

`ogc.api.sta.HistoricalLocations` *v0.1*

A HistoricalLocation represents the association of a Thing with its Location(s) at a specific time. It provides the temporal context for where a Thing was located, enabling tracking of movement or changes in position.

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## HistoricalLocation

A HistoricalLocation represents the association of a Thing with a Location (or set of Locations) at a specific time. It allows the movement of Things, or changes in their position, to be tracked through time. Each HistoricalLocation links a Thing to one or more Locations and records the temporal information for that association.

STA HistoricalLocation is based on the concept from [OGC and ISO 19156:2001, OGC 10-004r3 and ISO 19156:2011(E), OGC Abstract Specification: Geographic information — Observations and Measurements.](http://portal.opengeospatial.org/files/?artifact_id=41579)

### Limitations
For compliance with SwaggerHub where the schema can be referred:
- type of id is not specified, while it shall be string or number
- type of metadata property is not specified, while it shall be string or object

## References

Requirements: [http://www.opengis.net/spec/iot_sensing/1.1/req/datamodel/historicallocation](https://docs.ogc.org/is/18-088/18-088.html#historicallocation)

## Examples

### A HistoricalLocation represents the association of a Thing with a Location (or set of Locations) at a specific time.
#### json
```json
{
  "@iot.id": 1,
  "@iot.selfLink": "http://example.org/v1.1/HistoricalLocations(1)",
  "time": "2024-09-01T12:00:00Z",
  "Thing@iot.navigationLink": "http://example.org/v1.1/HistoricalLocations(1)/Thing",
  "Locations@iot.navigationLink": "http://example.org/v1.1/HistoricalLocations(1)/Locations"
}

```

#### jsonld
```jsonld
{
  "@context": "https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/HistoricalLocations/context.jsonld",
  "@iot.id": 1,
  "@iot.selfLink": "http://example.org/v1.1/HistoricalLocations(1)",
  "time": "2024-09-01T12:00:00Z",
  "Thing@iot.navigationLink": "http://example.org/v1.1/HistoricalLocations(1)/Thing",
  "Locations@iot.navigationLink": "http://example.org/v1.1/HistoricalLocations(1)/Locations"
}
```

#### ttl
```ttl
@prefix geo: <http://www.opengis.net/ont/geosparql#> .
@prefix prov: <http://www.w3.org/ns/prov#> .

<http://w3id.org/ogcincubator/bblocks-sta/1> geo:hasGeometry <http://example.org/v1.1/HistoricalLocations(1)/Locations> ;
    prov:entity <http://example.org/v1.1/HistoricalLocations(1)/Thing> ;
    prov:startedAtTime "2024-09-01T12:00:00Z" .


```

## Schema

```yaml
$schema: http://json-schema.org/draft-04/schema#
title: HistoricalLocation object
description: Schema for HistoricalLocation entity in OGC SensorThings API 1.3
type: object
properties:
  '@iot.id':
    description: The Id of the HistoricalLocation
    x-jsonld-id: '@id'
  '@iot.selfLink':
    type: string
    description: The direct link to the HistoricalLocation entity
    x-jsonld-id: http://www.opengis.net/def/rel/iana/1.0/self
  time:
    type: string
    format: date-time
    description: The time when the Thing was at the Location (PROV startedAtTime).
    x-jsonld-id: http://www.w3.org/ns/prov#startedAtTime
  Thing@iot.navigationLink:
    type: string
    description: Reference link to the related Thing entity
    x-jsonld-id: http://www.w3.org/ns/prov#entity
    x-jsonld-type: '@id'
  Locations@iot.navigationLink:
    type: string
    description: Reference link to the related Location entities
    x-jsonld-id: http://www.opengis.net/ont/geosparql#hasGeometry
    x-jsonld-type: '@id'
required:
- '@iot.id'
- '@iot.selfLink'
- Thing@iot.navigationLink
- Locations@iot.navigationLink
x-jsonld-prefixes:
  orel: http://www.opengis.net/def/rel/
  prov: http://www.w3.org/ns/prov#
  geo: http://www.opengis.net/ont/geosparql#

```

Links to the schema:

* YAML version: [schema.yaml](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/HistoricalLocations/schema.json)
* JSON version: [schema.json](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/HistoricalLocations/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "@iot.id": "@id",
    "@iot.selfLink": "orel:iana/1.0/self",
    "time": "prov:startedAtTime",
    "Thing@iot.navigationLink": {
      "@id": "prov:entity",
      "@type": "@id"
    },
    "Locations@iot.navigationLink": {
      "@id": "geo:hasGeometry",
      "@type": "@id"
    },
    "orel": "http://www.opengis.net/def/rel/",
    "prov": "http://www.w3.org/ns/prov#",
    "geo": "http://www.opengis.net/ont/geosparql#",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/HistoricalLocations/context.jsonld)

## Sources

* [OGC SensorThings API Part 1: Sensing Version 1.1](https://docs.ogc.org/is/18-088/18-088.html#historicallocation)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/British-Oceanographic-Data-Centre/bblocks-sta](https://github.com/British-Oceanographic-Data-Centre/bblocks-sta)
* Path: `_sources/HistoricalLocations`

