# Constraints

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

* Constraints of the spatial object type SpotElevation:
	* The dimension of the property value coordinate shall be 1
	* The property value shall be expressed referring to a vertical coordinate reference system
	
* Constraints of the spatial object type ContourLine:
	* The dimension of the property value coordinate shall be 1.
	* The property value shall be expressed referring to a vertical coordinate reference system.

**Prerequisites**

**Test method**

The following checks are performed for every feature in the dataset:

* Check that the [dimension](#dimensionSE) of the property value coordinate, of the SpotElevation feature type, is 1 (OCL: "inv: propertyValue.dimension=1").

* Check that the [dimension](#dimensionCL) of the property value coordinate, of the ContourLine feature type, is 1 (OCL: "inv: propertyValue.dimension=1").

The following checks shall be manually performed for every feature in the dataset:

* Check that the property value of the SpotElevation feature type is expressed referring to a vertical coordinate reference system.

* Check that the property value of the ContourLine feature type is expressed referring to a vertical coordinate reference system.


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-EL](./README.md#ref_TG_DS_EL) 5.6.2.1.2.; 5.6.2.1.5.
* [IR-ISDSS](./README.md#ref_IR-ISDSS) Annex III, Sections 1.5.1.2. and 1.5.1.3.

**Test type**: Automated + Manual

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
dimension SpotElevation <a name="dimensionSE"></a> | //schema-element(el-vec:SpotElevation)/el-vec:propertyValue | 1 | No
dimension ContourLine <a name="dimensionCL"></a> | //schema-element(el-vec:ContourLine)/el-vec:propertyValue | 1 | No