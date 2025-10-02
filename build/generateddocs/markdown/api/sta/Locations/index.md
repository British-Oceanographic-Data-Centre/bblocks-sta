
# STA Location (Schema)

`ogc.api.sta.Locations` *v0.1*

A Location represents the spatial position of a Thing. Locations are encoded using a geometry, typically expressed in GeoJSON, and may include descriptive metadata. Locations can be associated with one or more Things and tracked historically through HistoricalLocations.

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## Location

A Location represents the spatial position of a Thing. It describes where a Thing is situated, using a geometry (commonly encoded in GeoJSON) and may also include descriptive metadata and user-defined properties. A Thing may have multiple Locations, and the association between a Thing and its Locations can change over time, tracked via HistoricalLocations.

##### Needs to be change from here
STA sensor is based on the concept from [OGC and ISO 19156:2001, OGC 10-004r3 and ISO 19156:2011(E), OGC Abstract Specification: Geographic information — Observations and Measurements.](http://portal.opengeospatial.org/files/?artifact_id=41579)

### Limitations
For compliance with SwaggerHub where the schema can be referred:
- type of id is not specified, while it shall be string or number
- type of metadata property is not specified, while it shall be string or object

##### Till here


## References

Requirements: [http://www.opengis.net/spec/iot_sensing/1.1/req/datamodel/Location](https://docs.ogc.org/is/18-088/18-088.html#location)

## Examples

### A Location represents the spatial position of a Thing. It describes where a Thing is situated, using a geometry.
#### json
```json
{
  "@iot.id": 1,
  "@iot.selfLink": "http://example.org/v1.1/Locations(101)",
  "name": "BODC Test Site A",
  "description": "Test monitoring station located on the coast near Liverpool.",
  "encodingType": "application/vnd.geo+json",
  "location": {
    "type": "Point",
    "coordinates": [-3.0005, 53.4002]
  },
  "HistoricalLocations@iot.navigationLink": "http://example.org/v1.1/Locations(101)/HistoricalLocations",
  "Things@iot.navigationLink": "http://example.org/v1.1/Locations(101)/Things"
}

```

#### jsonld
```jsonld
{
  "@context": "https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Locations/context.jsonld",
  "@iot.id": 1,
  "@iot.selfLink": "http://example.org/v1.1/Locations(101)",
  "name": "BODC Test Site A",
  "description": "Test monitoring station located on the coast near Liverpool.",
  "encodingType": "application/vnd.geo+json",
  "location": {
    "type": "Point",
    "coordinates": [
      -3.0005,
      53.4002
    ]
  },
  "HistoricalLocations@iot.navigationLink": "http://example.org/v1.1/Locations(101)/HistoricalLocations",
  "Things@iot.navigationLink": "http://example.org/v1.1/Locations(101)/Things"
}
```

#### ttl
```ttl
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix geo: <http://www.opengis.net/ont/geosparql#> .
@prefix prov: <http://www.w3.org/ns/prov#> .
@prefix sosa: <http://www.w3.org/ns/sosa/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<http://w3id.org/ogcincubator/bblocks-sta/1> dcterms:description "Test monitoring station located on the coast near Liverpool." ;
    dcterms:format "application/vnd.geo+json" ;
    dcterms:title "BODC Test Site A" ;
    geo:hasGeometry [ a <http://w3id.org/ogcincubator/bblocks-sta/Point> ;
            geo:asWKT -3.0005e+00,
                5.34002e+01 ] ;
    prov:hadLocation <http://example.org/v1.1/Locations(101)/HistoricalLocations> ;
    sosa:hosts <http://example.org/v1.1/Locations(101)/Things> .


```

## Schema

```yaml
$schema: http://json-schema.org/draft-04/schema#
title: Locations object
description: Schema for Locations entity in OGC SensorThings API 1.3
type: object
properties:
  '@iot.id':
    description: The Id of the Location
    x-jsonld-id: '@id'
  '@iot.selfLink':
    type: string
    description: The direct link to the Location entity
    x-jsonld-id: http://www.opengis.net/def/rel/iana/1.0/self
  name:
    type: string
    description: A label for the Location, commonly a short descriptive name.
    x-jsonld-id: http://purl.org/dc/terms/title
  description:
    type: string
    description: Description of the Location entity.
    x-jsonld-id: http://purl.org/dc/terms/description
  encodingType:
    type: string
    description: The encoding type of the metadata property. Its value is one of the
      ValueCode enumeration (see Table 15 for the available ValueCode).
    x-jsonld-id: http://purl.org/dc/terms/format
  location:
    type: object
    description: A JSON object that describes the geometry of the Location.
    x-jsonld-id: http://www.opengis.net/ont/geosparql#hasGeometry
    x-jsonld-extra-terms:
      type: '@type'
      coordinates: http://www.opengis.net/ont/geosparql#asWKT
  properties:
    type: object
    description: A JSON Object containing user-annotated properties as key-value pairs.
    x-jsonld-id: https://schema.org/additionalProperty
    x-jsonld-extra-terms:
      altitude:
        x-jsonld-id: http://www.w3.org/ns/sosa/hasResult
        x-jsonld-context:
          value: https://schema.org/value
          reference: http://purl.org/dc/terms/description
          unitOfMeasurement:
            '@id': http://qudt.org/schema/qudt/unit
            '@context':
              name: https://schema.org/name
              symbol: https://schema.org/symbol
              definition: '@id'
      mountingPoint: https://schema.org/location
      platformType: https://schema.org/additionalType
  HistoricalLocations@iot.navigationLink:
    type: string
    formats: uri
    description: Reference link to related HistoricalLocation entities.
    x-jsonld-id: http://www.w3.org/ns/prov#hadLocation
    x-jsonld-type: '@id'
  Things@iot.navigationLink:
    type: string
    formats: uri
    description: Reference link to related Thing entities.
    x-jsonld-id: http://www.w3.org/ns/sosa/hosts
    x-jsonld-type: '@id'
x-jsonld-prefixes:
  orel: http://www.opengis.net/def/rel/
  dct: http://purl.org/dc/terms/
  geo: http://www.opengis.net/ont/geosparql#
  sdo: https://schema.org/
  sosa: http://www.w3.org/ns/sosa/
  qudt: http://qudt.org/schema/qudt/
  prov: http://www.w3.org/ns/prov#

```

Links to the schema:

* YAML version: [schema.yaml](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Locations/schema.json)
* JSON version: [schema.json](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Locations/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "@iot.id": "@id",
    "@iot.selfLink": "orel:iana/1.0/self",
    "name": "dct:title",
    "description": "dct:description",
    "encodingType": "dct:format",
    "location": {
      "@context": {
        "type": "@type",
        "coordinates": "geo:asWKT"
      },
      "@id": "geo:hasGeometry"
    },
    "properties": {
      "@context": {
        "altitude": {
          "@id": "sosa:hasResult",
          "@context": {
            "value": "sdo:value",
            "reference": "dct:description",
            "unitOfMeasurement": {
              "@id": "qudt:unit",
              "@context": {
                "name": "sdo:name",
                "symbol": "sdo:symbol",
                "definition": "@id"
              }
            }
          }
        },
        "mountingPoint": "sdo:location",
        "platformType": "sdo:additionalType"
      },
      "@id": "sdo:additionalProperty"
    },
    "HistoricalLocations@iot.navigationLink": {
      "@id": "prov:hadLocation",
      "@type": "@id"
    },
    "Things@iot.navigationLink": {
      "@id": "sosa:hosts",
      "@type": "@id"
    },
    "orel": "http://www.opengis.net/def/rel/",
    "dct": "http://purl.org/dc/terms/",
    "geo": "http://www.opengis.net/ont/geosparql#",
    "sdo": "https://schema.org/",
    "sosa": "http://www.w3.org/ns/sosa/",
    "qudt": "http://qudt.org/schema/qudt/",
    "prov": "http://www.w3.org/ns/prov#",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Locations/context.jsonld)

## Sources

* [OGC SensorThings API Part 1: Sensing Version 1.1](https://docs.ogc.org/is/18-088/18-088.html#location)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/British-Oceanographic-Data-Centre/bblocks-sta](https://github.com/British-Oceanographic-Data-Centre/bblocks-sta)
* Path: `_sources/Locations`

