## HistoricalLocation

A HistoricalLocation represents the association of a Thing with a Location (or set of Locations) at a specific time. It allows the movement of Things, or changes in their position, to be tracked through time. Each HistoricalLocation links a Thing to one or more Locations and records the temporal information for that association.

STA HistoricalLocation is based on the concept from [OGC and ISO 19156:2001, OGC 10-004r3 and ISO 19156:2011(E), OGC Abstract Specification: Geographic information — Observations and Measurements.](http://portal.opengeospatial.org/files/?artifact_id=41579)

### Limitations
For compliance with SwaggerHub where the schema can be referred:
- type of id is not specified, while it shall be string or number
- type of metadata property is not specified, while it shall be string or object

## References

Requirements: [http://www.opengis.net/spec/iot_sensing/1.1/req/datamodel/historicallocation](https://docs.ogc.org/is/18-088/18-088.html#historicallocation)
