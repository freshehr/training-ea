# 17th Dec 13:00 openEHR workshop Session 3

## Agenda

## East Accord: openEHR Workshop 17th December 2020
| Topic                                    | Dtn. | Start | End   |
| ---------------------------------------- | ---- | ----- | ----- |
| What do we mean by ReSPECT+?             | 45   | 13:00 | 13:45 |
| Break                                    | 10   | 13:45 | 13:55 |
| Candidate information models             | 45   | 13:55 | 14:40 |
| Break                                    | 10   | 14:40 | 14:50 |
| Towards Patient-centric information?	    | 45   | 14:50 | 15:35 |
| Break                                    | 10   | 15:35 | 14:45 |
| Practical archetyping/templating         | 45   | 15:45 | 16:30 |
| Questions/ issues		 		             | 10   | 16:30 | 16:40 |

## Practical tooling 

We will be doing most of this work as a single group but if you do wish to work yourself with the archetype and template tooling 
1. Open a web browser – Chrome or Firefox are best

2. Go to [https://tools.openehr.org/designer](https://tools.openehr.org/designer/) 
(Best if you open this link in a new tab).


3. Login: 		`freshehr_training`	
   Password: 	`ad4freshtraining`


### Technical material

We will not be doing any specific technical work in this session but for you may find this document helpful as a follow-up to the brief Technical Intro.

https://freshehr.github.io/dhi-proms/


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

What is openEHR? - Introduction: https://www.openehr.org/about/what_is_openehr

openEHR Zotero library: https://www.zotero.org/libraries


Clinical Knowledge Managers (CKMs) - archetype repositories and governance tools:

International CKM: https://ckm.openehr.org/ckm/

Apperta CKM (UK): https://ckm.apperta.org/ckm/


