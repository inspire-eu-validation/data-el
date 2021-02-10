# Elevation TIN theme-specific requirement - DRAFT

**Purpose**: Verify that

* (1) The property values included within a single instance of ElevationTIN spatial object type (TIN model) shall be referenced to one and only one vertical coordinate reference system.

* (2) Triangles intersecting a stop line shall be removed from a TIN surface, leaving holes in the surface. If coincidence occurs on surface boundary triangles, the result shall be a change of the surface boundary.

* (3) The vector spatial objects provided as components of a TIN collection shall fulfil the generic consistency rules provided for vector objects.


**Prerequisites**

**Test method**



**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 12 (1)
* [TG DS-EL](./README.md#ref_TG_DS_EL) 5.4.1.2.1.

**Test type**: Manual

**Notes** 


## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                   |  XPath expression                 |Multiplicity       |Voidable
------------------------------ | --------------------------------- | ------------------|----------
