
# STA Datastream Properties Context (Schema)

`ogc.api.sta.Datastream.Properties` *v0.1*

JSON-LD context applied to each SensorThings API Datastream occurrence.

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## SensorThings API Datastream custom properties context

This building block defines the JSON-LD mapping for the custom `properties`
member attached to each SensorThings API Datastream occurrence.

The parent Datastream context supplies the entity-level mappings for its name,
description, observation metadata, self link, and navigation links.

## Examples

### SensorThings API Datastream custom properties
#### json
```json
{
  "properties": {
    "name": "Example datastream property",
    "description": "Metadata attached to an individual datastream.",
    "identifier": "example-datastream-property-1",
    "category": "quality",
    "value": "example",
    "unitCode": "http://qudt.org/vocab/unit/UNITLESS"
  }
}

```

#### jsonld
```jsonld
{
  "@context": "https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream/Properties/context.jsonld",
  "properties": {
    "name": "Example datastream property",
    "description": "Metadata attached to an individual datastream.",
    "identifier": "example-datastream-property-1",
    "category": "quality",
    "value": "example",
    "unitCode": "http://qudt.org/vocab/unit/UNITLESS"
  }
}
```

#### ttl
```ttl
@prefix schema: <https://schema.org/> .

<http://qudt.org/vocab/unit/UNITLESS> schema:category "quality" ;
    schema:description "Metadata attached to an individual datastream." ;
    schema:identifier "example-datastream-property-1" ;
    schema:name "Example datastream property" ;
    schema:value "example" .

[] schema:additionalProperty <http://qudt.org/vocab/unit/UNITLESS> .


```

## Schema

```yaml
$schema: http://json-schema.org/draft-04/schema#
title: SensorThings API Datastream custom properties
description: Custom properties attached to a SensorThings API Datastream occurrence.
type: object
additionalProperties: true
properties:
  properties:
    type: object
    additionalProperties: true
    x-jsonld-id: https://schema.org/additionalProperty
    x-jsonld-extra-terms:
      hasSystemProperty: http://www.w3.org/ns/ssn/system/hasSystemProperty
      status: https://schema.org/status
      name: https://schema.org/name
      license: https://schema.org/license
      description: https://schema.org/description
      url: https://schema.org/url
      usageInfo: https://schema.org/usageInfo
      identifier: https://schema.org/identifier
      propertyID: https://schema.org/propertyID
      category: https://schema.org/category
      termCode: https://schema.org/termCode
      inDefinedTermSet: https://schema.org/inDefinedTermSet
      provider: https://schema.org/provider
      value: https://schema.org/value
      unitCode: '@id'
      unitText: https://schema.org/unitText
x-jsonld-prefixes:
  sdo: https://schema.org/
  ssn-system: http://www.w3.org/ns/ssn/system/
x-bblocks-metadata:
  itemIdentifier: ogc.api.sta.Datastream.Properties
  register: https://british-oceanographic-data-centre.github.io/bblocks-sta/build/register.json
  version: '0.1'
  dateOfLastChange: '2026-11-09'

```

Links to the schema:

* YAML version: [schema.yaml](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream/Properties/schema.json)
* JSON version: [schema.json](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream/Properties/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "properties": {
      "@context": {
        "hasSystemProperty": "ssn-system:hasSystemProperty",
        "status": "sdo:status",
        "name": "sdo:name",
        "license": "sdo:license",
        "description": "sdo:description",
        "url": "sdo:url",
        "usageInfo": "sdo:usageInfo",
        "identifier": "sdo:identifier",
        "propertyID": "sdo:propertyID",
        "category": "sdo:category",
        "termCode": "sdo:termCode",
        "inDefinedTermSet": "sdo:inDefinedTermSet",
        "provider": "sdo:provider",
        "value": "sdo:value",
        "unitCode": "@id",
        "unitText": "sdo:unitText"
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
[context.jsonld](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream/Properties/context.jsonld)

## Sources

* [OGC SensorThings API Part 1: Sensing Version 1.1](https://docs.ogc.org/is/18-088/18-088.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/British-Oceanographic-Data-Centre/bblocks-sta](https://github.com/British-Oceanographic-Data-Centre/bblocks-sta)
* Path: `_sources/Datastream/Properties`

