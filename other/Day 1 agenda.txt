# openEHR workshop Session 1

## Agenda

## East Accord: openEHR Training Session One 08-Dec-2020

| Topic                                    | Dtn. | Start | End   |
| ---------------------------------------- | ---- | ----- | ----- |
| Intro			 ?                         | 10   | 09:00 | 09:10 |
| What is openEHR?                         | 45   | 09:10 | 09:55 |
| Break                                    | 10   | 09:55 | 10:05 |
| Introduction  to Archetype and Templates | 45   | 10:05 | 10:50 |
| Break                                    | 10   | 10:50 | 11:00 |
| Build an  openEHR app demo               | 45   | 11:00 | 11:45 |
| Break                                    | 5    | 11:45 | 11:50 |
| Practical  modelling                     | 45   | 11:50 | 12:35 |
| Break                                    | 5    | 12:35 | 12:40 |
| Tech  intro/ wash-up                     | 20   | 12:40 | 13:00 |


## Practical session - Getting started

1. Open a web browser – Chrome or Firefox are best

2. Go to [https://tools.openehr.org/designer](https://tools.openehr.org/designer/) 
(Best if you open this link in a new tab).


3. Login: 		`freshehr_training`	
   Password: 	`ad4freshtraining`

4. Choose the repository allocated to you – Aberdeen or Dundee

5. Find ‘Nursing Admission Assessment STARTER.v0' in the list of templates. This will open the template.

6. Open the original ['Nursing Admission Assessment paper form'](Nursing%20Admission%20Assessment.pdf) (Best if you open this link in a new tab). 


## A. Tidy the basic template

### Problem/Diagnosis	

 - Rename the Problem/Diagnosis archetype to 'Main Diagnosis'

- Constrain out everything apart from 'Problem/Diagnosis name'

### Adverse Reaction Risk

- Pull in the 'Adverse Reaction Risk' archetype

- Set it's occurrences to 0..* to allow multiple allergies to be recorded.
  
- Constrain out everything apart from 'Substance' and 'Manifestation'

- Rename ‘Manifestation’ to ‘Reaction Details’ and make it mandatory

### Medication Order

- Clone 'Specific direction description'

- Rename one to 'Dose' and the other to 'Frequency'

### Vital Signs section

 - Pull in Pulse Oximetry into Vital Signs section

- Constrain out everything apart from 'SpO2' ratio

- Make 'systolic' and 'diastolic' Blood pressure mandatory


### Add a Clinical Frailty scale

Go to the International CKM 

[https://ckm.openehr.org/ckm/archetypes/1013.1.4691/export](https://ckm.openehr.org/ckm/archetypes/1013.1.4691/export)

 (Best if you open this link in a new tab).

- Press the ‘Export ADL’ button and save the archetype somewhere on your system

- Go back into Archetype Designer and go to top-menu->‘Import’ then either Browse to your file or drag and drop then Upload.

- Go back to your template, click on ‘content’, then pull in the Clinical Frailty scale from the list of archetypes on the right.

## B. Create a new local archetype - Additional information on admission

The nurses have used the templates you created but have asked for some changes.

You can view the original document here  

['Additional Information on Admission'](Additional%20information%20on%20admission.pdf) (Best if you open this link in a new tab).


- Create a new ADMIN_ENTRY archetype called ‘Inpatient admission details’ then add these ‘element’ datapoints ...

**Mode of access**	

			Ambulatory  	

			Wheelchair	

			Stretcher	

			Other		_________________________________

**Transported with	Oxygen**	

			Monitor	

			IV		

			Other		_________________________________

**Admission method	Waiting list**		

			Booked		

			Planned		

			A&E department	

			General Practitioner	

			Bed Bureau	

				Consultant Clinic	

			Other			____________________________		

**Additional Help needed**	

		Yes  	     No  

Once you have created your new archetype, go back to your template. Highlight ‘content’ and add your new archetype then Save it.

## Download Postman artefacts

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/7643fba2c3a2034777e4#?env%5Bdhi-scotland%5D=W3sia2V5IjoiZWhyc2NhcGVCYXNlVXJsIiwidmFsdWUiOiJodHRwczovL2Nkci5jb2RlNGhlYWx0aC5vcmcvcmVzdC92MSIsImVuYWJsZWQiOnRydWV9LHsia2V5Ijoib3BlbmVockJhc2VVcmwiLCJ2YWx1ZSI6Imh0dHBzOi8vY2RyLmNvZGU0aGVhbHRoLm9yZy9yZXN0L29wZW5laHIvdjEiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6Im9wZW5FaHJFeHBsb3JlciIsInZhbHVlIjoiaHR0cHM6Ly9leHBsb3Jlci5jb2RlNGhlYWx0aC5vcmcvZXhwbG9yZXIiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6IkNEUk5hbWUiLCJ2YWx1ZSI6ImVocnNjYXBlLmNvbSIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiZG9tYWluU3VmZml4IiwidmFsdWUiOiJjb2RlNGhlYWx0aC5vcmciLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6IlNlc3Npb25IZWFkZXIiLCJ2YWx1ZSI6IkVoci1TZXNzaW9uLWRpc2FibGVkIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJVc2VybmFtZSIsInZhbHVlIjoiYTgxZjQ3YzYtYTc1Ny00ZTM0LWI2NDQtM2NjYzYyYjRhMDFjIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJQYXNzd29yZCIsInZhbHVlIjoiJDJhJDEwJDYxOWtpIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJBdXRob3JpemF0aW9uIiwidmFsdWUiOiJCYXNpYyBZVGd4WmpRM1l6WXRZVGMxTnkwMFpUTTBMV0kyTkRRdE0yTmpZell5WWpSaE1ERmpPaVF5WVNReE1DUTJNVGxyYVE9PSIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiYWNjb3VudE5hbWUiLCJ2YWx1ZSI6ImRoaS1zY290bGFuZCIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiY29tbWl0dGVyTmFtZSIsInZhbHVlIjoiRHIgQ2hhbCIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoicGF0aWVudE5hbWUiLCJ2YWx1ZSI6Ikl2b3IgQ294IiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJzdWJqZWN0SWQiLCJ2YWx1ZSI6Ijk5OTk5OTkwMDAiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6Im5oc051bWJlciIsInZhbHVlIjoiOTk5OTk5OTAwMCIsImVuYWJsZWQiOnRydWV9LHsia2V5Ijoic3ViamVjdE5hbWVzcGFjZSIsInZhbHVlIjoidWsubmhzLm5oc19udW1iZXIiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6ImVocklkIiwidmFsdWUiOiIzZTY3NDczOS05NTBjLTRiOGEtOTc2Yi01YWVmMjFjNjE4YzUiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6InBhcnR5SWQiLCJ2YWx1ZSI6IjQwOTUwMyIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoidGVtcGxhdGVJZCIsInZhbHVlIjoiRm9vdF9hbmRfQW5rbGVfUFJPTXMtdjAiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6ImNvbXBvc2l0aW9uSWQiLCJ2YWx1ZSI6IjA5NWFkYzg3LTcxY2MtNDFlMS1hYTQ2LWFmOWQ3MmY4ZGRmNjo6YTgxZjQ3YzYtYTc1Ny00ZTM0LWI2NDQtM2NjYzYyYjRhMDFjOjoxIiwiZW5hYmxlZCI6dHJ1ZX1d)

ehrscapeBaseUrl: https://cdr.code4health.org/rest/v1

openehrBaseUrl: https://cdr.code4health.org/rest/openehr/v1

https://cdr.code4health.org/studio


### Further reading

#### General Information:

openEHR website: https://www.openehr.org/

openEHR videos and presentations: https://www.youtube.com/c/openehr/featured

openEHR Discourse (discussion forum): https://discourse.openehr.org/

What is an open platform? - https://inidus.com/what-is-an-open-platform/

What is openEHR? - Introduction: https://www.openehr.org/about/what_is_openehr


openEHR Zotero library: https://www.zotero.org/libraries


Clinical Knowledge Managers (CKMs) - archetype repositories and governance tools:

International CKM: https://ckm.openehr.org/ckm/

Apperta CKM (UK): https://ckm.apperta.org/ckm/


#### Social Care Examples:

Social Care Project on Apperta CKM: https://ckm.apperta.org/ckm/projects/1051.61.50
A repository for the social care related archetypes and templates that we have been working on for various use cases
Care Home Dataset template: https://ckm.apperta.org/ckm/templates/1051.57.273

Based on the care home data inventory described in a recent paper by Lucy Johnston et al from Edinburgh Napier University, which is available here: https://www.medrxiv.org/content/10.1101/2020.08.17.20176503v2 

The original data inventory is shown below, along with another care home dataset that we have used as an example in our data models.
![](images/care-home-data-stds.png)
