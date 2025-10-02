## Location

A Location represents the spatial position of a Thing. It describes where a Thing is situated, using a geometry (commonly encoded in GeoJSON) and may also include descriptive metadata and user-defined properties. A Thing may have multiple Locations, and the association between a Thing and its Locations can change over time, tracked via HistoricalLocations.

STA location is based on the concept from [OGC and ISO 19156:2001, OGC 10-004r3 and ISO 19156:2011(E), OGC Abstract Specification: Geographic information — Observations and Measurements.](http://portal.opengeospatial.org/files/?artifact_id=41579)

### Limitations
For compliance with SwaggerHub where the schema can be referred:
- type of id is not specified, while it shall be string or number
- type of metadata property is not specified, while it shall be string or object

##### Till here


## References

Requirements: [http://www.opengis.net/spec/iot_sensing/1.1/req/datamodel/Location](https://docs.ogc.org/is/18-088/18-088.html#location)
