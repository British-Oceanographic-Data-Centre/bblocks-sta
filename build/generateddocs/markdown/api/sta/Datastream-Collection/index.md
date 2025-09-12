
# STA Datastream as ObsCollection (Schema)

`ogc.api.sta.Datastream-Collection` *v0.1*

Metadata about a coherent set of observations - linked to a stream of observations. [OGC 10-004r3 / ISO 19156:2011]

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## What it represents

Forces the datastream to be an upper-level ObservationCollection setting common values, and the values stream to be regarded as a link to an ObservationCollection

### Limitations

TBD

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
  "@context": "https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream-Collection/context.jsonld",
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
    qudt:unit [ schema:name "Unitless" ] ;
    sosa:Observation <http://www.opengis.net/def/observationType/OGC-OM/2.0/OM_Measurement> ;
    sosa:hasMember <https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/Observations> ;
    sosa:madeByPlatform <https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/Thing> ;
    sosa:madeBySensor <https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/Sensor> ;
    sosa:observedProperty <https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Datastreams(2e92962c0b6996add9517e4242ea9bdcd2511e0ff7ac61981c6051a52b51f05c)/ObservedProperty> ;
    schema:name "2e92962c0b6996add9517e4242ea9bdc:d2511e0ff7ac61981c6051a52b51f05c" .


```

## Schema

```yaml
$schema: http://json-schema.org/draft-04/schema#
allOf:
- $ref: https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream/schema.yaml
x-jsonld-extra-terms:
  Observations@iot.navigationLink:
    x-jsonld-id: http://www.w3.org/ns/sosa/hasMember
    x-jsonld-type: '@id'
x-jsonld-prefixes:
  sosa: http://www.w3.org/ns/sosa/

```

Links to the schema:

* YAML version: [schema.yaml](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream-Collection/schema.json)
* JSON version: [schema.json](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream-Collection/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "@iot.id": "@id",
    "@iot.selfLink": "orel:iana/1.0/self",
    "Observations@iot.navigationLink": {
      "@id": "sosa:hasMember",
      "@type": "@id"
    },
    "name": "sdo:name",
    "description": "dct:description",
    "observationType": {
      "@id": "sosa:Observation",
      "@type": "@id"
    },
    "unitOfMeasurement": "qudt:unit",
    "symbol": "sdo:symbol",
    "unitDefinition": "@id",
    "observedArea": "geo:hasGeometry",
    "phenomenonTime": "sosa:phenomenonTime",
    "resultTime": "sosa:resultTime",
    "properties": "sdo:additionalProperty",
    "value": "sdo:value",
    "unitText": "sdo:unitText",
    "unitCode": "@id",
    "category": "sdo:CategoryCode",
    "termCode": "sdo:termCode",
    "inDefinedTermSet": "sdo:inDefinedTermSet",
    "hasSystemProperty": "ssn-system:hasSystemProperty",
    "status": "sdo:PropertyValue",
    "provider": "sdo:Organization",
    "type": "@type",
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
    "orel": "http://www.opengis.net/def/rel/",
    "sdo": "https://schema.org/",
    "dct": "http://purl.org/dc/terms/",
    "sosa": "http://www.w3.org/ns/sosa/",
    "qudt": "http://qudt.org/schema/qudt/",
    "geo": "http://www.opengis.net/ont/geosparql#",
    "ssn-system": "http://www.w3.org/ns/ssn/system/",
    "prov": "http://www.w3.org/ns/prov#",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream-Collection/context.jsonld)

## Sources

* [OGC SensorThings API Part 1: Sensing Version 1.1](https://docs.ogc.org/is/18-088/18-088.html#datastream)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/British-Oceanographic-Data-Centre/bblocks-sta](https://github.com/British-Oceanographic-Data-Centre/bblocks-sta)
* Path: `_sources/Datastream-Collection`

