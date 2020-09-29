
# Introduction

Thes APIs are developed to interoperate with the [General Practitioner EHR system](https://github.com/Morail/introsde_project_dfr)
# Description

The APIs allow the requester to perform different operation on a single main resource `patients`.

## Operation on patients resource
CRUD operation on the entities are redirected to the integrated system. The entities can be added, modified, retrieved or deleted. 

 - `GET /patients` together with the detailed view `GET /patients/{patientId}` 
 - `POST /patients` to create a new patient in the GP's EHR database
 - `PATCH /patients/{patientId}` to modify the information about a single patient
 - `DELETE /patients/{patientId}` to delete that entity from the EHR database

## Operations on prescriptions and measurements
In addition to the CRUD operation on the patients resource it is possibile to query the EHR for `prescriptions` and `measurements` linked to a specific `patient`. Also these two resources can also be created and submitted to the EHR system as well.

- `GET, POST /patients/{patientId}/prescriptions` 
- `GET, POST /patients/{patientId}/measurements` 
