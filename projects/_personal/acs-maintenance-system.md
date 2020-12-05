---
layout: project
published: true
title: ACS Maintenance System

project_title: ACS Customer Services Maintenance Requests System
client: Accommodation and Commercial Services (ACS), The University of Sheffield
summary: Developed two open source Google Apps Scripts for use in the University of Sheffield's Accommodation Customer Services Maintenance Requests System.

summary_in_full: true

repos:
  - name: gs-sheets-menu
    url: https://github.com/johnellis0/gs-sheets-menu
  - name: gs-sheets-form-utils
    url: https://github.com/johnellis0/gs-sheets-form-utils
---

## Overview

ACS Customer Services at the University of Sheffield utilizes a Google Form linked to a Google Sheet as their maintenance reporting and tracking system. Students report their issues via the form whereas CS staff can enter details directly into the spreadsheet.

The system works well for the students submitting requests and as a central record of maintenance requests before they are dispatched to the different maintenance teams.

There were however a few issues lowering staff effectiveness:
 - Form submissions were not inserted sequentially
   - If entries were manually entered into the sheet this would cause form submissions to be inserted into the middle of the sheet.
   - Due to high amount of requests it is important that new requests are inserted at the bottom so that they do not get missed.
 - Duplicate form submissions were produced occasionally
   - Students can re-submit a duplicate request if they do not close the submission confirmation page in their browser.
   - Read more about this issue on the [Google Support Forum](https://support.google.com/docs/thread/40048414?hl=en).
 - Requests needed archiving regularly
   - High amount of requests quickly leads to a high row count on the active sheet, reducing performance and increasing amount of time needed to scroll through records

Strict business and budgetary requirements greatly limited what could be done to address these problems.

I created two open-source projects to help 
 - [gs-sheets-menu](#gs-sheets-menu) - Provides utilities to detect & delete duplicates, insert form submissions sequentially and automatic archiving among others.
 - [gs-sheets-form-utils](#gs-sheets-form-utils) - Provides a sheet based menu so users can edit settings without entereing the Google Scripts editor.

The creation of these two projects then meant that a script to resolve Customer Services issues could be developed within the budgetary and time constrains as less proprietary code would be needed. This project is not available to view however information on the two open-source scripts can be found below.

## gs-sheets-menu

This adds utilities for copying & moving form submissions sequentially, duplicates detection & deletion, automatic archiving & periodic active sheets, scheduled sheet sweeps to catch any submissions missed due to Google Script server downtime, among others.

[View gs-sheets-menu on GitHub.](https://github.com/johnellis0/gs-sheets-menu)

## gs-sheets-form-utils
This adds the ability to create a sheet based settings menu.

This is beneficial as it means the script can be programmed to use the settings on the sheet menu instead of hardcoded values that would require users to go into the Scripts Editor to change.

Google Scripts supports adding native menus to the spreadsheets toolbar however for this to work the user needs to authorize the script for their Google Account 

The below screenshot shows an example menu, more are available on the [project GitHub page](https://github.com/johnellis0/gs-sheets-menu).

![image](https://user-images.githubusercontent.com/34400721/101220297-59c7a480-367d-11eb-8942-c11e64edbfef.png)

[View gs-sheets-form-utils on GitHub.](https://github.com/johnellis0/gs-sheets-form-utils)

## Outcome
The developed system has been in use since January 2020 and has proven itself to be a fast and reliable solution, processing up to thousands of requests a day during the busy periods.

It has received an overwhelmingly and entirely positive response from the other staff members who are grateful not to have to suffer from any of the original issues anymore.

The two open-source scripts have had their functionality extended beyond what is required by ACS Customer Services in the hopes that others may be able to benefit from some of their functionality.
