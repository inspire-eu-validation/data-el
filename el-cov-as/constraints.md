# Elevation Grid Coverage - Constraints

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

* The grid dimension shall always be 2 for an elevation grid coverage (domainDimensionIs2).
* The domainExtent shall be at least populated with a subtype of EX_GeographicExtent (domainExtentContainsGeographicElement).
* The coordinate reference system used to reference the grid shall be provided (domainRequiresCRS).
* All the ElevationGridCoverage instances, to which an aggregated ElevationGridCoverage instance refers, shall share the same orientation of grid axes and the same grid spacing in each direction (identicalOffsetVectorsWithinElevationCoverageAggregation).
* The origin of the grid shall be described in two dimensions (originDimensionIs2).
* The values in the range set shall be described by the Float type (rangeSetValuesAreOfTypeFloat).

**Prerequisites**

**Test method**

The following checks are performed for every feature in the dataset:

* Check that the grid [dimension](#dimension) is 2 for an elevation grid coverage (OCL: "inv:domainSet.dimension=2").

* Check that the [domainExtent](#domainExtent) is at least populated with a subtype of EX_GeographicExtent (OCL: "inv: domainExtent.geographicElement->size()>=1").

* Check that the [coordinate reference system](#originCRS) used to reference the grid is provided (OCL: "inv: domainSet.origin.coordinateReferenceSystem->notEmpty").

* Check that the [origin](#origin) of the grid is described in two dimensions (OCL: "inv: domainSet.origin.dimension=2").

The following checks shall be manually performed for every feature in the dataset:

* Check that all the ElevationGridCoverage instances, to which an aggregated ElevationGridCoverage instance refers, share the same orientation of grid axes and the same grid spacing in each direction (OCL: "Inv: contributingElevationCoverage->forAll(v | v.domainSet.offsetVectors = self.domainSet.offsetVectors)").

* Check taht the values in the range set are described by the Float type (OCL: "inv: rangeSet->forAll(v | v.oclIsKindOf(Float))").


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-EL](./README.md#ref_TG_DS_EL) 5.5.2.1.1.
* [IR-ISDSS](./README.md#ref_IR-ISDSS) Annex III, Section 1.4.1.1.

**Test type**: Automatic + Manual

**Notes** 


## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression                     |Multiplicity       |Voidable
---------------------------------------------------------- | ------------------------------------- | ------------------|----------
dimension <a name="dimension"></a> | //schema-element(el-cov:ElevationGridCoverage)/gml:domainSet/gml:RectifiedGrid/@dimension | 1 | Not applicable
domainExtent <a name="domainExtent"></a> | //schema-element(el-cov:ElevationGridCoverage)/el-cov:domainExtent/gmd:EX_Extent/gmd:geographicElement | 1..\* | No
origin CRS <a name="originCRS"></a> | //schema-element(el-cov:ElevationGridCoverage)/gml:domainSet/gml:RectifiedGrid/gml:origin/gml:Point/@srsName | 0..1 | Not applicable
origin dimension <a name="origin"></a> | //schema-element(el-cov:ElevationGridCoverage)/gml:domainSet/gml:RectifiedGrid/gml:origin/gml:Point/@srsDimension | 0..1 | Not applicable