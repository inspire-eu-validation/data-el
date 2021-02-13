# Elevation - Requirements on data quality and consistency - Contour line test

**Purpose**: Verify whether contour lines follow the consistency rules specified in Commission Regulation 1089/2010 ([IR-ISDSS](./README.md#ref_IR-ISDSS)). 

(2) Connected contour line spatial objects shall have the same elevation value when they are referenced to the same vertical coordinate reference system.

(5) Contour line spatial objects having different elevation value shall neither intersect nor touch each other when they are referenced to the same vertical coordinate reference system.

**Prerequisites**

This is only applicable to datasets following the ElevationVectorElements application schema.

**Test method**

Inspect elevationPropertyTypeValue referenced to the same vertical coordinate reference system for each pair of contour lines. The test is passed when
	* each connected contour lines have the same elevation value and
	* contour lines having different elevation values neither intersect nor touch each other.

**Reference(s)**: 

* [TG DS-EL](./README.md#ref_TG_DS_EL) 10.2.1
* [IR-ISDSS](./README.md#ref_IR-ISDSS) Annex III, Section 1.7.6(2) and 1.7.6(5)

**Test type**: Manual

**Notes** 

1 This test can be performed entirely on the basis of the information available in the database of the data providers.
2 This is only applicable to datasets following the ElevationVectorElements application schema.

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                   |  XPath expression                 |Multiplicity       |Voidable
------------------------------ | --------------------------------- | ------------------|----------
