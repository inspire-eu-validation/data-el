# Conformance class: Information accessibility, Elevation

Conformance class for the requirements related to the accessibility of referenced information, for example, information stored in registries (code lists, coordinate reference systems).

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schemas, Elevation".

This conformance class is part of the [INSPIRE Data Specification on Elevation](../README.md).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the data set, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](#ref_TG_DS_tmpl) | [Information accessibility](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/information-accessibility) | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-EL](#ref_TG_DS_EL) | [GML application schemas, Elevation](../el-gml/README.md) | INSPIRE spatial data set encoded in GML, Elevation features | n/a |
 
## Feature types <a name="feature-types"></a>

The instantiable feature types are:

* For coverage datasets:

	* ElevationGridCoverage
	
* For vector datasets:

	* Breakline
	* ContourLine
	* IsolatedArea
	* SpotElevation
	* VoidArea
	
* For TIN datasets:
	
	* ElevationTIN


*Note*: When "features" or "spatial objects" are mentioned in the test cases, this refers only to instances of feature types of this application schema, not to any types specified in any other application schema.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-EL <a name="ref_TG_DS_EL"></a>   | [INSPIRE Data Specification on Elevation – Technical Guidelines version 3.0](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_EL_v3.0.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-EL](#ref_TG_DS_EL)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Code lists](./code-list.md)  | ready for review  | A.5.1 |
| [Feature references](./features.md)  | ready for review  | A.1.4 |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
gml            | http://www.opengis.net/gml/3.2
el-cov         | http://inspire.ec.europa.eu/schemas/el-cov/4.0
el-vec		   | http://inspire.ec.europa.eu/schemas/el-vec/4.0
el-tin	 	   | http://inspire.ec.europa.eu/schemas/el-tin/4.0

The following variables are used to refer to the corresponding Xpath expressions in all test descriptions:

Variable       | Value
-------------- | -------------------------------------------------
$features      |  //schema-element(el-cov:ElevationGridCoverage) <br> //schema-element(el-vec:Breakline) <br> //schema-element(el-vec:ContourLine) <br> //schema-element(el-vec:IsolatedArea) <br> //schema-element(el-vec:SpotElevation) <br> //schema-element(el-vec:VoidArea) <br> //schema-element(el-tin:ElevationTIN)