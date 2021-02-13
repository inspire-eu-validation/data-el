# Conformance class: Data consistency, Elevation

Conformance class for the requirements related to the consistency of the data.

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has a direct dependency to the conformance class "INSPIRE GML application schemas".

This conformance class is part of the [INSPIRE Data Specification on Elevation](../README.md).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the data set, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](#ref_TG_DS_tmpl) | [Data consistency](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/data-consistency) | n/a |

### Indirect dependencies

none

 
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
TG DS-EL-corr <a name="ref_TG_DS_EL_corr"></a>   | [Corrigenda to the INSPIRE Data Specification on Elevation – Technical Guidelines version 3.0](https://inspire.ec.europa.eu/file/1609/download?token=9WROnWt0)
IR-ISDSS <a name="ref_IR-ISDSS"></a>   | [Commission Regulation (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](https://eur-lex.europa.eu/eli/reg/2010/1089/2014-12-31)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-EL](#ref_TG_DS_EL)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Specific requirement related to metadata](./metadata-specific-req.md)  | ready for review  | A.4 |
| [Contour line test](./contour-line-test.md)  | ready for review  | A.3.6 |
| [Break line test](./break-line-test.md)  | ready for review  | A.3.7 |
| [Isolated area test](./isolated-area-test.md)  | ready for review  | A.3.8 |


## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
el-cov         | http://inspire.ec.europa.eu/schemas/el-cov/4.0
el-vec	 	   | http://inspire.ec.europa.eu/schemas/el-vec/4.0
el-tin	 	   | http://inspire.ec.europa.eu/schemas/el-tin/4.0
gml            | http://www.opengis.net/gml/3.2