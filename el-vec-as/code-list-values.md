# Code list values

**Purpose**: Verify whether all attributes whose value type is a code list take the values set out therein

**Prerequisites**

**Test method**

When an attribute has a code list as its type, verify that the values comply with the definitions and include the values set out in Annex II, III and IV of the Implementing Rule. To pass this test verify that any instance of an attribute:

* takes only values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'none'.
* takes only a value explicitly specified in the INSPIRE code list register or shall take a value that is narrower (i.e. more specific) than those explicitly specified in the application schema when the code list‘s extensibility is 'narrower'.
* takes values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'open' or if a value is not one of the values listed in the code list register check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule and that all extensions conform to the requirements (This last check is a manual test).

The following check is performed for every feature in the dataset, for the not extensible codelist:

* Check that all the [datumWaterLevel](#datumWaterLevel) element has a xlink:href attribute pointing to a [valid value](#validValue1). If the check fails report [disallowedCodeListValue](#disallowedCodeListValue).

| <a name="validValue1"></a> Valid values for xlink:href attribute of [datumWaterLevel](#datumWaterLevel) element are available in the INSPIRE Registry. | 
| ---- | 
| WaterLevelValue: http://inspire.ec.europa.eu/codelist/WaterLevelValue |


The following check is performed for every feature in the dataset, for the 'narrower' codelist:

* Check that all the [spotElevationType](#spotElevationType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue1). If the check fails a manual check will be required asking to review the codelist definition in order to verify that any extensions do not overlap with the codelists that are defined in Annexes II, III and IV of the Implementing Rule. In particular, for the 'narrower' codelists the extended values shall refer to a parent value defined by the Implementing Rule. If the check fails report [reviewCodeListValue](#reviewCodeListValue).

* Check that all the [breakLineType](#breakLineType) elements has a xlink:href attribute pointing to a [pre-defined value](#preDefinedValue2). If the check fails a manual check will be required asking to review the codelist definition in order to verify that any extensions do not overlap with the codelists that are defined in Annexes II, III and IV of the Implementing Rule. In particular, for the 'narrower' codelists the extended values shall refer to a parent value defined by the Implementing Rule. If the check fails report [reviewCodeListValue](#reviewCodeListValue).

| <a name="preDefinedValue1"></a> Pre-defined values for xlink:href attribute of [spotElevationType](#spotElevationType) element are available in the INSPIRE Registry| 
| ---- | 
| SpotElevationTypeValue: http://inspire.ec.europa.eu/codelist/SpotElevationTypeValue |

| <a name="preDefinedValue2"></a> Pre-defined values for xlink:href attribute of [breakLineType](#breakLineType) element are available in the INSPIRE Registry| 
| ---- | 
| BreakLineTypeValue: http://inspire.ec.europa.eu/codelist/BreakLineTypeValue |
 


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (1)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (3)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (1)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (2)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (4)

**Test type**: Automated + Manual check (if required)

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
disallowedCodeListValue <a name="disallowedCodeListValue"/> | XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that is not one of the allowed values listed at $codelist. Please note that the URIs of all code list values from the INSPIRE Registry shall be referenced using the http protocol.
reviewCodeListValue <a name="reviewCodeListValue"/> | XML document '{filename}', {featureType} '{gmlid}': The property '{property}' has a value '{value}' that is not one of the pre-defined values in the INSPIRE data specification. The same value is used by {count} other features in the dataset, too. Extensions to the pre-defined values are allowed, but must not overlap with one of the pre-defined values and be consistent with the specification of the property. Please review the definition of the value. Please note that the URIs of all code list values from the INSPIRE Registry shall be referenced using the http protocol. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression				|Multiplicity       |Voidable
---------------------------------------------------------- | -------------------------------|-------------------|---------
datumWaterLevel <a name="datumWaterLevel"></a> | //schema-element(el-vec:ContourLine)/el-vec:localDepthDatum/el-vec:ChartDatum/el-vec:datumWaterLevel/@xlink:href | 1 (The parent element is optional) | No
spotElevationType <a name="spotElevationType"></a> | //schema-element(el-vec:SpotElevation)/el-vec:spotElevationType/@xlink:href | 1 | Yes
breakLineType <a name="breakLineType"></a> | //schema-element(el-vec:BreakLine)/el-vec:breakLineType/@xlink:href | 1 | No