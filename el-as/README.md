# Conformance class: Application schema, Elevation Base Types

Conformance class for the requirements associated with the application schema. 

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schemas, Elevation".

This conformance class is part of the [INSPIRE Data Specification on Elevation](../README.md).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

none

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-EL](./README.md#ref_TG_DS_EL) | [GML application schemas, Elevation](../el-gml/README.md) | INSPIRE spatial data set encoded in GML, Elevation features | n/a |
 
## Feature types <a name="feature-types"></a>

This application schema defines only two enumarations, used by feature types defined in the other application schemas. It is used to associate the specific-requirements that relate to objects defined by the other application schemas.


*Note*: When "features" or "spatial objects" are mentioned in the test cases, this refers to instances of feature types of the two application schemas, Elevation Grid Coverage and Elevation Vector Elements.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-EL <a name="ref_TG_DS_EL"></a>   | [INSPIRE Data Specification on Elevation – Technical Guidelines version 3.0](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_EL_v3.0.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-EL](#ref_TG_DS_EL)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Data provision](./data-provision.md)  | Draft  | A.1.6  |
| [External Object Identifiers](./ext-object-id.md)  | Draft  | A.1.6  |

External Object Identifiers

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
el-cov         | http://inspire.ec.europa.eu/schemas/el-cov/4.0
el-vec	 	   | http://inspire.ec.europa.eu/schemas/el-vec/4.0
el-tin	 	   | http://inspire.ec.europa.eu/schemas/el-tin/4.0
base           | http://inspire.ec.europa.eu/schemas/base/3.3
gml            | http://www.opengis.net/gml/3.2
wfs            | http://www.opengis.net/wfs/2.0
xsi            | http://www.w3.org/2001/XMLSchema-instance
xlink          | http://www.w3.org/1999/xlink
xml            | http://www.w3.org/XML/1998/namespace
