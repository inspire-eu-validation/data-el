# Code lists

**Purpose**: Verify that code lists extensions can be accessed.

**Prerequisites**

**Test method**

* Verify that any code list extensions are publicly accessible via HTTP, i.e. inspect extensible code list values property elements. If a reference (@xlink:href) has a value that does not start with http://inspire.ec.europa.eu/codelist/, verify that a HTTP GET request to the URI retrieves a document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following empty code list:

* [SpotElevationClassValue](#SpotElevationClassValue): http://inspire.ec.europa.eu/codelist/SpotElevationClassValue


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS-EL](./README.md#ref_TG_DS_EL) 5.6.3.3.

**Test type**: Automated

**Notes**

The SpotElevationClassValue is an "externally governed" codelist and the values are not available in a registry, but are documented in a pdf.
For this reason, the following values are also accepeted because they are suggested in the [TG DS-EL](./README.md#ref_TG_DS_EL) even if they are not available in the INSPIRE Registry:

Identifier | Labels
------------------------------ | -------------------------------------------
http://inspire.ec.europa.eu/codeList/SpotElevationClassValue/0	| Created, never classified
http://inspire.ec.europa.eu/codeList/SpotElevationClassValue/1	| Unclassified
http://inspire.ec.europa.eu/codeList/SpotElevationClassValue/2	| Low Vegetation
http://inspire.ec.europa.eu/codeList/SpotElevationClassValue/3	| Medium Vegetation
http://inspire.ec.europa.eu/codeList/SpotElevationClassValue/4	| High Vegetation
http://inspire.ec.europa.eu/codeList/SpotElevationClassValue/5	| List/SpotElevationClassValue/5
http://inspire.ec.europa.eu/codeList/SpotElevationClassValue/6	| Building
http://inspire.ec.europa.eu/codeList/SpotElevationClassValue/7	| Low point (noise)
http://inspire.ec.europa.eu/codeList/SpotElevationClassValue/8	| Model Key-point (mass point)
http://inspire.ec.europa.eu/codeList/SpotElevationClassValue/9	| Water
http://inspire.ec.europa.eu/codeList/SpotElevationClassValue/12	| Overlap Points


## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression      |Multiplicity   |Voidable
---------------------------------------------------------- | -----------------------|---------------|---------------------------------
SpotElevationClassValue <a name="SpotElevationClassValue"></a> | //schema-element(el-vec:SpotElevation)/el-vec:classification/@xlink:href | 1 | Yes
