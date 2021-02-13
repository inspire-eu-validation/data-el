# Elevation - Requirements on data quality and consistency - Isolated area test

**Purpose**: Verify whether an isolated area does not touch the external boundary of a void area.

(6) The boundary of an isolated area spatial object shall not touch the external boundary of a void area spatial object when they are referenced to the same vertical coordinate reference system.

**Prerequisites**

This is only applicable to datasets following the ElevationVectorElements application schema.

**Test method**

Inspect each instance of IsolatedArea spatial object type. The test is passed when non of them touches the external boundary of VoidArea object type that contains it when they are referenced to the same vertical reference system.

**Reference(s)**: 

* [TG DS-EL](./README.md#ref_TG_DS_EL) 10.2.1
* [IR-ISDSS](./README.md#ref_IR-ISDSS) Annex III, Section 1.7.6(6)

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
