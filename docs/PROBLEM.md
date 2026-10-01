# Federal Business Profile Branch API - Problem Statement

## User

[Choose exactly one primary user for version 1.]

## Current problem

Information is split across public government sources; the analyst must manually search, compare, and interpret records.

## Decision supported

Whether to research the vendor further, add it to a shortlist, or identify data gaps before taking the next step.

## Version 1 outcome

A combined profile showing basic entity/registration information, relevant socioeconomic certifications, and high-level federal-award history.

## Out of scope

Login/accounts; updating SAM.gov data; procurement eligibility/risk scoring; writing data back to government systems; scraping websites.

## Decisions 

If one public data source is temporarily unavailable but the other returns usable data, the application returns a partial business profile with HTTP 200. The response identifies which source is unavailable and explains what information could not be included. The application returns HTTP 502 only when it cannot return the required profile because upstream services are unavailable or send an invalid response.
