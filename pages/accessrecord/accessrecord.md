---
title: Access Record HTML
keywords: getcarerecord
tags: [getcarerecord]
sidebar: accessrecord_sidebar
permalink: accessrecord.html
summary: "Introduction to the GP Connect Access Record HTML capability."
---

{% include todo.html content="This capability pack is published as a **work in progress** version and as such is subject to change. It has been published to show the direction of travel and to serve as a discussion document for parties involved with the implementation and consumption of GP Connect FHIR based APIs." %}

For direct patient care purposes only, the primary care record contains a wealth of useful information that can improve patient safety and efficiency if it is made interoperable (subject to information governance (IG) and clinical safety requirements) across health care settings.

{% include important.html content="See [NHS Digital - FAQ on legal access to personal confidential data - Definitions questions - How is Direct Patient Care defined?](http://content.digital.nhs.uk/article/3638/Personal-data-access-FAQs){:target='_blank'} for details of what constitutes direct patient care." %}

The information sections initially in scope for care record access (Stage 1) are:

1. Summary
2. Encounters
3. Clinical Items
4. *Administrative Items*<sup>*</sup>
5. Referrals
6. Immunisations
7. Problems and Issues
8. Medications
9. Observations
10. *Investigations*<sup>*</sup>
11. Allergies and Adverse Reactions
12. Patient Demographics (minimal)
13. Patient's GP Practice and Organisation (minimal)


{% include important.html content="The Clinical Items section exists as it is not currently possible to reliably distinguish procedures, diagnoses, symptoms and other clinically coded items into their own sections due to the way they are stored in the primary care record principal systems. " %}

{% include important.html content="Initially some sections of the patient care record (marked above with a <sup>*</sup> may not initially be available from all primary care record principal systems.  The Investigations section will be considered for Stage 2 so for Stage 1 numeric results will be included in the Observation section." %}

## HTML View ##

{% include roadmap.html content="Work is currently underway to refine the GP Connect HTML views to ensure alignment (where appropriate) with SCR, GP2GP and GPES requirements." %}

### Purpose ###

In an unstructured and pre-rendered format (HTML), this capability will provide health professionals with access to a patient's primary care record by requesting sections or headings. Where appropriate, a date range can be defined to filter the retrieval of larger sections. These views can be incorporated directly into electronic patient record systems.

Significant effort has already been made to unify the HTML section views from all four principal suppliers but it is expected that this will be an iterative process during development, user acceptance testing (UAT) and First of Type (FoT).

The content displayed in the HTML views has then been used as a common baseline of available data to guide the structured and coded Access Record approach.

### Use Cases ###

- Extended access GP practices can view all of the patient's primary care views even when the record is held on a different GP system
- Other care settings (for example, 111, Physio, Community, Emergency, Acute/Secondary, Social) can view the patient's GP record (those held by the patient's recorded GP practice) to better inform care decisions they may be making for a patient.

### Profiled FHIR Resources ###

See the [AccessRecord HTML FHIR Resources](datalibraryaccessRecord.html) page for details of the FHIR profiles used for the Access Record HTML operation.

### SPINE Interactions ###

The Access Record HTML capability message set includes the following set of Spine interactions:

| Operation                 | InteractionID             | 
|---------------------------|---------------------------| 
| [Get Care Record](accessrecord_use_case_retrieve_a_care_record_section.html) | `urn:nhs:names:services:gpconnect:fhir:operation:gpc.getcarerecord-1` |
