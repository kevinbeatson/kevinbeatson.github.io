---
layout: post
published: true
title: Electronic Whiteboards using Oracle APEX
---

## Electronic Whiteboards

We have used Oracle APEX to create different display "boards" to support the care of Patients during their stay in our hospitals. These are built directly on our Oracle database. These boards have been developed in house over a number of years.
Most of the boards are permenantly "on" and require no user input. They auto-refresh to update every few minutes. Some allow users to authenticate and drill down to see more information or update data.
These systems are designed to support the specific care of individual patients and the management of the flow of patients throught the hospitals.

### Emergency Department Boards

There is one display board that shows all patient currently within the Emergency Department (ED). This can be launched with launched with a parameter based on the location within the department to show a smaller list of patients pertinent to those under he care of staff in that area.
So for example here we can see the patients waiting in the Ambulance arrivals area

![EDAmbulance.jpg]({{site.baseurl}}/img/EDAmbulance.jpg)
The board shows;
- The Cubicle in which the patient is located
- the patients initials, sex and age
- visual indicators, here we can see the forget-me-not which indicates dementia, a ceiling of care alert and frailty flags
- The most recent National Early Warning Score (NEWS) and the time since the observations were taken
- whether the patient has been streamed or assessed and whatthe priority level is
- if the patient has been seen by a doctor, by whom and at what time
- the responsible consultant
- if a treatment decision has been reached and how long has elapsed since the patient has been seen by a doctor 
- if Canulae have been fitted
- if there are pathology or radiology results to view
- key tasks the patient is waiting for (and how long)
- the Glasgow Prediction Score
- if the patient is ready for transfer
- for patients flagged for admissison the destination is shown (once recorded)
- total time in ED
- if the ED Coding has been completed
- total time in ED and the projected breach time

Most of the data items have pop up tooltips/more detail. All the data is held in the main ED/PAS system and queried directly.






