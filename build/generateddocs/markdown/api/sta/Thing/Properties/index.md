
# STA Thing Properties Context (Schema)

`ogc.api.sta.Thing.Properties` *v0.1*

JSON-LD context applied to each SensorThings API Thing occurrence.

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## SensorThings API Thing custom properties context

This building block defines the JSON-LD mapping for the custom `properties`
member attached to each SensorThings API Thing occurrence.

The parent Thing context supplies the entity-level mappings for its name,
description, self link, and navigation links.

## Examples

### SensorThings API Thing custom properties
#### json
```json
{
  "properties": {
    "category": "platform",
    "identifier": "example-platform-1",
    "provider": "Example provider",
    "name": "Example platform",
    "termCode": "platform",
    "inDefinedTermSet": "https://example.org/vocabulary",
    "value": "example",
    "propertyID": "platform-type"
  }
}

```

#### jsonld
```jsonld
{
  "@context": "https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/Properties/context.jsonld",
  "properties": {
    "category": "platform",
    "identifier": "example-platform-1",
    "provider": "Example provider",
    "name": "Example platform",
    "termCode": "platform",
    "inDefinedTermSet": "https://example.org/vocabulary",
    "value": "example",
    "propertyID": "platform-type"
  }
}
```

#### ttl
```ttl
@prefix schema: <https://schema.org/> .

[] schema:additionalProperty [ schema:category "platform" ;
            schema:identifier "example-platform-1" ;
            schema:inDefinedTermSet "https://example.org/vocabulary" ;
            schema:name "Example platform" ;
            schema:propertyID "platform-type" ;
            schema:provider "Example provider" ;
            schema:termCode "platform" ;
            schema:value "example" ] .


```

## Schema

```yaml
$schema: http://json-schema.org/draft-04/schema#
title: SensorThings API Thing custom properties
description: Custom properties attached to a SensorThings API Thing occurrence.
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
  itemIdentifier: ogc.api.sta.Thing.Properties
  register: https://british-oceanographic-data-centre.github.io/bblocks-sta/build/register.json
  version: '0.1'
  dateOfLastChange: '2026-11-06'

```

Links to the schema:

* YAML version: [schema.yaml](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/Properties/schema.json)
* JSON version: [schema.json](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/Properties/schema.yaml)


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
[context.jsonld](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Thing/Properties/context.jsonld)

## Sources

* [OGC SensorThings API Part 1: Sensing Version 1.1](https://docs.ogc.org/is/18-088/18-088.html)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/British-Oceanographic-Data-Centre/bblocks-sta](https://github.com/British-Oceanographic-Data-Centre/bblocks-sta)
* Path: `_sources/Thing/Properties`

