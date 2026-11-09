
# STA Sensor Properties Context (Schema)

`ogc.api.sta.Sensor.Properties` *v0.1*

JSON-LD context applied to each SensorThings API Sensor occurrence.

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## SensorThings API Sensor custom properties context

This building block defines the JSON-LD mapping for the custom `properties`
member attached to each SensorThings API Sensor occurrence.

The parent Sensor context supplies the entity-level mappings for its name,
description, encoding type, metadata, self link, and Datastream navigation link.

## Examples

### SensorThings API Sensor custom properties
#### json
```json
{
  "properties": {
    "category": "temperature sensor",
    "identifier": "TMP36-1",
    "manufacturer": "Example manufacturer",
    "model": "TMP36",
    "serialNumber": "SN-0001",
    "name": "Example temperature sensor",
    "value": "active",
    "unitCode": "http://qudt.org/vocab/unit/DEG_C"
  }
}

```

#### jsonld
```jsonld
{
  "@context": "https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Sensor/Properties/context.jsonld",
  "properties": {
    "category": "temperature sensor",
    "identifier": "TMP36-1",
    "manufacturer": "Example manufacturer",
    "model": "TMP36",
    "serialNumber": "SN-0001",
    "name": "Example temperature sensor",
    "value": "active",
    "unitCode": "http://qudt.org/vocab/unit/DEG_C"
  }
}
```

#### ttl
```ttl
@prefix schema: <https://schema.org/> .

<http://qudt.org/vocab/unit/DEG_C> schema:category "temperature sensor" ;
    schema:identifier "TMP36-1" ;
    schema:manufacturer "Example manufacturer" ;
    schema:model "TMP36" ;
    schema:name "Example temperature sensor" ;
    schema:serialNumber "SN-0001" ;
    schema:value "active" .

[] schema:additionalProperty <http://qudt.org/vocab/unit/DEG_C> .


```

## Schema

```yaml
$schema: http://json-schema.org/draft-04/schema#
title: SensorThings API Sensor custom properties
description: Custom properties attached to a SensorThings API Sensor occurrence.
type: object
additionalProperties: true
properties:
  properties:
    type: object
    additionalProperties: true
    x-jsonld-id: https://schema.org/additionalProperty
    x-jsonld-extra-terms:
      category: https://schema.org/category
      hasSystemProperty: http://www.w3.org/ns/ssn/system/hasSystemProperty
      identifier: https://schema.org/identifier
      manufacturer: https://schema.org/manufacturer
      model: https://schema.org/model
      serialNumber: https://schema.org/serialNumber
      valueReference: https://schema.org/valueReference
      name: https://schema.org/name
      termCode: https://schema.org/termCode
      inDefinedTermSet: https://schema.org/inDefinedTermSet
      propertyID: https://schema.org/propertyID
      value: https://schema.org/value
      unitCode: '@id'
      unitText: https://schema.org/unitText
      maxValue: https://schema.org/maxValue
      minValue: https://schema.org/minValue
x-jsonld-prefixes:
  sdo: https://schema.org/
  ssn-system: http://www.w3.org/ns/ssn/system/
x-bblocks-metadata:
  itemIdentifier: ogc.api.sta.Sensor.Properties
  register: https://british-oceanographic-data-centre.github.io/bblocks-sta/build/register.json
  version: '0.1'
  dateOfLastChange: '2026-11-09'

```

Links to the schema:

* YAML version: [schema.yaml](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Sensor/Properties/schema.json)
* JSON version: [schema.json](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Sensor/Properties/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "properties": {
      "@context": {
        "category": "sdo:category",
        "hasSystemProperty": "ssn-system:hasSystemProperty",
        "identifier": "sdo:identifier",
        "manufacturer": "sdo:manufacturer",
        "model": "sdo:model",
        "serialNumber": "sdo:serialNumber",
        "valueReference": "sdo:valueReference",
        "name": "sdo:name",
        "termCode": "sdo:termCode",
        "inDefinedTermSet": "sdo:inDefinedTermSet",
        "propertyID": "sdo:propertyID",
        "value": "sdo:value",
        "unitCode": "@id",
        "unitText": "sdo:unitText",
        "maxValue": "sdo:maxValue",
        "minValue": "sdo:minValue"
      },
      "@id": "sdo:additionalProperty"
    },
    "sdo": "https://schema.org/",
    "ssn-system": "http://www.w3.org/ns/ssn/system/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Sensor/Properties/context.jsonld)

## Sources

* [OGC SensorThings API Part 1: Sensing Version 1.1](https://docs.ogc.org/is/18-088/18-088.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/British-Oceanographic-Data-Centre/bblocks-sta](https://github.com/British-Oceanographic-Data-Centre/bblocks-sta)
* Path: `_sources/Sensor/Properties`

