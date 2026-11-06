# Sensor Things API Building Blocks

This is set of data [building blocks](https://ogcincubator.github.io/bblocks-docs/) describing reusable components of the Sensor Things API 1.1.  Building blocks provide elements that may be reused, and mappings to the underlying OMS model via the SOSA ontology. 


Initial work on the bblocks extraction was done for the particular cases of the Iliad project.
This initial draft can be missing some elements of the STA and relax on some formal constraints for the better support of the JSON Schema, OpenAPI 3.0.1 and JSON-LD specifications.
The mapping of schema elements to formal definitions (JSON-LD context files) shall be treated as draft proposition.


## Building Blocks

### `ogc.api.sta.Observation` — STA Observation

**Type:** schema

Representation of the result of act of measuring or otherwise determining the value of a property. [OGC 10-004r3 / ISO 19156:2011]

### `ogc.api.sta.Datastream` — STA Datastream

**Type:** schema

Metadata about a coherent set of observations, linked to value stream. [OGC 10-004r3 / ISO 19156:2011]

### `ogc.api.sta.FeatureOfInterest` — STA FeatureOfInterest (FOI)

**Type:** schema

Representation of the result of the FeatureOfInterest. 

### `ogc.api.sta.HistoricalLocations` — STA HistoricalLocation

**Type:** schema

A HistoricalLocation represents the association of a Thing with its Location(s) at a specific time. It provides the temporal context for where a Thing was located, enabling tracking of movement or changes in position.

### `ogc.api.sta.Locations` — STA Location

**Type:** schema

A Location represents the spatial position of a Thing. Locations are encoded using a geometry, typically expressed in GeoJSON, and may include descriptive metadata. Locations can be associated with one or more Things and tracked historically through HistoricalLocations.

### `ogc.api.sta.ObservedProperty` — STA ObservedProperty

**Type:** schema

An ObservedProperty specifies the phenomenon of an Observation. It defines what is being observed or measured, typically referenced using a URI from a controlled vocabulary or ontology.

### `ogc.api.sta.Sensor` — STA Sensor

**Type:** schema

A Sensor is an instrument that observes a property or phenomenon with the goal of producing an estimate of the value of the property.

### `ogc.api.sta.Thing` — STA Thing

**Type:** schema

A thing is an object of the physical world (physical things) or the information world (virtual things) that is capable of being identified and integrated into communication networks. [ITU-T Y.2060]

### `ogc.api.sta.Datastream.Datastream-Values-ObsCollection` — STA Datastream Values as ObservationCollection

**Type:** schema

Profile of STA where the values of a Datastream are modelled as a sub-collection

### `ogc.api.sta.Datastream-Collection` — STA Datastream as ObsCollection

**Type:** schema

Metadata about a coherent set of observations - linked to a stream of observations. [OGC 10-004r3 / ISO 19156:2011]

