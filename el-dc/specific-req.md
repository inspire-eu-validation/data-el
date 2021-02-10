# Elevation - Requirements on data quality and consistency - DRAFT

**Purpose**: 

(1) If measures other than ISO data quality measures have been used to evaluate an elevation data set, the Lineage metadata element shall include information about those measures and, if possible, a reference to an online resource where more information is available.
(2) Connected contour line spatial objects shall have the same elevation value when they are referenced to the same vertical coordinate reference system.
(3) When the elevation values of break line spatial objects are given as third coordinates (Z), the intersection point of two break line spatial objects shall have the same elevation value.
(4) When a contour line spatial object and a break line spatial object provided in the same vertical coordinate reference system intersect each other, the intersection point shall have the same elevation value (if the elevation values of break line spatial objects are given by the third (Z) coordinate).
(5) Contour line spatial objects having different elevation value shall neither intersect nor touch each other when they are referenced to the same vertical coordinate reference system.
(6) The boundary of an isolated area spatial object shall not touch the external boundary of a void area spatial object when they are referenced to the same vertical coordinate reference system.


**Prerequisites**

**Test method**


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) Section 6
* [TG DS-EL](./README.md#ref_TG_DS_EL) Section 6

**Test type**: Manual

**Notes** 


## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                   |  XPath expression                 |Multiplicity       |Voidable
------------------------------ | --------------------------------- | ------------------|----------
