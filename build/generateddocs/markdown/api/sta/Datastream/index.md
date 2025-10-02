
# STA Datastream (Schema)

`ogc.api.sta.Datastream` *v0.1*

Metadata about a coherent set of observations, linked to value stream. [OGC 10-004r3 / ISO 19156:2011]

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## What it represents

A Datastream groups a collection of Observations measuring the same ObservedProperty and produced by the same Sensor. [https://docs.ogc.org/is/18-088/18-088.html#datastream].

Datastreams may be raw values or observation objects inheriting common property values from the Datastream description.

### Limitations

Observations navigation link is to an array of observation properties. This requires an extra schema element to navigate the relationship between OMS/SOSA ObservationCollection and the set of observations as direct members. 

## References

Requirements: [http://www.opengis.net/spec/iot_sensing/1.1/req/datamodel#datastream](https://docs.ogc.org/is/18-088/18-088.html#datastream)

## Examples

### Observation whose Datastream has an ObservationType of OM_Measurement. A result’s data type is defined by the observationType.
#### json
```json
    {
      "unitOfMeasurement": {
        "name": "Unitless",
        "definition": "http://qudt.org/schema/qudt/UNITLESS"
      },
      "description": "The datastream of jf2024 by sensor: 2e92962c0b6996add9517e4242ea9bdc for observed property: Jelly Fish Abundance Property",
      "name": "2e92962c0b6996add9517e4242ea9bdc:d2511e0ff7ac61981c6051a52b51f05c",
      "observationType": "http://www.opengis.net/def/observationType/OGC-OM/2.0/OM_Measurement",
      "@iot.id": "2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c",
      "@iot.selfLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)",
      "Observations@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/Observations",
      "ObservedProperty@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/ObservedProperty",
      "Sensor@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/Sensor",
      "Thing@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/Thing"
    }

```

#### jsonld
```jsonld
{
  "@context": "https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream/context.jsonld",
  "unitOfMeasurement": {
    "name": "Unitless",
    "definition": "http://qudt.org/schema/qudt/UNITLESS"
  },
  "description": "The datastream of jf2024 by sensor: 2e92962c0b6996add9517e4242ea9bdc for observed property: Jelly Fish Abundance Property",
  "name": "2e92962c0b6996add9517e4242ea9bdc:d2511e0ff7ac61981c6051a52b51f05c",
  "observationType": "http://www.opengis.net/def/observationType/OGC-OM/2.0/OM_Measurement",
  "@iot.id": "2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c",
  "@iot.selfLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)",
  "Observations@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/Observations",
  "ObservedProperty@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/ObservedProperty",
  "Sensor@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/Sensor",
  "Thing@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/Thing"
}
```

#### ttl
```ttl
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix qudt: <http://qudt.org/schema/qudt/> .
@prefix schema: <https://schema.org/> .
@prefix sosa: <http://www.w3.org/ns/sosa/> .

<http://w3id.org/ogcincubator/bblocks-sta/2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c> dcterms:description "The datastream of jf2024 by sensor: 2e92962c0b6996add9517e4242ea9bdc for observed property: Jelly Fish Abundance Property" ;
    dcterms:title "2e92962c0b6996add9517e4242ea9bdc:d2511e0ff7ac61981c6051a52b51f05c" ;
    qudt:unit qudt:UNITLESS ;
    sosa:Observation <http://www.opengis.net/def/observationType/OGC-OM/2.0/OM_Measurement> ;
    sosa:hasMember <https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/Observations> ;
    sosa:madeByPlatform <https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/Thing> ;
    sosa:madeBySensor <https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/Sensor> ;
    sosa:observedProperty <https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/ObservedProperty> .

qudt:UNITLESS schema:name "Unitless" .


```

## Schema

```yaml
$schema: http://json-schema.org/draft-04/schema#
title: Datastream object
description: Schema for Sensor things API 1.3 Datastream, inferred from OpenAPI implementations
type: object
properties:
  '@iot.id':
    type:
    - string
    - number
    description: The Id of the observation
    x-jsonld-id: '@id'
  '@iot.selfLink':
    type: string
    description: The direct link to the entity
    x-jsonld-id: http://www.opengis.net/def/rel/iana/1.0/self
  Observations@iot.navigationLink:
    type: string
    description: Reference link to stream of Observations.
    x-jsonld-id: http://www.w3.org/ns/sosa/hasMember
    x-jsonld-type: '@id'
x-jsonld-extra-terms:
  name: http://purl.org/dc/terms/title
  description: http://purl.org/dc/terms/description
  observationType:
    x-jsonld-id: http://www.w3.org/ns/sosa/Observation
    x-jsonld-type: '@id'
  unitOfMeasurement:
    x-jsonld-id: http://qudt.org/schema/qudt/unit
    x-jsonld-context:
      name: https://schema.org/name
      symbol: https://schema.org/symbol
      definition: '@id'
  observedArea: http://www.opengis.net/ont/geosparql#hasGeometry
  phenomenonTime: http://www.w3.org/ns/sosa/phenomenonTime
  resultTime: http://www.w3.org/ns/sosa/resultTime
  properties:
    x-jsonld-id: https://schema.org/additionalProperty
    x-jsonld-context:
      hasSystemProperty: http://www.w3.org/ns/ssn/system/hasSystemProperty
      status: https://schema.org/PropertyValue
      name: https://schema.org/name
      category: https://schema.org/CategoryCode
      termCode: https://schema.org/termCode
      inDefinedTermSet: https://schema.org/inDefinedTermSet
      provider: https://schema.org/Organization
      value: https://schema.org/value
      unitCode: '@id'
      unitText: https://schema.org/unitText
      description: http://purl.org/dc/terms/description
  ObservedProperty@iot.navigationLink:
    x-jsonld-id: http://www.w3.org/ns/sosa/observedProperty
    x-jsonld-type: '@id'
  Sensor@iot.navigationLink:
    x-jsonld-id: http://www.w3.org/ns/sosa/madeBySensor
    x-jsonld-type: '@id'
  Thing@iot.navigationLink:
    x-jsonld-id: http://www.w3.org/ns/sosa/madeByPlatform
    x-jsonld-type: '@id'
x-jsonld-prefixes:
  orel: http://www.opengis.net/def/rel/
  dct: http://purl.org/dc/terms/
  sosa: http://www.w3.org/ns/sosa/
  qudt: http://qudt.org/schema/qudt/
  sdo: https://schema.org/
  geo: http://www.opengis.net/ont/geosparql#
  ssn-system: http://www.w3.org/ns/ssn/system/
  prov: http://www.w3.org/ns/prov#
  sta: https://schemas.opengis.org/sta/def/core#

```

Links to the schema:

* YAML version: [schema.yaml](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream/schema.json)
* JSON version: [schema.json](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "name": "dct:title",
    "description": "dct:description",
    "observationType": {
      "@id": "sosa:Observation",
      "@type": "@id"
    },
    "unitOfMeasurement": {
      "@id": "qudt:unit",
      "@context": {
        "name": "sdo:name",
        "symbol": "sdo:symbol",
        "definition": "@id"
      }
    },
    "observedArea": "geo:hasGeometry",
    "phenomenonTime": "sosa:phenomenonTime",
    "resultTime": "sosa:resultTime",
    "properties": {
      "@id": "sdo:additionalProperty",
      "@context": {
        "hasSystemProperty": "ssn-system:hasSystemProperty",
        "status": "sdo:PropertyValue",
        "name": "sdo:name",
        "category": "sdo:CategoryCode",
        "termCode": "sdo:termCode",
        "inDefinedTermSet": "sdo:inDefinedTermSet",
        "provider": "sdo:Organization",
        "value": "sdo:value",
        "unitCode": "@id",
        "unitText": "sdo:unitText"
      }
    },
    "ObservedProperty@iot.navigationLink": {
      "@id": "sosa:observedProperty",
      "@type": "@id"
    },
    "Sensor@iot.navigationLink": {
      "@id": "sosa:madeBySensor",
      "@type": "@id"
    },
    "Thing@iot.navigationLink": {
      "@id": "sosa:madeByPlatform",
      "@type": "@id"
    },
    "@iot.id": "@id",
    "@iot.selfLink": "orel:iana/1.0/self",
    "Observations@iot.navigationLink": {
      "@id": "sosa:hasMember",
      "@type": "@id"
    },
    "orel": "http://www.opengis.net/def/rel/",
    "dct": "http://purl.org/dc/terms/",
    "sosa": "http://www.w3.org/ns/sosa/",
    "qudt": "http://qudt.org/schema/qudt/",
    "sdo": "https://schema.org/",
    "geo": "http://www.opengis.net/ont/geosparql#",
    "ssn-system": "http://www.w3.org/ns/ssn/system/",
    "prov": "http://www.w3.org/ns/prov#",
    "sta": "https://schemas.opengis.org/sta/def/core#",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream/context.jsonld)

## Sources

* [OGC SensorThings API Part 1: Sensing Version 1.1](https://docs.ogc.org/is/18-088/18-088.html#datastream)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/British-Oceanographic-Data-Centre/bblocks-sta](https://github.com/British-Oceanographic-Data-Centre/bblocks-sta)
* Path: `_sources/Datastream`

