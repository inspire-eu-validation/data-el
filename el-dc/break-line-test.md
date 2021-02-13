# Elevation - Requirements on data quality and consistency - Break line test

**Purpose**: Verify whether break lines follow the consistency rules specified in Commission Regulation 1089/2010 ([IR-ISDSS](./README.md#ref_IR-ISDSS)).

(3) When the elevation values of break line spatial objects are given as third coordinates (Z), the intersection point of two break line spatial objects shall have the same elevation value.

(4) When a contour line spatial object and a break line spatial object provided in the same vertical coordinate reference system intersect each other, the intersection point shall have the same elevation value (if the elevation values of break line spatial objects are given by the third (Z) coordinate).

**Prerequisites**

This is only applicable to datasets following the ElevationVectorElements application schema.

**Test method**

For each brake line that has an intersection point expressed as third coordinate (Z) in the same vertical coordinate reference system inspect the elevation value at the intersection point. The test is passed when the elevationPropertyTypeValue at this point is equal
	* for any pair of intersecting break lines and/or
	* for any intersecting brake line and contour line.

**Reference(s)**: 

* [TG DS-EL](./README.md#ref_TG_DS_EL) 10.2.1
* [IR-ISDSS](./README.md#ref_IR-ISDSS) Annex III, Section 1.7.6(3) and 1.7.6(4)

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
