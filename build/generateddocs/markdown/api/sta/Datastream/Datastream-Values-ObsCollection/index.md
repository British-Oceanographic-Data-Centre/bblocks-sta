
# STA Datastream Values as ObservationCollection (Schema)

`ogc.api.sta.Datastream.Datastream-Values-ObsCollection` *v0.1*

Profile of STA where the values of a Datastream are modelled as a sub-collection

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## What it represents

A Datastream (Collection Profile) groups a collection of Observations measuring the same ObservedProperty and produced by the same Sensor. [https://docs.ogc.org/is/18-088/18-088.html#datastream].

### Limitations

TBD

## References

Requirements: [http://www.opengis.net/spec/iot_sensing/1.1/req/datamodel#datastream](https://docs.ogc.org/is/18-088/18-088.html#datastream)

## Examples

### Observation whose Datastream has an ObservationType of OM_Measurement. A result’s data type is defined by the observationType.
#### json
```json
{
  "@iot.count": 3,
  "value": [
    {
      "result": {
        "type": "https://w3id.org/iliad/oim/ext/jellyfish/JellyFishAbundance",
        "label": "Result for jelly fish observation made by: 5432 on: 2024-03-30T11:35:00 location: 5 species: Rhopilema nomadica",
        "identifier": "9fff93dc8112faf563c83c0cbeade0e7",
        "aphiaID": "https://marinespecies.org/aphia.php?p=taxdetails&id=232032",
        "individualCount": "6-50",
        "sampleSizeValue": "11-30",
        "scientificName": "Rhopilema nomadica",
        "stingByJellyFish": "1",
        "strandedJellyfish": "Beach+Sea",
        "organismQuantity": "Some",
        "organismQuantityType": "individuals",
        "sampleSizeUnit": "cm",
        "scientificNameID": "https://marinespecies.org/aphia.php?p=taxdetails&id=232032"
      },
      "phenomenonTime": "2024-03-30T11:35:00",
      "resultTime": "2024-03-30T11:35:00",
      "@iot.id": "5c9828ee2b0cb39ae13fc06dd238960f",
      "@iot.selfLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('5c9828ee2b0cb39ae13fc06dd238960f')",
      "Datastream@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('5c9828ee2b0cb39ae13fc06dd238960f')/Datastream",
      "FeatureOfInterest@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('5c9828ee2b0cb39ae13fc06dd238960f')/FeatureOfInterest"
    },
    {
      "result": {
        "type": "https://w3id.org/iliad/oim/ext/jellyfish/JellyFishAbundance",
        "label": "Result for jelly fish observation made by: 5432 on: 2024-03-30T11:17:00 location: 1 species: Rhopilema nomadica",
        "identifier": "cdc6d5dfd68abd526a43df7ccd099b70",
        "aphiaID": "https://marinespecies.org/aphia.php?p=taxdetails&id=232032",
        "individualCount": "1-5",
        "sampleSizeValue": "11-30",
        "scientificName": "Rhopilema nomadica",
        "stingByJellyFish": "0",
        "strandedJellyfish": "0",
        "organismQuantity": "Few",
        "organismQuantityType": "individuals",
        "sampleSizeUnit": "cm",
        "scientificNameID": "https://marinespecies.org/aphia.php?p=taxdetails&id=232032"
      },
      "phenomenonTime": "2024-03-30T11:17:00",
      "resultTime": "2024-03-30T11:17:00",
      "@iot.id": "ec36b55fb78177474b2f5ec2227c0818",
      "@iot.selfLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('ec36b55fb78177474b2f5ec2227c0818')",
      "Datastream@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('ec36b55fb78177474b2f5ec2227c0818')/Datastream",
      "FeatureOfInterest@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('ec36b55fb78177474b2f5ec2227c0818')/FeatureOfInterest"
    },
    {
      "result": {
        "type": "https://w3id.org/iliad/oim/ext/jellyfish/JellyFishAbundance",
        "label": "Result for jelly fish observation made by: 5432 on: 2024-03-30T11:17:00 location: 1 species: Other",
        "identifier": "4f09272faa610d8ad453ee42cd8deaef",
        "aphiaID": "Other",
        "individualCount": "1-5",
        "sampleSizeValue": "11-30",
        "scientificName": "Other",
        "stingByJellyFish": "0",
        "strandedJellyfish": "0",
        "organismQuantity": "Few",
        "organismQuantityType": "individuals",
        "sampleSizeUnit": "cm",
        "scientificNameID": "Other"
      },
      "phenomenonTime": "2024-03-30T11:17:00",
      "resultTime": "2024-03-30T11:17:00",
      "@iot.id": "af6992915f7037c10949a4aab2119109",
      "@iot.selfLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('af6992915f7037c10949a4aab2119109')",
      "Datastream@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('af6992915f7037c10949a4aab2119109')/Datastream",
      "FeatureOfInterest@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('af6992915f7037c10949a4aab2119109')/FeatureOfInterest"
    }
  ]
}
```

#### jsonld
```jsonld
{
  "@context": "https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream/Datastream-Values-ObsCollection/context.jsonld",
  "@iot.count": 3,
  "value": [
    {
      "result": {
        "type": "https://w3id.org/iliad/oim/ext/jellyfish/JellyFishAbundance",
        "label": "Result for jelly fish observation made by: 5432 on: 2024-03-30T11:35:00 location: 5 species: Rhopilema nomadica",
        "identifier": "9fff93dc8112faf563c83c0cbeade0e7",
        "aphiaID": "https://marinespecies.org/aphia.php?p=taxdetails&id=232032",
        "individualCount": "6-50",
        "sampleSizeValue": "11-30",
        "scientificName": "Rhopilema nomadica",
        "stingByJellyFish": "1",
        "strandedJellyfish": "Beach+Sea",
        "organismQuantity": "Some",
        "organismQuantityType": "individuals",
        "sampleSizeUnit": "cm",
        "scientificNameID": "https://marinespecies.org/aphia.php?p=taxdetails&id=232032"
      },
      "phenomenonTime": "2024-03-30T11:35:00",
      "resultTime": "2024-03-30T11:35:00",
      "@iot.id": "5c9828ee2b0cb39ae13fc06dd238960f",
      "@iot.selfLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('5c9828ee2b0cb39ae13fc06dd238960f')",
      "Datastream@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('5c9828ee2b0cb39ae13fc06dd238960f')/Datastream",
      "FeatureOfInterest@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('5c9828ee2b0cb39ae13fc06dd238960f')/FeatureOfInterest"
    },
    {
      "result": {
        "type": "https://w3id.org/iliad/oim/ext/jellyfish/JellyFishAbundance",
        "label": "Result for jelly fish observation made by: 5432 on: 2024-03-30T11:17:00 location: 1 species: Rhopilema nomadica",
        "identifier": "cdc6d5dfd68abd526a43df7ccd099b70",
        "aphiaID": "https://marinespecies.org/aphia.php?p=taxdetails&id=232032",
        "individualCount": "1-5",
        "sampleSizeValue": "11-30",
        "scientificName": "Rhopilema nomadica",
        "stingByJellyFish": "0",
        "strandedJellyfish": "0",
        "organismQuantity": "Few",
        "organismQuantityType": "individuals",
        "sampleSizeUnit": "cm",
        "scientificNameID": "https://marinespecies.org/aphia.php?p=taxdetails&id=232032"
      },
      "phenomenonTime": "2024-03-30T11:17:00",
      "resultTime": "2024-03-30T11:17:00",
      "@iot.id": "ec36b55fb78177474b2f5ec2227c0818",
      "@iot.selfLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('ec36b55fb78177474b2f5ec2227c0818')",
      "Datastream@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('ec36b55fb78177474b2f5ec2227c0818')/Datastream",
      "FeatureOfInterest@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('ec36b55fb78177474b2f5ec2227c0818')/FeatureOfInterest"
    },
    {
      "result": {
        "type": "https://w3id.org/iliad/oim/ext/jellyfish/JellyFishAbundance",
        "label": "Result for jelly fish observation made by: 5432 on: 2024-03-30T11:17:00 location: 1 species: Other",
        "identifier": "4f09272faa610d8ad453ee42cd8deaef",
        "aphiaID": "Other",
        "individualCount": "1-5",
        "sampleSizeValue": "11-30",
        "scientificName": "Other",
        "stingByJellyFish": "0",
        "strandedJellyfish": "0",
        "organismQuantity": "Few",
        "organismQuantityType": "individuals",
        "sampleSizeUnit": "cm",
        "scientificNameID": "Other"
      },
      "phenomenonTime": "2024-03-30T11:17:00",
      "resultTime": "2024-03-30T11:17:00",
      "@iot.id": "af6992915f7037c10949a4aab2119109",
      "@iot.selfLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('af6992915f7037c10949a4aab2119109')",
      "Datastream@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('af6992915f7037c10949a4aab2119109')/Datastream",
      "FeatureOfInterest@iot.navigationLink": "https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('af6992915f7037c10949a4aab2119109')/FeatureOfInterest"
    }
  ]
}
```

#### ttl
```ttl
@prefix sosa: <http://www.w3.org/ns/sosa/> .

<http://w3id.org/ogcincubator/bblocks-sta/5c9828ee2b0cb39ae13fc06dd238960f> sosa:hasFeatureOfInterest <https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('5c9828ee2b0cb39ae13fc06dd238960f')/FeatureOfInterest> ;
    sosa:hasSimpleResult [ ] ;
    sosa:phenomenonTime "2024-03-30T11:35:00" ;
    sosa:resultTime "2024-03-30T11:35:00" ;
    sosa:usedProcedure <https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('5c9828ee2b0cb39ae13fc06dd238960f')/Datastream> .

<http://w3id.org/ogcincubator/bblocks-sta/af6992915f7037c10949a4aab2119109> sosa:hasFeatureOfInterest <https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('af6992915f7037c10949a4aab2119109')/FeatureOfInterest> ;
    sosa:hasSimpleResult [ ] ;
    sosa:phenomenonTime "2024-03-30T11:17:00" ;
    sosa:resultTime "2024-03-30T11:17:00" ;
    sosa:usedProcedure <https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('af6992915f7037c10949a4aab2119109')/Datastream> .

<http://w3id.org/ogcincubator/bblocks-sta/ec36b55fb78177474b2f5ec2227c0818> sosa:hasFeatureOfInterest <https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('ec36b55fb78177474b2f5ec2227c0818')/FeatureOfInterest> ;
    sosa:hasSimpleResult [ ] ;
    sosa:phenomenonTime "2024-03-30T11:17:00" ;
    sosa:resultTime "2024-03-30T11:17:00" ;
    sosa:usedProcedure <https://sensor-things-api-sensor-things-api.apps.dcw1.paas.psnc.pl/jf2024/api/v1.0/Observations('ec36b55fb78177474b2f5ec2227c0818')/Datastream> .


```

## Schema

```yaml
$schema: http://json-schema.org/draft-04/schema#
properties:
  '@iot.count':
    type: number
    x-jsonld-id: https://www.w3.org/TR/vocab-ssn/#collectionCount
  value:
    type: array
    items:
      allOf:
      - $ref: https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Observation/schema.yaml
    x-jsonld-id: '@graph'
x-jsonld-extra-terms:
  Observations@iot.navigationLink:
    x-jsonld-id: https://www.w3.org/TR/vocab-ssn/#hasMember
    x-jsonld-type: '@id'
x-jsonld-prefixes:
  sosa: https://www.w3.org/TR/vocab-ssn/#

```

Links to the schema:

* YAML version: [schema.yaml](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream/Datastream-Values-ObsCollection/schema.json)
* JSON version: [schema.json](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream/Datastream-Values-ObsCollection/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "@iot.count": "sosa:collectionCount",
    "@iot.id": "@id",
    "@iot.selfLink": "orel:iana/1.0/self",
    "phenomenonTime": "http://www.w3.org/ns/sosa/phenomenonTime",
    "result": "http://www.w3.org/ns/sosa/hasSimpleResult",
    "resultQuality": {
      "@context": {
        "dqv:value": "dqv:value"
      },
      "@id": "dqv:hasQualityMeasurement"
    },
    "resultTime": "http://www.w3.org/ns/sosa/resultTime",
    "Datastream@iot.navigationLink": {
      "@id": "http://www.w3.org/ns/sosa/usedProcedure",
      "@type": "@id"
    },
    "FeatureOfInterest@iot.navigationLink": {
      "@id": "http://www.w3.org/ns/sosa/hasFeatureOfInterest",
      "@type": "@id"
    },
    "value": "@graph",
    "Observations@iot.navigationLink": {
      "@id": "sosa:hasMember",
      "@type": "@id"
    },
    "sosa": "https://www.w3.org/TR/vocab-ssn/#",
    "orel": "http://www.opengis.net/def/rel/",
    "dqv": "http://www.w3.org/ns/dqv#",
    "sdo": "https://schema.org/",
    "dct": "http://purl.org/dc/terms/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://british-oceanographic-data-centre.github.io/bblocks-sta/build/annotated/api/sta/Datastream/Datastream-Values-ObsCollection/context.jsonld)

## Sources

* [OGC SensorThings API Part 1: Sensing Version 1.1](https://docs.ogc.org/is/18-088/18-088.html#datastream)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/British-Oceanographic-Data-Centre/bblocks-sta](https://github.com/British-Oceanographic-Data-Centre/bblocks-sta)
* Path: `_sources/Datastream/Datastream-Values-ObsCollection`

