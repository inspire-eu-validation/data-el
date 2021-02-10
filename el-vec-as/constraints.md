# Constraints - DRAFT

**Purpose**: Verify that:

* Constraints of the spatial object type SpotElevation:
	* The dimension of the property value coordinate shall be 1
	* The property value shall be expressed referring to a vertical coordinate reference system
	
* Constraints of the spatial object type ContourLine:
	* The dimension of the property value coordinate shall be 1.
	* The property value shall be expressed referring to a vertical coordinate reference system.

**Prerequisites**

**Test method**

The following checks are performed for every feature in the dataset.


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-EL](./README.md#ref_TG_DS_EL) 5.5.2.1.2., 5.5.2.2.1.

**Test type**: Automated

**Notes** 

Verify that the OCL constraints that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation).

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression                     |Multiplicity       |Voidable
---------------------------------------------------------- | ------------------------------------- | ------------------|----------
LandCoverUnit geometry <a name="geometries"></a> | //schema-element(el-tin:LandCoverUnit)/el-tin:geometry/gml:Surface <br> //schema-element(el-tin:LandCoverUnit)/el-tin:geometry/gml:Point <br> //schema-element(el-tin:LandCoverDataset)/el-tin:member/el-tin:LandCoverUnit/el-tin:geometry/gml:Surface <br> //schema-element(el-tin:LandCoverDataset)/el-tin:member/el-tin:LandCoverUnit/el-tin:geometry/gml:Point | 1 | No
coveredPercentage <a name="coveredPercentage"></a> | //schema-element(el-tin:LandCoverUnit)/el-tin:landCoverObservation/el-tin:LandCoverObservation/el-tin:mosaic/el-tin:LandCoverValue/el-tin:coveredPercentage <br> //schema-element(el-tin:LandCoverDataset)/el-tin:member/el-tin:LandCoverUnit/el-tin:landCoverObservation/el-tin:LandCoverObservation/el-tin:mosaic/el-tin:LandCoverValue/el-tin:coveredPercentage | 1 | Yes
