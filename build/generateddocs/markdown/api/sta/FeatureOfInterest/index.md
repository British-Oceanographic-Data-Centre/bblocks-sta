
# STA FeatureOfInterest (FOI) (Schema)

`ogc.api.sta.FeatureOfInterest` *v0.1*

Representation of the result of the FeatureOfInterest. 

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## What it represents

An Observation results in a value being assigned to a phenomenon. The phenomenon is a property of a feature, the latter being the FeatureOfInterest of the Observation [OGC and ISO 19156:2011]. In the context of the Internet of Things, many Observations’ FeatureOfInterest can be the Location of the Thing. For example, the FeatureOfInterest of a wifi-connect thermostat can be the Location of the thermostat (i.e., the living room where the thermostat is located in). In the case of remote sensing, the FeatureOfInterest can be the geographical area or volume that is being sensed.

### Limitations
For compliance with SwaggerHub where the schema can be referred:
- type of id is not specified, while it shall be string or number
- type of feature property is not specified, while it shall be string or object

## References

Requirements: [http://www.opengis.net/spec/iot_sensing/1.1/req/datamodel/feature-of-interest](https://docs.ogc.org/is/18-088/18-088.html#featureofinterest)

## Examples

### FeatureOfInterest basic example.
#### json
```json
{
  "@iot.id": 1,
  "@iot.selfLink": "http://example.org/v1.1/FeaturesOfInterest(1)",
  "Observations@iot.navigationLink": "FeaturesOfInterest(1)/Observations",

  "name": "Weather Station YYC.",
  "description": "This is a weather station located at the Calgary Airport.",
  "encodingType": "application/geo+json",
  "feature": {
    "type": "Feature",
    "geometry":{
      "type": "Point",
      "coordinates": [-114.06,51.05]
    }
  }
}

```

#### jsonld
```jsonld
{
  "@context": "https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/FeatureOfInterest/context.jsonld",
  "@iot.id": 1,
  "@iot.selfLink": "http://example.org/v1.1/FeaturesOfInterest(1)",
  "Observations@iot.navigationLink": "FeaturesOfInterest(1)/Observations",
  "name": "Weather Station YYC.",
  "description": "This is a weather station located at the Calgary Airport.",
  "encodingType": "application/geo+json",
  "feature": {
    "type": "Feature",
    "geometry": {
      "type": "Point",
      "coordinates": [
        -114.06,
        51.05
      ]
    }
  }
}
```

#### ttl
```ttl
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix geo: <http://www.opengis.net/ont/geosparql#> .
@prefix sosa: <http://www.w3.org/ns/sosa/> .

<http://w3id.org/ogcincubator/bblocks-sta/1> dcterms:description "This is a weather station located at the Calgary Airport." ;
    dcterms:format "application/geo+json" ;
    dcterms:title "Weather Station YYC." ;
    geo:hasGeometry [ a <http://w3id.org/ogcincubator/bblocks-sta/Feature> ] ;
    sosa:isFeatureOfInterestOf <http://w3id.org/ogcincubator/bblocks-sta/FeaturesOfInterest(1)/Observations> .


```

## Schema

```yaml
$schema: http://json-schema.org/draft-04/schema#
title: FeatureOfInterest object
description: Schema for Sensor things API 1.1 FeatureOfInterest
type: object
required:
- '@iot.id'
- '@iot.selfLink'
- name
- description
- encodingType
- feature
- Observations@iot.navigationLink
properties:
  '@iot.id':
    description: The Id of the Feature
    x-jsonld-id: '@id'
  '@iot.selfLink':
    type: string
    description: The direct link to the entity
    x-jsonld-id: http://www.opengis.net/def/rel/iana/1.0/self
  name:
    type: string
    description: A property provides a label for FeatureOfInterest entity, commonly
      a descriptive name.
    x-jsonld-id: http://purl.org/dc/terms/title
  description:
    type: string
    description: The description about the FeatureOfInterest.
    x-jsonld-id: http://purl.org/dc/terms/description
  encodingType:
    type: string
    description: The encoding type of the feature property. Its value is one of the
      ValueCode enumeration (see https://docs.ogc.org/is/18-088/18-088.html#tab-encodingtype-codes
      for the available ValueCode)..
    const: application/geo+json
    x-jsonld-id: http://purl.org/dc/terms/format
  feature:
    description: The detailed description of the feature. The data type is defined
      by encodingType.
    x-jsonld-id: http://www.opengis.net/ont/geosparql#hasGeometry
    x-jsonld-extra-terms:
      type: '@type'
      coordinates: http://www.opengis.net/ont/geosparql#asWKT
  properties:
    type: object
    description: optional properties for the feature.
  Observations@iot.navigationLink:
    type: string
    description: Reference link to the Observations.
    x-jsonld-id: http://www.w3.org/ns/sosa/isFeatureOfInterestOf
    x-jsonld-type: '@id'
x-jsonld-prefixes:
  orel: http://www.opengis.net/def/rel/
  dct: http://purl.org/dc/terms/
  geo: http://www.opengis.net/ont/geosparql#
  sosa: http://www.w3.org/ns/sosa/

```

Links to the schema:

* YAML version: [schema.yaml](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/FeatureOfInterest/schema.json)
* JSON version: [schema.json](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/FeatureOfInterest/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "@iot.id": "@id",
    "@iot.selfLink": "orel:iana/1.0/self",
    "name": "dct:title",
    "description": "dct:description",
    "encodingType": "dct:format",
    "feature": {
      "@context": {
        "type": "@type",
        "coordinates": "geo:asWKT"
      },
      "@id": "geo:hasGeometry"
    },
    "Observations@iot.navigationLink": {
      "@id": "sosa:isFeatureOfInterestOf",
      "@type": "@id"
    },
    "orel": "http://www.opengis.net/def/rel/",
    "dct": "http://purl.org/dc/terms/",
    "geo": "http://www.opengis.net/ont/geosparql#",
    "sosa": "http://www.w3.org/ns/sosa/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/FeatureOfInterest/context.jsonld)

## Sources

* [OGC SensorThings API Part 1: Sensing Version 1.1](https://docs.ogc.org/is/18-088/18-088.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/British-Oceanographic-Data-Centre/bblocks-sta](https://github.com/British-Oceanographic-Data-Centre/bblocks-sta)
* Path: `_sources/FeatureOfInterest`

