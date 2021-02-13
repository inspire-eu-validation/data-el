# Elevation Grid Coverage - theme-specific requirement

**Purpose**: Verify that the following specic requirements are meet.

(1) By way of derogation from the requirement in Section 2.2 of Annex II ([IR-ISDSS](./README.md#ref_IR-ISDSS)), any grid compatible with one of the following coordinate reference systems may be used for making gridded Elevation data available:
	— two-dimensional geodetic coordinates (latitude and longitude) based on a datum specified in 1.2 of Annex II and using the parameters of the GRS80 ellipsoid;
	— plane coordinates using the ETRS89 Lambert Conformal Conic coordinate reference system;
	— plane coordinates using the ETRS89 Transverse Mercator coordinate reference system.
The grid specified in Section 2.2.1 of Annex II shall not be used."

(2) The domainExtent attribute of every ElevationGridCoverage instance shall be at least populated with a subtype of the EX_GeographicExtent type. (NOTE: This specific requirement is tested in an automatic way as constraint)

(3) The elevation property values included within the range set of a single ElevationGridCoverage shall be referenced to one and only one vertical coordinate reference system.

(4) All the ElevationGridCoverage instances, to which an aggregated ElevationGridCoverage instance refers, shall be consistent. This means that they shall share the same range type, Coordinate Reference System and resolution. They shall also support grid alignment, i.e. the grid points in one ElevationGridCoverage instance line up with grid points of the other ElevationGridCoverage instances, so that grid cells do not partially overlap.

(5) The contributing footprints of any two ElevationGridCoverage instances referred to by the same aggregated ElevationGridCoverage instance shall be either adjacent or disjoint.

(6) The union of the contributing footprints of the ElevationGridCoverage instances referred to by the same aggregated ElevationGridCoverage instance shall determine the geographic extent (domainExtent) of the aggregated ElevationGridCoverage instance.

(7) The ElevationGridCoverage package shall be restricted to two-dimensional geometries.

(8) Information about the acquisition dates of data contained in elevation grid coverages shall be provided at least in one of the following ways:
	(a) by providing the metadata element Temporal reference for each spatial object through the metadata attribute of the spatial object type ElevationGridCoverage;
	(b) by providing the metadata element Temporal reference required by Regulation (EC) No 1205/2008 as a temporal extent.


**Prerequisites**

**Test method**

Check manually that the specic requirements are meet.

**Reference(s)**: 

* [TG DS-EL](./README.md#ref_TG_DS_EL) 6.2.2.2.; 5.5.1.2.1.; 5.5.1.2.6.; 5.5.1.6.; 5.5.1.7.
* [IR-ISDSS](./README.md#ref_IR-ISDSS) Annex III, Section 1.7.2

**Test type**: Manual

**Notes** 


## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                   |  XPath expression                 |Multiplicity       |Voidable
------------------------------ | --------------------------------- | ------------------|----------
