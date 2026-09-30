# Upstream API Notes

## Purpose

This document records the external APIs evaluated for the Federal
Business Profile. It separates verified provider behavior from design
assumptions that still need validation.

## SAM.gov Entity Management API

### Purpose in this project

[What information does this API contribute to the business profile?]

The SAM.gov Entity Management API provides public entity-registration information for the business identified by a UEI. In version 1, this information will supply the business identity, registration status, address, and available economic or business-type details for the combined profile.

Source: https://open.gsa.gov/api/entity-api/

### Base URL and endpoint

[Record the exact base URL, API version, and entity lookup endpoint.]

### Lookup input

[How does a caller request one entity by UEI?]

### Authentication

[State how the public API key is provided. Never write the real key.]

The SAM.gov Entity Management API requires a SAM.gov Public API Key. For this personal project, the key will be requested through a personal SAM.gov/Login.gov account and stored outside source control. It will not be committed to GitHub or included in this document.

Source: https://open.gsa.gov/api/entity-api/

### Relevant response data

[List only the fields relevant to your version 1 profile: legal business
name, UEI, address, registration status, and certification/business types.]

### No-result behavior

[What does the API return when a UEI does not match an entity?]

### Failure and rate-limit behavior

[Document HTTP error behavior, rate limits, and the source link where you
verified the information.]

The API documentation sets a request limit for Public API Keys. The application must handle rate-limit responses without repeatedly retrying requests or presenting stale information as current.

Verified rate limit: 1,000 calls.

Source: https://open.gsa.gov/api/entity-api/

When the limit is exceeded, the API returns 400 error.

### Open questions

- [Question you still need to answer]

## USAspending API

### Purpose in this project

[What information does this API contribute to the business profile?]

### Base URL and endpoint

[Record the exact base URL, endpoint path, and HTTP method for award search.]

### Lookup input

[Explain how a business/recipient is matched. Do not assume a UEI works
until the official documentation proves it.]

### Authentication

[State whether authentication is required.]

### Relevant response data

[List the award fields your version 1 user needs.]

### No-result behavior

[What does the API return if no awards match?]

### Failure and rate-limit behavior

[Document errors/rate limits and the source link where verified.]

### Open questions

- [Question you still need to answer]

## Integration implications

- [One difference between the APIs that affects the combined profile.]
- [One reliability or data-quality risk.]
- [One design decision this research will influence.]
