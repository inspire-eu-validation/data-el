# Elevation theme-specific requirement - DRAFT

**Purpose**: Verify that:

* By way of derogation from the requirement in Section 2.2 of Annex II, any grid compatible with one of the following coordinate reference systems may be used for making gridded Elevation data available:
	— two-dimensional geodetic coordinates (latitude and longitude) based on a datum specified in 1.2 of Annex II and using the parameters of the GRS80 ellipsoid;
	— plane coordinates using the ETRS89 Lambert Conformal Conic coordinate reference system;
	— plane coordinates using the ETRS89 Transverse Mercator coordinate reference system.
	The grid specified in Section 2.2.1 of Annex II shall not be used."

* The domainExtent attribute of every ElevationGridCoverage instance shall be at least populated with a subtype of the EX_GeographicExtent type.

* The elevation property values included within the range set of a single ElevationGridCoverage shall be referenced to one and only one vertical coordinate reference system.

* All the ElevationGridCoverage instances, to which an aggregated ElevationGridCoverage instance refers, shall be consistent. This means that they shall share the same range type, Coordinate Reference System and resolution. They shall also support grid alignment, i.e. the grid points in one ElevationGridCoverage instance line up with grid points of the other ElevationGridCoverage instances, so that grid cells do not partially overlap.

* The contributing footprints of any two ElevationGridCoverage instances referred to by the same aggregated ElevationGridCoverage instance shall be either adjacent or disjoint.

* The union of the contributing footprints of the ElevationGridCoverage instances referred to by the same aggregated ElevationGridCoverage instance shall determine the geographic extent (domainExtent) of the aggregated ElevationGridCoverage instance.

* The ElevationGridCoverage package shall be restricted to two-dimensional geometries.

* Information about the acquisition dates of data contained in elevation grid coverages shall be provided at least in one of the following ways:
	(a) by providing the metadata element Temporal reference for each spatial object through the metadata attribute of the spatial object type ElevationGridCoverage;
	(b) by providing the metadata element Temporal reference required by Regulation (EC) No 1205/2008 as a temporal extent.


**Prerequisites**

**Test method**


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 12 (1)
* [TG DS-EL](./README.md#ref_TG_DS_EL) 

**Test type**: Manual

**Notes** 


## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                   |  XPath expression                 |Multiplicity       |Voidable
------------------------------ | --------------------------------- | ------------------|----------
