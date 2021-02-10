# Constraints - DRAFT

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

The following check is performed for every feature in the dataset.

* The grid dimension shall always be 2 for an elevation grid coverage.
* The domainExtent shall be at least populated with a subtype of EX_GeographicExtent.
* The coordinate reference system used to reference the grid shall be provided.
* All the ElevationGridCoverage instances, to which an aggregated ElevationGridCoverage instance refers, shall share the same orientation of grid axes and the same grid spacing in each direction.
* The origin of the grid shall be described in two dimensions.
* The values in the range set shall be described by the Float type.


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-EL](./README.md#ref_TG_DS_EL) 

**Test type**: Manual

**Notes** 


## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression                     |Multiplicity       |Voidable
---------------------------------------------------------- | ------------------------------------- | ------------------|----------
