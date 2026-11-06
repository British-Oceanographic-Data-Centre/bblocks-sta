
# STA Thing Top-Level Context (Schema)

`ogc.api.sta.Thing.TopLevelContext` *v0.1*

Top-level JSON-LD context shared by SensorThings API Thing representations.

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## SensorThings API Thing top-level context

This building block defines the shared JSON-LD mapping for the `properties`
member of SensorThings API Thing representations.

Entity-specific contexts, such as the Thing context, can be applied within the
top-level context without duplicating these shared property mappings.

## Examples

### Shared SensorThings API properties
#### json
```json
{
  "properties": {
    "category": "platform",
    "identifier": "example-platform-1",
    "name": "Example platform",
    "value": "example"
  }
}

```

#### jsonld
```jsonld
{
  "@context": "https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/TopLevelContext/context.jsonld",
  "properties": {
    "category": "platform",
    "identifier": "example-platform-1",
    "name": "Example platform",
    "value": "example"
  }
}
```

#### ttl
```ttl
@prefix schema: <https://schema.org/> .

[] schema:additionalProperty [ schema:category "platform" ;
            schema:identifier "example-platform-1" ;
            schema:name "Example platform" ;
            schema:value "example" ] .


```

## Schema

```yaml
$schema: http://json-schema.org/draft-04/schema#
title: SensorThings API Thing top-level context
description: Shared top-level properties used by SensorThings API Thing representations.
type: object
additionalProperties: true
properties:
  properties:
    type: object
    additionalProperties: true
    x-jsonld-id: https://schema.org/additionalProperty
    x-jsonld-extra-terms:
      category: https://schema.org/category
      identifier: https://schema.org/identifier
      provider: https://schema.org/provider
      name: https://schema.org/name
      termCode: https://schema.org/termCode
      inDefinedTermSet: https://schema.org/inDefinedTermSet
      value: https://schema.org/value
      propertyID: https://schema.org/propertyID
x-jsonld-prefixes:
  sdo: https://schema.org/
x-bblocks-metadata:
  itemIdentifier: ogc.api.sta.Thing.TopLevelContext
  register: https://british-oceanographic-data-centre.github.io/bblocks-sta/build/register.json
  version: '0.1'
  dateOfLastChange: '2026-11-06'

```

Links to the schema:

* YAML version: [schema.yaml](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/TopLevelContext/schema.json)
* JSON version: [schema.json](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/TopLevelContext/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "properties": {
      "@context": {
        "category": "sdo:category",
        "identifier": "sdo:identifier",
        "provider": "sdo:provider",
        "name": "sdo:name",
        "termCode": "sdo:termCode",
        "inDefinedTermSet": "sdo:inDefinedTermSet",
        "value": "sdo:value",
        "propertyID": "sdo:propertyID"
      },
      "@id": "sdo:additionalProperty"
    },
    "sdo": "https://schema.org/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/TopLevelContext/context.jsonld)

## Sources

* [OGC SensorThings API Part 1: Sensing Version 1.1](https://docs.ogc.org/is/18-088/18-088.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/British-Oceanographic-Data-Centre/bblocks-sta](https://github.com/British-Oceanographic-Data-Centre/bblocks-sta)
* Path: `_sources/Thing/TopLevelContext`

