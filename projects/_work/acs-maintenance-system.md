---
layout: project
published: true
title: ACS Maintenance System

project_title: ACS Customer Services Maintenance Requests System
client: Accommodation and Commercial Services, The University of Sheffield
summary: Developed two open source Google Apps Scripts for Google Sheets for use in Customer Services Maintenance Requests System.

repos:
  - name: gs-sheets-menu
    url: https://github.com/johnellis0/gs-sheets-menu
  - name: gs-sheets-form-utils
    url: https://github.com/johnellis0/gs-sheets-form-utils
---

### Overview

ACS Customer Services implemented a Google Form and linked Google Sheet to have one central location for receiving and tracking student maintenance requests.

This system works well for customer services however there were a few issues lowering staff productivity:
 - Form submissions are not inserted after manual entries, leading to new requests getting inserted into the middle of the sheet and lost. 
 - Google Forms occasionally produces duplicate submissions, hours or even days apart. These being sent to maintenance teams can disrupt SLA's.
 - Responses need to be kept for records however they build up quickly on the main sheet so manual archiving is required.

Due to strict budgetary constraints I made the decision to improve on the current system, make use of the Universitys existing Google Workspace subscription, by implementing a Google Apps Script to fix the existing issues, improving staff productivity.

I developed a script, gs-sheets-form-utils, which provides utility functions to add extra functionality.

The actual code in production is proprietary so is not public however the two open source scripts are available to read about below and there are links to both Github repositories at the top of this page.

### gs-sheets-menu



### gs-sheets-form-utils



### Result


