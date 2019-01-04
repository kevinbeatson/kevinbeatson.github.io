---
layout: post
published: true
title: Electronic Whiteboards using Oracle APEX
tags: [OrclApex,Showcase]
bigimg: /img/cropped-aPicture8.jpg
---

## Electronic Whiteboards

We have used [Oracle APEX](https://apex.oracle.com/) to create different display "boards" to support the care of Patients during their stay in our hospitals. These boards have been developed in house over a number of years and are built directly on our Oracle database.
Located throughout the hospitals at the point of use, most of the boards are permenantly "on" and require no user input. They auto-refresh to update every few minutes to reflect changes made on the patient administration and clinical systems. Some allow users to authenticate and drill down to see more information or update data.
These systems are designed to support the specific care of individual patients and also the management of flow of patients through the hospitals.

### Emergency Department Boards

There is one display board that shows all patient currently within the Emergency Department (ED). This can be launched with a parameter based on the location to show a shorter list of patients to those staff in that area, whereas others will show full lists of patients.
So for example here we can see the patients waiting in the Ambulance arrivals area
![EDAmbulance.jpg]({{site.baseurl}}/img/EDAmbulance.jpg)

The board shows
- The cubicle in which the patient is located
- The patients initials, sex and age
- Visual indicators. Here we can see the forget-me-not which indicates dementia, a ceiling of care alert and frailty flags
- The most recent National Early Warning Score (NEWS) and the time since the observations were taken
- Whether the patient has been streamed or assessed and what the priority level is
- If the patient has been seen by a doctor, by whom and at what time
- The responsible consultant
- If a treatment decision has been reached and how long has elapsed since the patient has been seen by a doctor 
- If canulae have been fitted
- If there are pathology or radiology results to view
- Key tasks the patient is waiting for (and for how long)
- The Glasgow Admission Prediction Score
- If the patient is ready for transfer
- For patients flagged for admissison the destination is shown (once recorded)
- If the ED Coding has been completed
- Total time in ED and the projected breach time

Most of the data items have pop up tooltips or drill downs to show more detail. All the data is held in the main ED/PAS system and queried directly. Users can authenticate using their normal network logon and perform limited updates - for example recording times or creating or acknowledging tasks 

### Arrivals Boards

The Arrivals Boards are loacted within the admitting wards areas and the control room as "permenantly on" displays. They show patients that are on their way to the wards as well as patients already admitted onto a ward. They clearly show the status of a patient in relation to their being seen by an admitting doctor. This is a key safety factor in ensuring patients get seen quickly.

![arrivalsbd.png]({{site.baseurl}}/img/arrivalsbd.png)

The screens can be configured to show specific specialties, groups of specialties or all patients. 
Te board shows
- The location of the patient (or intended location if still in ED, or coming directly from Primary Care)
- LoS (legth of Stay)
- Reason for admission & who discussed the admission 
- Sepsis Screening Status
- Clerking Status (TBS = To Be Seen)
- A flag if the patient can outlie (i.e. be sent to a ward belonging to a different specialty)
- RFT - is the patient ready to transfer

### Activity Predictor

We stream data to an Oracle 11gR2 database using Oracle Streams, we have a transformation process which runs every 15 minutes that updates the "real time" data that is displayed in this screen. This shows the position in relation to attendances to the Emergency Department and admissions and discharges to the two acute hospitals.
Current stats are shown alongside averaages, upper and lower control limits based on activity data over the preceeding two years. Colour coding is used to give a quick indication of the state of the hospital.

![edactivitybd.png]({{site.baseurl}}/img/edactivitybd.png)

### Bed Status
This board shows the bed stock of the Hospitals (only one shown in the screenshot below)
Bed managers can see the location of available beds, if they are male or female and the numbers of expected discharges today and tomorrow.
![bedstock.JPG]({{site.baseurl}}/img/bedstock.JPG)
clicking the ward shorname/number will drill down into the Ward Whiteboard so they van review detail
The screen auto-refreshes every tem minutes, but can be manually refreshed.

_more to follow_




