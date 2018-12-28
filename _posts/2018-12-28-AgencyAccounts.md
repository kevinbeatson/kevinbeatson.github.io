---
layout: post
title: Agency Logons
#subtitle: Excerpt from Soulshaping by Jeff Brown
bigimg: /img/cropped-aPicture8.jpg
#tags: [books, test]
---
## The Problem with Nurse Access

We use a lot of Bank and Agency Staff.
To login to Nursing Assessments, Vital Signs recording and EPMA the user has to login using a valid CPD User account (CPD is our ePR/PAS).
These accounts are Single Sign on, and so must be set up in active directory. This is problematic, since Agency nurses tend to pitch up out of hours quite a lot!

Our initial approach was to have agency staff accounts all setup and ready for this; AGENCY1, AGENCY2 etc.
The idea was that the local service would have “sealed envelopes” with user names, passwords and instructions. Once used, the details would be passed back to central user admin and the accounts re-set. There were a few problems with this;
The admin process isn’t really sustainable
Generic accounts with known passwords are not really a good thing!
The audit on any screen would show “AGENCYn” — we’d need to cross reference against a manual list of who had what & when
These agency logins can be shared i.e. more than one user using an agency login concurrently
overall — a pretty poor approach.

## What We Did
First thing was that the Nurse Bank Management and Medical Staffing got a grip as far as possible telling all Bank that they need to be on the system and trained, with access before they will get shifts. Locums need to arrange training & access  before the shift start.
Managing the process better massively reduced the problem.

## A note about the Laptops
Booting up a laptop can be time consuming and many nursing staff will want to access a laptop – often for a relatively minor system update. For this reason the laptops have a generic logon that boots into windows. The nurse then logs on to the clinical application using their normal network logon – this facilitates quick access and speedy user swapping. The laptops are tied down in general functionality.

## Technical Solution
Using our normal user account creation process we created a number of generic user accounts that matched the roles- HCA, Staff Nurse etc. These were set up on CPD just like a normal named user.
We do not create an AD/Network account to match these.
When an Agency nurse attends out of “office hours”, they report to the nurse in charge of the ward. The Nurse in charge has access to an Oracle Apex Application that we wrote in house. This application allows them to grant temporary access to the Agency Nurse;
The generic user accounts are displayed in a list;

 ![](https://github.com/kevinbeatson/kevinbeatson.github.io/blob/master/img/a2aa9c-genuser.jpg)
 
 end
 
