### Introduction

#### Purpose of document
The purpose of this document is to outline the contents of the Australian Core Data for Interoperability (AUCDI) and to provide insights into its development context. 


#### Intended audience of the document 
The intended audience of this document is stakeholders interested in improving health data interoperability in Australia. This includes consumers, clinical and technical subject matter experts, healthcare organisations, peak bodies, technology and software industry partner organisations, jurisdictions, and government organisations.


### About Sparked

#### Sparked overview

As part of 2023-24 Federal Budget funding to implement new initiatives to improve digital health information sharing, the Australian Government provided $15.7 million over two years to progress national health information sharing priorities. This funding included $9.3 million over two years for Australia’s Commonwealth Scientific and Industrial Research Organisation (CSIRO) to work with all Australian Governments, the Australian Digital Health Agency, HL7 Australia and the health technology industry to develop and adopt national data standards, including clinical information models, terminology value sets and Fast Healthcare Interoperability Resources (FHIR) standards.  

Australia’s first FHIR accelerator, ‘Sparked’, was launched in August 2023 to deliver national core clinical data for interoperability to support health information sharing, the AUCDI. Over the next two years, aligned FHIR standards to support the implementation of AUCDI in Australian settings will be developed by the technical community. 

Sparked is a community-driven collaboration comprising government, technology and software industry partners, provider organisations, clinical and industry peak bodies, healthcare practitioners, and domain experts with a common goal – to accelerate the creation and use of national FHIR standards in healthcare information exchange. 
The program is led by CSIRO’s Australian e-Health Research Centre (AEHRC) as the community coordinator in partnership with the Department of Health and Aged Care (DOHAC), the Australian Digital Health Agency (Agency) and HL7 Australia (HL7 AU). 

<img src="sparked-partnership.png" width="100%">


#### Sparked deliverables 

CSIRO is leading the clinical and technical community collaboration and consensus for developing the AUCDI and AU Core FHIR implementation guides, which are expected to be ready by mid-2025. 

Sparked will create the following products during the two-year program:
* Australian Core Data for Interoperability (AUCDI), 
* AU eRequesting Data for Interoperability (AUeReqDI),
* AU Core FHIR Implementation Guide,
* AU eRequesting FHIR Implementation Guide,
* Royal College of Pathologists Australasia (RCPA) value sets,
* Royal Australian and New Zealand College of Radiologists (RANZCR) value sets, 
* Target Operating Model for AU FHIR Standards development, and 
* Standards development roadmap to highlight priorities and sequence going forward.

<img src="sparked-deliverables.png" width="100%">

#### Sparked Community approach

Using an open and transparent standards development approach, Sparked is developing an active community of clinicians, software industry vendors, private and public healthcare organisations, and government agencies to co-design and validate nationally agreed health data standards.

This community-centric and consensus-driven approach will ensure standards are driven by community needs and are more readily understood, adopted, and implemented. This builds on the successful approach adopted globally through US-based HL7 FHIR Accelerators such as the Argonaut project. More information on these projects is in 11.2.2.
To participate in our Sparked community – visit our registration page at [sparked.csiro.au](https://sparked.csiro.au/index.php/get-involved-with-sparked). 


### About Australian Core Data for Interoperability (AUCDI)

#### Background

The Australian health IT landscape is characterised by isolated health information systems, often confined within single clinics or organisations. This fragmentation is prevalent across primary, acute, and tertiary care sectors. The consistency in health data structure is generally limited to systems provided by the same technology industry partner, leading to a lack of alignment between different clinical systems.

This situation poses significant challenges in sharing and exchanging information across systems, impacting the development of value-added services like clinical decision support. The local and often proprietary development of these systems has necessitated the mapping or transformation of health data between systems, increasing the risk of errors and potential loss of critical clinical data.

The fragmented nature of these systems complicates the capture and reuse of health data. Data captured in one system often cannot be efficiently or accurately reused in another, leading to redundant data entry and potential inconsistencies in electronic health records. This not only increases the workload for healthcare providers but also poses risks to clinical safety and quality of care. Inaccurate or incomplete data can lead to misinformed clinical decisions and compromised health outcomes.

Additionally, the focus on developing data sets for secondary rather than primary clinical use adds to the data collection burden for care providers. This approach often overlooks the immediate clinical needs and usability, potentially compromising the effectiveness of clinical decision support systems and the overall quality of health care delivered.

#### Role and purpose of AUCDI

The AUCDI is changing the approach to health data and is set to become a national asset focused on establishing an independent base of reusable, standardised information models and related artefacts.  As clinical systems converge their internal data structures towards AUCDI, this common, consensus-based data foundation will reduce the need for data transformations and mappings, supporting safer and simpler interoperability. 

The AUCDI is intentionally agnostic of:
* Any single clinical use case while being constructed as a foundation for many clinical use cases,
* Any single clinical system vendor while being strongly informed by functionality and data available in current clinical systems, and 
* Any single technical implementation or exchange approach while providing the clinical data requirements for developing the FHIR AU Core specifications and subsequent Implementation Guides (IG).

The AUCDI:
* Will provide the initial foundation for an evolving ecosystem of agreed data groups, purpose-built to reflect clinical requirements for the data required to support the provision of care, exchange, aggregation for analysis, and to support clinical decision support. 
* Describes and defines a set of data groups comprising one or more data elements, forming the foundation of a common language to allow systems to exchange semantically accurate data more efficiently.

* Will act as an agent for change by bridging fragmented silos of data and providing a foundation of building blocks of standardised data applicable to multiple use cases across a variety of clinical specialties, geographical locations, and professional contexts and problems.
* Incorporates and builds upon existing standards and ongoing work from national and international programs and initiatives. It has not been developed in isolation.
* Is a living artefact that will evolve and grow in future iterations to support additional use cases – adding breadth by including new clinical data groups and depth by expanding with further granular detail.

AUCDI Release 1 (R1) is focused on an agreement of “the core of the core” common data elements, meaning the absolute minimum data required to support standardised clinical information capture at the point of care as well as enable the safe and meaningful exchange of information to other care providers.  

##### AUCDI as a foundation

AUCDI provides the common data foundation that can be reused in other use cases. For example, the eRequesting data model leverages data groups from AUCDI, such as Sex and gender, Problem/Diagnosis summary and Adverse reaction risk summary, as well as adding new data groups that are specific to eRequesting model. AUCDI and eRequesting data groups will be packaged together to represent the complete eRequesting data model. 

The Australian eRequesting Data for Interoperability (AUeReqDI) is currently in development and will be published at the end of 2024. Future use-case specific data models can be developed using the same approach, potentially reusing some or all of the evolving ecosystem of AUCDI, AUeReqDI, and other data models as they evolve. 

<img src="sparked-foundation.png" width="100%">

#### AUCDI data groups
The AUCDI data groups are comprised of two components – clinical information models and terminologies. 

##### Clinical information models

An information model is a technical term commonly used in software engineering to describe the representation of data semantics. It is like a blueprint or map of how information and its meaning and relationships are managed and organised within a system.
Each clinical information model describes a single, discrete clinical concept and its clinically agreed data structure, pattern, and content. Some information models will be simple; others will represent a more complex grouping of related data. However, each information model includes:
* Metadata descriptions about the clinical concept and its intended purpose, purpose, and use,
* One or more component data elements, each associated with attributes such as data types, recommended values and constraints, and 
* Relationships between data elements. 
Within this document, groups of clinical information models are referred to as ‘data groups’. Examples include:
* ‘Adverse reaction risk summary’,
* ‘Procedure completed’, and
* ’Blood Pressure’.
Each clinical information model is designed to be reused across many data sets, projects, clinical scenarios, and geographical locations. Each one will vary in detail, growing in granularity over time as requirements for applications in different contexts are further understood. 

This core data for interoperability will grow towards providing a master set of information models inclusive of all relevant data elements and their attributes. Existing projects and priorities informed the development of these models and intended to be agnostic to any use case, project, application, or intent. As projects and clinical systems increasingly use the same clinical information models, data interoperability becomes significantly more straightforward because of these shared information models, minimising the need for data transformation and mapping, which can lead to errors or data loss.


##### Terminologies, SNOMED CT-AU and value sets
Within the information model, capturing data as text can be done through free text narrative or structured, coded text by selecting a word or phrase from a controlled terminology value set. A standardised set of terms is called a value set. Selection from an agreed value set from a standardised clinical terminology can dramatically improve the quality and consistency of data recording. Benefits include correct spelling, acceptable synonyms and limiting data entry selection to clinically appropriate values based on the context. Reusing agreed and validated terminology value sets within the clinical information models further enhances data exchange, clinical decision support, querying, and analysis of health data.

In Australia, SNOMED CT-AU is an adopted standard for recording structured clinical data in health records. In the Sparked program, SNOMED CT-AU is the primary terminology from which value sets are derived to support standardised coded data entry in the AUCDI’s clinical information models. Other code systems, such as LOINC, may also be used where agreed through consultation with the community of practice. Standardised terminologies have been selected because they are internationally recognised with an existing global implementation footprint.

Many SNOMED CT-AU value sets have already been developed and published by the National Clinical Terminology Service (NCTS). These nationally agreed and published value sets are maximal in nature to support reuse across multiple use cases and support the breadth of the ecosystem to enable interoperability.  Where the clinical context or use case requires it, specific IG specification or vendor implementations may specify constrained subsets of the AUCDI value sets.


#### Understanding the scope of AUCDI R1
The AUCDI focuses on core health data necessary to support high quality healthcare delivery. The first release of AUCDI, is the foundation on which more comprehensive information models will be built as standards, policies, technical implementations, and user requirements mature and evolve.

Key considerations in determining the scope of R1 were to: 
* Include data that is well understood, commonly used, and well supported by existing clinical systems,
* Identify incremental change that will create benefits and support broad reuse across multiple use cases,
* Create a starting block to build upon, avoiding breaking changes in the future as much as possible, and
* Support clinical safety and best practices.


##### Scope drivers
In designing national data standards, finding the balance between supporting current clinical practice and system implementations that are safe and scalable is crucial. There is also a tension to ensure that the design of the AUCDI can be extended to support future best practices and clinical workflow and leverage the potential for smart use of health data (e.g. CDS and AI), simultaneously avoiding the risk of backwardly incompatible changes and the cost of clinical system rework in subsequent AUCDI releases. This balance helps form a foundation to build on and evolve to become more extensive over time.  

Due to the extensive international engagement and acceptance of the International Patient Summary (11.2.5) and the need for health summary information across many clinical use cases, it was agreed  that the clinical content for a generic health summary would be used to identify many of the data groups and data elements to be included in AUCDI R1. Guided by the clinical concepts from the International Patient Summary, this content underpins any health summary or referral, supports chronic disease health assessment and management, and is a common approach to standardised clinical decision support tools such as a cardiovascular risk calculator or other health assessments (e.g., Aboriginal and Torres Strait Island Health Assessment).


##### Scope AUCDI R1

 The R1 scope of AUCDI includes: 
* Adverse reaction risk summary (allergies and intolerances),
* Problem/Diagnosis summary,
* Procedure completed,
* Vaccination administration (immunisations),
* Vital signs, measurements and other biomarkers for chronic disease and preventative health with an initial scope of cardiovascular risk calculation and diabetes care, 
* Medication use statement,
* Sex and gender, and
* Encounter information necessary to provide clinical context.

The focus of the AUCDI is the representation of the clinical content necessary for each of the data groups. System information, or system-derived information, is deliberately excluded from the scope of AUCDI unless it is also of clinically significant and requires clinical validation. Information related to technical aspects of recording data (such as author and record date/timestamp) will be managed in the technical implementation specifications (e.g., FHIR IG). 
Each data group is designed as a standalone module. The data groups can be mixed and matched to represent larger clinical data sets for use in different contexts. 
In each data group, most data elements are optional. Only a limited number of data elements within a specific data group are deemed mandatory, as the AUCDI is intentionally kept neutral for any specific use case. Data elements are only made mandatory where they are ubiquitous and considered necessary in every possible use case, or when the remainder of the data group makes no sense without a mandatory index data element. Optional data elements can be made mandatory for a specific implementation or FHIR IG.

Some data elements, for example, 'Comment' or 'Clinical Indication,' might share names and be present in several data groups to promote coherence across the data groups. 'Comment' serves as a universal data element with a uniform description across all data groups where it is found. Conversely, 'Clinical Indication' is encountered in a select few data groups. It ensures uniformity in naming and purpose across the data groups it appears in, such as 'Procedure Completed' and 'Medication Use Statement.' However, the specific semantics of each instance may be tailored to fit the concept, reusing value sets where clinically appropriate.
In R1, the scoped data models mark the foundational beginnings, “the core of the core”, on which to further build upon and fill out as the AUCDI progresses, and as further use cases and requirements mature. 

Data elements needing further community consultation or those not widely implemented and lacking significant clinical importance were omitted from the initial release (R1) and deferred to a backlog for consideration in future updates.


<img src="aucdi-scope.png" width="100%">

##### AUCDI Use cases

The community identified several priority use cases to inform the scope of AUCDI R1. These include:
* Transfer of care summary (e.g., discharge summary),
* Chronic disease management (e.g., care plan),
* Decision support (e.g., cardiovascular disease risk), and
* Referral.

##### Case study

The case study below, describes how the different AUCDI data groups can be reused to support multiple use cases, for a fictional woman named Maria. 

<div style="padding:50px;border-top: 1px solid orange;border-bottom:1px solid orange">Maria is 65-year-old women, living in regional Australia.  She leads a sedentary lifestyle, has a diet high in carbohydrates and sugars, and smokes cigarettes. She rarely consults with any Health professionals, unless her health issue is no longer self-manageable.<div>

<table>
    <tr>
        <td colspan=2>1. GP Visit - Maria visits her GP after experiencing worsening symptoms of Type 2 diabetes. During consultation, GP reviews her medical history, measures her BP, and orders some pathology tests for her current glucose levels and HbA1c, to assess her current diabetes control.
        </td>
    </tr>
    <tr>
        <td>
Related documents
* Patient summary
* Clinical notes
* Pathology request
        </td>
        <td>
Example data groups and terminology
* Problem/Diagnosis (E.g. SCT Code 44054006|Diabetes Mellitus Type 2|), Vaccination Administered, Adverse reaction risk, Sex and Gender, Tobacco smoking summary, Biomarkers (E.g. LOINC Code 4548-4: HbA1c,), Vital signs (LOINC Code 55284-4: BP), Measurements, Encounter – clinical context, Reason for test*, Test name*
        </td>
    </tr>
    <tr>
        <td colspan=2>2. Medication Management - Based on the test results, GP prescribes Metformin to improve her blood glucose control. Maria fills her prescription at a local pharmacy and begins her medication regimen.
</td>
    </tr>
    <tr>
        <td>Related documents
	Pathology results
</td>
        <td>Example data groups and terminology
	Problem/Diagnosis, Procedure completed, Adverse reaction risk, Medication statement (E.g. Medicine Name: AMT MP Code 21614011000036102|Metformin|), Sex and Gender​, Clinical indication
</td>
    </tr>
        <tr>
        <td colspan=2>3. Hospitalisation - Weeks later, Maria’s blood glucose control deteriorates to the point that she requires hospitalisation. She is admitted as an inpatient for stabilisation and also undergoes a procedure for an untreated foot ulcer
</td>
    </tr>
    <tr>
        <td>Related documents
	Hospital admission
	Discharge summary
</td>
        <td>Example data groups and terminology
	Problem/Diagnosis (E.g. SCT Code 237623001|Acute hyperglycaemia|, 371087003|Diabetic foot ulcer|), Procedure Completed (E.g. SCT-AU Code: 312733004|Debridement of foot ulcer|), Vaccination Administered, Adverse reaction risk, Medication statement, Sex and Gender, Tobacco smoking summary
</td>
    </tr>
     <tr>
        <td colspan=2>4. Discharge plan to GP - Maria is discharged from the hospital. The discharge plan includes instructions for medication management and follow-up appointments.
</td>
    </tr>
    <tr>
        <td>Related documents:
	Discharge summary
</td>
        <td>Example data groups and terminology:
	Problem/Diagnosis (E.g. 237623001|Acute hyperglycaemia|, 371087003|Diabetic foot ulcer|), Procedure Completed (E.g. SCT-AU Code: 312733004|Debridement of foot ulcer|), Medication statement, Biomarkers, Vital signs​
</td>
    </tr> <tr>
        <td colspan=2>5. Allied Health Referral - As part of her ongoing care, GP refers Maria to a Podiatrist to treat her foot ulcer and for advice regarding foot care.
</td>
    </tr>
    <tr>
        <td>Related documents:
	Referral to Allied Health
	Clinical notes
</td>
        <td>Examples data groups and terminology:
	Problem/Diagnosis (E.g. SCT-AU Code 371087003|Diabetic foot ulcer|), Procedure Completed (E.g. SCT-AU Code: 312733004|Debridement of foot ulcer|), Sex and Gender, Medication statement, Encounter – clinical context
</td>
    </tr> <tr>
        <td colspan=2>6. Specialist referral – Due to the complexity of her condition, Maria is also referred to an endocrinologist, for opinion and management of her diabetes and its complications.
</td>
    </tr>
    <tr>
        <td>Related documents:
	Referral to specialist
	Clinical notes
</td>
        <td>Example data groups and terminology:
	Problem/Diagnosis (E.g. SCT-AU Code 44054006|Diabetes Mellitus Type 2|, 371087003|Diabetic foot ulcer|), Procedure Completed, Sex and Gender, Medication statement, Encounter – clinical context
</td>
    </tr> <tr>
        <td colspan=2>7. Care plan - GP develops a comprehensive care plan for Maria, outlining her treatment, medications, lifestyle modifications, and scheduled follow-ups with her healthcare team
</td>
    </tr>
    <tr>
        <td>Related documents:
	Care plan
</td>
        <td>Example data groups and terminology:
	Problem/ Diagnosis (E.g. SCT-AU Code 44054006|Diabetes Mellitus Type 2|, Procedure Completed, Adverse reaction risk, Sex and Gender, Medication statement
</td>
    </tr> <tr>
        <td colspan=2>8. Transfer of care to new GP – Maria relocates, necessitating a transfer of her care. Her medical records, including her care plan and recent hospitalisation details are transferred to her new GP.
</td>
    </tr>
    <tr>
        <td>Related documents:
	Patient summary
	Care plan
</td>
        <td>Example data groups and terminology:
	Problem/Diagnosis, Procedure completed, Vaccination Administered, Adverse reaction risk, Sex and Gender, Medication statement, Tobacco smoking summary (E.g. SCT-AU code 77176002|Current smoker|, Biomarkers, Vital signs, Measurements, Encounter – clinical context
</td>
    </tr> <tr>
        <td colspan=2>9. Continuity of care and CVD risk - Maria continues her regular check-ups with her new GP, who reviews her medical records, coordinates her care with the podiatrist and endocrinologist, and calculates her CVD risk based on available health records as a preventative measure.
</td>
    </tr>
    <tr>
        <td>Related documents:
	Care plan
	CVD risk score
</td>
        <td>Example data groups and terminology:
	Sex and Gender, Medication statement, Tobacco smoking summary (e.g., SCT-AU code 77176002|Current smoker|), Biomarkers, Vital signs, Measurements
</td>
    </tr>

<table>

#### AUCDI, FHIR and AU Core Implementation Guide
The primary intent of the AUCDI is to design and govern a collection of coherent, reusable building blocks known as ‘data groups’. These data groups specify “what” is necessary for clinical recording and documentation, data reuse, and health information exchange.  However, it does not specify “how” the data is exchanged; this is the role fulfilled by the FHIR standard.

FHIR is the next-generation HL7 standard for exchanging healthcare data electronically. It is based on the lessons learnt from the many years of developing previous HL7 standards for healthcare data exchange.

The basic building blocks of FHIR, Resources, can be tailored to suit specific use cases by “profiling”. Whilst FHIR is an international standard, national and regional projects can provide localisation of resources and profiles. HL7 Australia’s “AU Base” IG provides localised resources extensions in the Australian context. AU Core specifies minimum data element support and system behaviour capability for a system to record, update, search, and retrieve core health and administrative information.
AU Core FHIR IG has been developed in reference to the AUCDI, representing the AUCDI data groups as FHIR artefacts. The Sparked HL7 AU Core Technical Design Group (AU Core TDG) has been tasked to design the AU Core FHIR IG under the governance framework of the [HL7 AU Australian FHIR Management Framework](https://confluence.hl7.org/display/HA/Australian+FHIR+Management+Framework).


<img src="aucdi-focus.png" width="100%">

#### Design of the AUCDI

The AUCDI has been developed in collaboration with the community and is informed by the key data drivers such as clinical recording and documentation, clinical decision support, data reuse and reporting requirements. 

<img src="aucdi-relationship.png" width="100%">

In order to support maximum reuse and leveraging previous investment, the data model has been informed by other key local and international initiatives and programs such as previous Australian specifications and international standards. This includes:
* My Health Record Specifications, 
* CSIRO Primary Care Data Quality Foundations (PCDQF), 
* AIHW Minimum Data Sets,
* International Patient Summary (IPS),
* The pan-Canadian Health Data Content Framework,
* United States Core Data for Interoperability (USCDI), 
* UK Professional Record Standards Body (PRSB),
* HL7 FHIR, and
* openEHR.

<img src="aucdi-aucore.png" width="100%">

The initial design of the AUCDI commenced in 2018 during the PCDQF project with an analysis of existing data in primary care clinical systems and national standards. The AUCDI has built upon this foundation, referencing a broader range of national and international standards and initiatives described.

The AUCDI is deliberately designed with a focus on clinicians and stakeholders, ensuring that the conceptual data models represent common, well-defined requirements identified from agreed use cases. The AUCDI direction and scope were established through in-person workshops involving clinicians, informaticians, software engineers, and other stakeholders, conducted over a period of months across 2023 and 2024. The structured representation of the AUCDI concepts in R1 has been informed by established clinical information model standards, particularly openEHR archetypes, which have been purposely developed by clinicians and informaticians focused on ensuring high-quality structured clinical data that is clinically safe and fit for purpose.

Core Design principles were developed to assist the development of AUCDI and to allow prioritisation by the Sparked team and the community. The following table sets out the design principles used and how the clinical information model has been aligned. 

<table>
<tr>
    <th>Design Principles</th><th>Alignment</th>
</tr>
<tr>
    <td>Reduce duplication - single entry, single development (multiple use and reuse)</td>
    <td>Data collected in a structured and coded manner enables data to be reused for clinical decision support; the population of summary information, forms, and letters; and for secondary use such as population health planning.</td>
</tr>
<tr>
    <td>Supports person-centred care - driven by a clinical quality and safety use case</td>
    <td>Using standardised coded structured data for health information will support good clinical care, unambiguous transfer of clinical information and clinical decision support. This allows delivery of the right care to the right person at the right time.</td>
</tr>
<tr>
    <td>No data for data’s sake</td>
    <td>Every proposed data element has a practical purpose.
Data models are intentionally minimal to start with, incorporating the minimum data elements to support safe and effective care, rather than collecting a comprehensive data set. In future releases, new data group concepts will be added and the level of detail of existing data groups will be increased to support clinical priorities and data requirements.
</td>
</tr>
<tr>
    <td>Driven by clinical data use first</td>
    <td>Clinical data collection should be driven by primary use first – clinical use; however secondary use should still be considered. Data designed for clinical use at the point of care should also enable the data to be reused and aggregated for secondary purposes.</td>
</tr>
<tr>
    <td>Supports best practice care, clinical guidelines, and clinician workflow </td>
    <td>The use of standardised, coded, structured data for clinical information will support best practice clinical care, clinical decision support including guidelines, and streamlined clinician workflow.</td>
</tr>
<tr>
    <td>Systems can support now or with minimal effort</td>
    <td>Most systems can support the minimal model represented in R1. In future releases, the R1 data groups may be enhanced or new data groups added to evolve towards a strategic roadmap with an agile iterative process.</td>
</tr>
<tr>
    <td>Alignment with national health data standards and initiatives</td>
    <td>Reference national standards and initiatives, such as:
* SNOMED CT-AU and the Australian Medicines Terminology (AMT)
* My Health Record
* The Royal Australian College of General Practitioners “Minimum requirements for general practice clinical information systems to improve usability”
</td>
</tr>
<tr>
    <td>Alignment with international standards and initiatives</td>
    <td>Reference international standards and initiatives, such as:
* International Patient Summary
* HL7 Gender Harmony Project
* Information models:
  * FHIR Resources
  * openEHR archetypes
</td>
</tr>
<tr>
    <td>Involve and consider all healthcare domains and care modalities </td>
    <td>The data groups are agnostic of any specific use case and needs to support usage in all healthcare domains and across healthcare modalities. Stakeholders engaged include primary, acute, and tertiary care and specialised domains and professions such as aged care and allied health.</td>
</tr>
</table>

More information on the rationale and approach to these design principles can be found in 10.3 and how they align with AUCDI R1.

### The AUCDI R1 library at a glance
The scope of the AUCDI R1 library of data groups (as clinical information models) is focused on commonly used clinical concepts, comprising of data elements confirmed by clinicians as ‘core’ for their clinical documentation and broadly supported by existing clinical information systems. The library is composed of the data groups and their component elements shown as below.

<img src="aucdi-glance.png" width="100%">
