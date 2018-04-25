---
title: FHIR&reg; resources overview
keywords: getcarerecord
tags: [design,structured]
sidebar: accessrecord_structured_sidebar
permalink: accessrecord_structured_development_resources_overview.html
summary: "List of FHIR resource profiles used in the Access Record Structured capability pack"
---

## Resources ##

The following profiled <span class="stu3">STU3</span> FHIR&reg; resources are used in this capability pack:

### Clinical ###

* [AllergyIntolerance](accessrecord_structured_development_allergyintolerance.html)
* [Medication](accessrecord_structured_development_medication.html)
* [MedicationStatement](accessrecord_structured_development_medicationstatement.html)
* [MedicationRequest](accessrecord_structured_development_medicationrequest.html)

### Administrative ###

* Patient
* Organization
* Practitioner
* Location

{% include tip.html content="Please see the [Foundations](foundations.html) section for details on population and consumption of the administrative resources." %}

### Structural ###

* [Bundle](accessrecord_structured_development_bundle.html)
* [List](accessrecord_structured_development_list.html)

## Common code and identifier systems ##

### Common code systems ###

The following common code systems are used when populating `CodeableConcept.coding.system` in resources for this capability:

| Name | Code system |
| ----------- | ------ |
| SNOMED CT   | `http://snomed.info/sct` |
| Read codes V2     | `http://read.info/readv2` |
| Read codes CTV3   | `http://read.info/ctv3` |


### Common identifier systems ###

The following common identifier systems are used when populating `Identifier.system` in resources for this capability:

| Name | Applies to | Identifier system |
| ---------- | -------- | ------ |
| NHS number | Patient | `https://fhir.nhs.uk/Id/nhs-number` |
| ODS code | Organisation | `https://fhir.nhs.uk/Id/ods-organization-code` |
| ODS site code | Location | `https://fhir.nhs.uk/Id/ods-site-code` |
| SDS user ID | Practitioner | `https://fhir.nhs.uk/Id/sds-user-id` |
| SDS role profile ID | Practitioner | `https://fhir.nhs.uk/Id/sds-role-profile-id` |


